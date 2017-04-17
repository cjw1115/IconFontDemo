# IconFontDemo
Xmarin.Forms Custon Font solution,contains icon font,like FontAewsome

### 关于如何在Xamarin.Forms中使用字体图标的一片博文（比较旧，但可以作为参考）
图标字体-fontaewsome
https://www.devdashboard.com/280/using-font-icons-for-xamarin-forms

### 自定义字体(Xamarin官网提供的解决办法，Perfect)

https://developer.xamarin.com/guides/xamarin-forms/user-interface/text/fonts/#Using_a_Custom_Font

### 注意
iOS需要在info.plist添加字体文件的说明:

`
<key>UIAppFonts</key>
<array>
  <string>Fonts/fontawesome-webfont.ttf</string>
</array>
`

### 如何使用？

        <ResourceDictionary>
            <OnPlatform x:Key="FontAwesome"
            x:TypeArguments="x:String"
            iOS="FontAwesome"
            Android="Fonts/fontawesome-webfont.ttf#FontAwesome"
            WinPhone="/Assets/Fonts/fontawesome-webfont.ttf#FontAwesome" />
        </ResourceDictionary>
        
在App.Xaml中一个平台特定的字符串资源，然后在需要使用FontFamily的地方用使用静态资源的方式引用即可


        <Label  Text="&#xf015;" TextColor="Red" FontFamily="{StaticResource FontAwesome}"    FontSize="50"></Label>

