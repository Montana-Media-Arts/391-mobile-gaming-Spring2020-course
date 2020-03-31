---
title: Multiple Pages
module: 13
jotted: true
---

# Go to a Different Page

One of the things that you might find important is navigating from one page to another. How does one do that in Xamarin?  In order for this to work, one must use asynchronous calls to take the user from one page to another.

First, let's add a new page.  Right-click the project and create a new Content page.  Name is Page2.  Alter the new page so that it indicates that we are on the a different page.

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

Run the simulator again and make sure that when you click the new button, it takes you to the second page.



