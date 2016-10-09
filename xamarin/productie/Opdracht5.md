# Opdracht 5

## 5.1 Xaml pagina's en databinding

In xaml pagina's declareer je in feite de opbouw en de elementen van een scherm.
Als er geen koppeling zou zijn met variabelen, classes en events zou het een statische scherm blijven.
Met binding kun je ervoor zorgen dat scherm(/-onderdelen) gekoppeld zijn aan je code en daardoor dynamisch is.
 
## 5.2 Voorbeeld aan de hand van de feedback App


Hieronder een feedback App die bestaat uit 2 schermen:
1. Een invoerscherm met een aantal usercontrols(views).
2. Een resultaatscherm met een overzicht van de ingevulde waardes.

Deze App laat zien hoe gegevens in het ene scherm via binding (via een viewmodel object) doorgegeven worden aan een andere scherm door het viewmodel object door te geven.

    > Invoerscherm: 
![Startscherm](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/binding1.png?raw=true)

    > Resultaatscherm
![Resultaatscherm](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/binding2.png?raw=true)

Het invoerscherm is alsvolgt opgebouwd:
~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentPage Title="KW1C Feedback App" Padding="20" xmlns="http://xamarin.com/schemas/2014/forms" xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml" x:Class="Databinding.Pages.SurveyPage">
	<ContentPage.Content>
		<ScrollView>
			<StackLayout>
				<StackLayout x:Name="surveyView" IsVisible="True">
					<StackLayout Spacing="20">
						<StackLayout Spacing="0">
							<Label Text="Naam:" />
							<Entry Text="{Binding Feedback.Naam}" />
						</StackLayout>
						<StackLayout Spacing="0">
							<Label Text="Geslacht:" />
							<StackLayout Orientation="Horizontal">
								<Label Text="Man" VerticalOptions="Center" />
								<Switch IsToggled="{Binding Feedback.Geslacht}" />
								<Label Text="Vrouw" VerticalOptions="Center" />
							</StackLayout>
						</StackLayout>
						<StackLayout Spacing="0">
							<Label Text="Verjaardag:" />
							<DatePicker Date="{Binding Feedback.Verjaardag}" />
						</StackLayout>
						<StackLayout Spacing="0">
							<Label Text="Cijfer:" />
							<StackLayout Orientation="Horizontal">
								<Stepper x:Name="cijferStepper" Value="{Binding Feedback.Cijfer}" Minimum="0" Maximum="10" />
								<Label Text="{Binding Value}" BindingContext="{x:Reference cijferStepper}" />
							</StackLayout>
						</StackLayout>
						<StackLayout Spacing="0">
							<Label Text="Locatie:" />
							<Picker x:Name="locatie" />
						</StackLayout>
						<Button Text="Submit" Clicked="SubmitData" />
					</StackLayout>
				</StackLayout>
			</StackLayout>
		</ScrollView>
	</ContentPage.Content>
</ContentPage>
~~~

In dit scherm hebben we verschillende typen usercontrols:
- Een default entry = een standaard invoerveld
- Een toggle of switch, hierboven gebruikt voor man of vrouw
- Een datumpicker om de gebruiker op eenvoudige wijze een datum te laten kiezen
- Een stepper waarmee de gebruiker met +/- buttons de waarde kan ophogen of verlagen
- Een picker oftewel een dropdown lijst waaruit de gebruiker er een kan kiezen

Hierboven is deze xaml pagina reeds voorbereid op binding met je code met behulp van de syntax {Binding [bindingvariabele]}

Voorbeeld van hierboven:
~~~xml
        <Entry Text="{Binding Naam}" />
~~~
en
~~~xml
		<Stepper x:Name="cijferStepper" Value="{Binding Cijfer}" Minimum="0" Maximum="10" />
		<Label Text="{Binding Value}" BindingContext="{x:Reference cijferStepper}" />
~~~

Het resultaatscherm is alsvolgt:
~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<ContentPage Title="Uitslag" xmlns="http://xamarin.com/schemas/2014/forms" xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml" x:Class="Databinding.Pages.ResultPage">
	<ContentPage.Content>
		<StackLayout Padding="20">
			<Label Text="Uitslag" FontSize="Large" FontAttributes="Bold" />
			<BoxView HeightRequest="1" BackgroundColor="Gray" HorizontalOptions="FillAndExpand" />

			<Label Text="Naam:" FontAttributes="Bold" />
			<Label Text="{Binding Naam}" />

			<Label Text="Geslacht:" FontAttributes="Bold" />
			<Label Text="{Binding Geslacht}" />

			<Label Text="Verjaardag:" FontAttributes="Bold" />
			<Label Text="{Binding Verjaardag}" />

			<Label Text="Cijfer:" FontAttributes="Bold" />
			<Label Text="{Binding Cijfer}" />

			<Label Text="Locatie:" FontAttributes="Bold" />
			<Label Text="{Binding Locatie}" />
		</StackLayout>
	</ContentPage.Content>
</ContentPage>
~~~



