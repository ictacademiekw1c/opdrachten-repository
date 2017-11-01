# Opdracht 6

## Opslag in een lokale database met SQLite

## Opdrachtomschrijving

De opdracht is dat een feedbackItem uit opdracht 5 wordt opgeslagen in een lokale SQLite database (op het moment dat er op de save button wordt geklikt in scherm 1) en dat er een feedbackItem uit de database wordt gehaald (de laatst toegevoegde) op het moment dat scherm 2 wordt opgevraagd.

## Implementeren SQLite

[uitleg implementatie SQLite](https://developer.xamarin.com/guides/xamarin-forms/working-with/databases/#PCL_Android) 

[Voorbeeld App met SQLite op github](https://github.com/xamarin/xamarin-forms-samples/tree/master/Todo/SharedProject/Todo)

## Stappenplan

### 1. Installeer SQLite.Net PCL (zoek op sqlite-net-pcl van Freddy Krueger) library in zowel de Android als de Portable project van je App
### 2. Maak een interface class aan in de Portable project als overerf template voor de werkelijke implementatie

~~~c#
using SQLite;

namespace <Jouw namespace>
{
    public interface ISQLite
    {
        //alleen deze method is specifiek per platform
        SQLiteConnection GetConnection();
    }
}
~~~

### 3. Maak een class aan in het android project met de inheritance van deze interface class en een implementatie van de GetConnection() method.

~~~c#
using <jouwnamespace>.Droid;
using Xamarin.Forms;
using System.IO;

[assembly: Dependency(typeof(SQLite_FeedbackItem))]

namespace AppSQLite.Droid
{
    //inheritance van de portable interface
    public class SQLite_FeedbackItem : ISQLite
    {
        public SQLite_FeedbackItem() { }

        //implementatie van de connectie method
        public SQLite.SQLiteConnection GetConnection()
        {
            var sqliteFilename = "FeedbackItemSQLite.db3";
            string documentsPath = System.Environment.GetFolderPath(System.Environment.SpecialFolder.Personal); // Documents folder
            var path = Path.Combine(documentsPath, sqliteFilename);
            // Create the connection
            var conn = new SQLite.SQLiteConnection(path);
            // Return the database connection
            return conn;
        }

    }
} 

~~~
Hiermee is alle droid specifieke code geimplementeerd.

### 4. Implementeer de class die alle interactie met de SQLite database implementeert, dus connectie, select, insert, update en delete methods. Noem het bijvoorbeeld FeedbackItemDB.cs

~~~c#
using SQLite;
using System;

using System.Collections.Generic;
using System.Linq;
using Xamarin.Forms;

namespace <jouwnamespace>
{
    public class FeedbackItemDB
    {
        static object locker = new object();
        SQLiteConnection dbconn;

        public FeedbackItemDB()
        {
            dbconn = DependencyService.Get<ISQLite>().GetConnection();
            // create the tables
            dbconn.CreateTable<FeedbackItem>();
        }

        public IEnumerable<FeedbackItem> GetItems()
        {
            lock (locker)
            {
                return (from i in dbconn.Table<FeedbackItem>() select i).ToList();
            }
        }

        public FeedbackItem GetItem(int id)
        {
            lock (locker)
            {
                return dbconn.Table<FeedbackItem>().FirstOrDefault(x => x.ID == id);
            }
        }

        public int SaveItem(FeedbackItem item)
        {
            lock (locker)
            {
                if (item.ID != 0)
                {
                    dbconn.Update(item);
                    return item.ID;
                }
                else
                {
                    return dbconn.Insert(item);
                }
            }
        }

        public int DeleteItem(int id)
        {
            lock (locker)
            {
                return dbconn.Delete<FeedbackItem>(id);
            }
        }
    }
}
~~~

### 5. Breidt de __FeedbackItem__ class aan met een ID en wat assembly directives voor de SQLite library om de database - tabel te kunnen aanmaken/gebruiken.

~~~c#

using SQLite;

namespace <jouwnamespace>
{
    public class FeedbackItem
    {
        //aanwijzingen voor sqlite voor de primaitre sleutel
        [PrimaryKey, AutoIncrement]
        public int ID { get; set; }
        public string Naam { get; set; }

        ...(etc)

~~~

### 6. Instantieer een FeedbackitemDB object in je app class, zodat je die beschikbaar hebt in al je pages.
~~~c#
   public class App : Application
    {
        //dit heb je al
        public App()
        {
            MainPage = new NavigationPage(new SurveyPage());
        }

        static FeedbackItemDB db;

        public static FeedbackItemDB Db
        {
            get
            {
                if (db == null)
                {
                    db = new FeedbackItemDB();
                }
                return db;
            }
        }
~~~

### 7. Gebruik het db object om een FeedbackItem op te slaan in je SurveyPage class bij het clicken op de submit button.

~~~c#
    //Opslaan in de database
    App.Db.SaveItem(ViewModel.Feedback);
~~~

### 8. Wil je in je pagina alle FeedbackItems ophalen dan doe je dat alsvolgt:

~~~c#

//Onderzoek waar je deze code moet plaatsen
FeedbackItems = new ObservableCollection<FeedbackItem>(App.Db.GetItems());

~~~
