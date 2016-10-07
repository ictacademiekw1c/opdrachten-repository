# Opdracht 5

## 5.1 Xaml pagina's en databinding

In xaml pagina's declareer je in feite de opbouw en de elementen van een scherm.
Als er geen koppeling zou zijn met variabelen, classes en events zou het een statische scherm blijven.
Met binding kun je ervoor zorgen dat scherm(/-onderdelen) gekoppeld zijn aan je code en daardoor dynamisch is.
 
## 5.2 Voorbeeld aan de hand van de feedback App

We gaan uit van een app met het volgende scherm als startscherm:

![Startscherm](https://github.com/ictacademiekw1c/opdrachten-repository/blob/master/xamarin/images/binding1.png?raw=true)

Dit scherm is alsvolgt opgebouwd:
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
							<Entry Text="{Binding Naam}" />
						</StackLayout>
						<StackLayout Spacing="0">
							<Label Text="Geslacht:" />
							<StackLayout Orientation="Horizontal">
								<Label Text="Man" VerticalOptions="Center" />
								<Switch IsToggled="{Binding Geslacht}" />
								<Label Text="Vrouw" VerticalOptions="Center" />
							</StackLayout>
						</StackLayout>
						<StackLayout Spacing="0">
							<Label Text="Verjaardag:" />
							<DatePicker Date="{Binding Verjaardag}" />
						</StackLayout>
						<StackLayout Spacing="0">
							<Label Text="Cijfer:" />
							<StackLayout Orientation="Horizontal">
								<Stepper x:Name="cijferStepper" Value="{Binding Cijfer}" Minimum="0" Maximum="10" />
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


