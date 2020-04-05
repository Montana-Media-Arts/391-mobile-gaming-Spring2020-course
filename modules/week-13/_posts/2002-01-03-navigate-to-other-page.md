---
title: Multiple Pages
module: 13
jotted: true
---

# Go to a Different Page

<a href="https://umontana.zoom.us/rec/play/v8AtI-z--jk3TNSX4gSDCqQsW9TsJqqsgSMfq6dYmR3mAHgKMQf3Y7tBM7TLkezls5KeTECq3sLfqhqW?continueMode=true&_x_zm_rtaid=DlWtLI-zRlCUpYLqasgjPA.1585764072172.6cf1bc0be13f13c9ac0eb5ca428d956c&_x_zm_rhtaid=855">Video</a>

One of the things that you might find valuable is navigating from one page to another. How does one do that in Xamarin?  For this to work, one must use asynchronous calls to take the user from one page to another.

First, let's add a new page.  Right-click the project and create a new Content page.  Name the page, Page2.  Alter the new page so that it indicates that we are on the second page.

Then, go back to the first page and add a new button.

```html
<Button Text="Other Page!"
    HorizontalOptions="Center"
    VerticalOptions="CenterAndExpand"
    Clicked="OnButtonClickedAsync"/>
```

Notice the new click event.  It requires a new asynchronous method in the C#. It looks like this.

```csharp
async void OnButtonClickedAsync(object sender, EventArgs args)
{     
    await Navigation.PushAsync(new NavigationPage(new Page2()));
}
```

Don't forget to change the App.xaml.cs page, so that it says the following

```csharp
 MainPage = new NavigationPage(new MainPage());
```

instead of

```csharp
 MainPage = new MainPage();
```

Rerun the simulator and make sure that when you click the new button, it takes you to the second page.