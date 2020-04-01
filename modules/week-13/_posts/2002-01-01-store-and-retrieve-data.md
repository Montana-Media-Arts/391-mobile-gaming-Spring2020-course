---
title: Store and Retrieve Data
module: 13
jotted: true
---

# Store Data

<a href="https://umontana.zoom.us/rec/play/7sIvce2t_D03GYfA4wSDAfN8W467LKms1iFP_vULzErnUHcLOlfzMOAaaseyy60hS1Nue43Mx0BaEvE?continueMode=true&_x_zm_rtaid=DlWtLI-zRlCUpYLqasgjPA.1585764072172.6cf1bc0be13f13c9ac0eb5ca428d956c&_x_zm_rhtaid=855">Video</a>

We are going to store our information in a file.  When we get the information, we will write it to a file.  Then, we will click a different button to display the information.

The following shows how one stores the data in a file.

```csharp
File.WriteAllText(fileName, text);
```
Just don't forget to import **System.IO;**

For our example, we will change it so that it looks like this.

```csharp
int count = 0;
void Button_Clicked(object sender, System.EventArgs e)
{
    var myName = name.Text;
    count++;
    ((Button)sender).Text = $"You clicked {count} times." + myName;

    string fileName = Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.LocalApplicationData), "temp.txt");
    
    File.WriteAllText(fileName, myName);

}
```

# Retrieve Data

After writing to the file, we want to read from the file.  In order to access the file, you must access the file path again and then read the text.

Here is a code example.

```csharp
string text = File.ReadAllText(fileName);
```

Let's update the XAML and then write the following stored information to the label.

```html
<Label x:Name="ActualText"></Label>
<Entry x:Name="name" Text="I am here" MaxLength="10" TextColor="Green"/>
<Button Text="Click Me" Clicked="Button_Clicked" />
```

To update the Label, we need to change the C# code to look like this.

```csharp
string fileName = Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.LocalApplicationData), "temp.txt");
string text = File.ReadAllText(fileName);
ActualText.Text = "Hi there " + text;
```