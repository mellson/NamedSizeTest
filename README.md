# NamedSizeTest
Xamarin Project for showcasing a problem with Named Font Sizes not being applied

There are styles for each font size enum in `App.xaml`
I have tried using two different `TypeArguments` - both have no effect:

```
<Setter Property="FontSize">
    <OnPlatform x:TypeArguments="x:String"
      Android="Micro"
      iOS="Micro"
      WinPhone="Micro"/>
</Setter>
```

and

```
<Setter Property="FontSize">
    <OnPlatform x:TypeArguments="NamedSize"
      Android="Micro"
      iOS="Micro"
      WinPhone="Micro"/>
</Setter>
```



Named font sizing are currently not being applied correctly in Xamarin Forms.
Small discussion about it here: https://forums.xamarin.com/discussion/comment/263548

When you run the app you will see that it looks like this:

![img](https://github.com/appbureauet/NamedSizeTest/raw/master/Style1.png)

When it actually should look like this:

![img](https://github.com/appbureauet/NamedSizeTest/raw/master/Style2.png)
