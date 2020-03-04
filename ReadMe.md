## FontMenuCombo

# Features

* ## FontMenu sample
    User can select FontFamily,FontStyle,FontWeight and FontSize, or reset to default font.

* ## FontComboBox sample
    User can select FontFamily,FontStyle,FontWeight and FontSize.

* class ResourceKeySetting
Value property is set from Settings.Settings.
If Settings.Settings value is default value, Value property uses DynamicResource.

## example
````
Settings.Settings
Name=MyFontSize, Type=string, Default= (empty string)

<Resources>
    <ResourceKeySetting x:Key="MyFontSize"
	    ResourceKey="{x:Static SystemFonts.MessageFontSizeKey}"
        SettingName="MyFontSize"/>
</Resources>

<TextBlock
    Text="SampleText"
    FontSize="{Binding Source={StaticResouce MyFontSize},Path=Value}"/>
````
