---
title: Get Information
module: 13
jotted: true
---

# Get Information

<a href="https://umontana.zoom.us/rec/play/75J4duv5_zI3S9GQ5QSDBvAtW47pLaOs0SQbq_Fcmh23U3MBYQGjNLFBZuUEr8iuIwwb7LTkFg05R-qN?continueMode=true&_x_zm_rtaid=DlWtLI-zRlCUpYLqasgjPA.1585764072172.6cf1bc0be13f13c9ac0eb5ca428d956c&_x_zm_rhtaid=855">Video</a>

What is more interesting though is how we get information from the user.  We use the Entry tag to get it.

Add the following to the XAML page.

```html
    <Entry x:Name="name" Text="I am here" MaxLength="10" TextColor="Green"/>
```

However, we need to get the information from the textbox.

The following code retrieves the information when the button is clicked.

```csharp
 var myName = name.Text;
```

Now, we concatenate the name to the number of clicks.

The new code looks like this.

```csharp
int count = 0;
void Button_Clicked(object sender, System.EventArgs e)
{
     var myName = name.Text;
    count++;
    ((Button)sender).Text = $"You clicked {count} times." + myName;
}
```




