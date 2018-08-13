[![Build Status](https://www.myget.org/BuildSource/Badge/xam-plugin-simpleappintro?identifier=ef243495-8aec-4134-af86-1d4e3d1bf1c3)](https://www.myget.org/)  [![nuget](https://img.shields.io/nuget/v/Xam.Plugin.SimpleAppIntro.svg)](https://www.nuget.org/packages/Xam.Plugin.SimpleAppIntro/)

# Xam.Plugin.SimpleAppIntro
Just a nice and simple AppIntro for your Xamarin Forms project 


# Setup
* Available on Nuget:
https://www.nuget.org/packages/Xam.Plugin.SimpleAppIntro

!!Install into your .net standaard project. !!


# Screenshots
![example1](https://raw.githubusercontent.com/galadril/Xam.Plugin.SimpleAppIntro/master/1.png) ![example2](https://raw.githubusercontent.com/galadril/Xam.Plugin.SimpleAppIntro/master/2.png)


# Usage
You can now create new simple sliders and add them to a SimpleAppIntro page 

```
var welcomePage = new SimpleAppIntro();

// Add some simple slides
welcomePage.AddSlide("Welcome", "This is a sample app showing off the new App Intro", "cup_icon.png");
welcomePage.AddSlide("Slides", "You can add slides and have a clean app intro", "cup_icon.png");
welcomePage.AddSlide("Other", "Tell your user what they can do with your app", "cup_icon.png");

MainPage.Navigation.PushModalAsync(welcomePage);
```


# Animated
You can also specify your own Lottie animated icon for each slide. Just create an AnimatedSimpleAppIntro like:

```
var welcomePage = new AnimatedSimpleAppIntro();

// Add some simple slides
welcomePage.AddSlide("Welcome", "This is a sample app showing off the new App Intro", "world.json");
```


# Properties
You can set the next properties

```
welcomePage.DoneText = "Finish";
welcomePage.SkipText = "Skip";
welcomePage.NextText = "Next";

welcomePage.ShowPositionIndicator = true;
welcomePage.ShowSkipButton = true;
welcomePage.ShowNextButton = true;
```


# Theming
You can set the next colors

```
welcomePage.BarColor = "#607D8B";
welcomePage.SkipButtonBackgroundColor = "#FF9700";
welcomePage.DoneButtonBackgroundColor = "#8AC149";
welcomePage.NextButtonBackgroundColor = "#8AC149";

welcomePage.SkipButtonTextColor = "#FFFFFF";
welcomePage.NextButtonTextColor = "#FFFFFF";
welcomePage.DoneButtonTextColor = "#FFFFFF";
```

And you can also specify an image instead of the default skip/done/next buttons:

```
welcomePage.DoneButtonImage = "baseline_done_white_24.png";
```



# Callback 
You can use the two callback methods to get more info on the events 

```
welcomePage.OnSkipButtonClicked = OnSkipButtonClicked;
welcomePage.OnDoneButtonClicked = OnDoneButtonClicked;
	  
/// <summary>
/// On skip button clicked
/// </summary>
private void OnSkipButtonClicked()
{
	Console.Write("Skip button clicked");
}

/// <summary>
/// On done button clicked
/// </summary>
private void OnDoneButtonClicked()
{
	Console.Write("Done button clicked");
}
```

