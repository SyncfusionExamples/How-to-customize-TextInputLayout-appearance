# How to customize TextInputLayout appearance 
This demo sample explains how to customize TextInputLayout appearance 
# Adding SfTextInputLayout reference
You can add SfTextInputLayout reference using one of the following methods:

## Method 1: Adding SfTextInputLayout reference from nuget.org

Syncfusion Xamarin components are available in nuget.org. To add SfTextInputLayout to your project, open the NuGet package manager in Visual Studio, search for Syncfusion.Xamarin.Core, and then install it.


## Method 2: Adding SfTextInputLayout reference from toolbox

Syncfusion also provides Xamarin Toolbox. Using this toolbox, you can drag the Xamarin Text Input Layout (SfTextInputLayout) control to the XAML page. It will automatically install the required NuGet packages and add the namespace to the page. To install Syncfusion Xamarin Toolbox, refer to Toolbox.

## Method 3: Adding SfTextInputLayout assemblies manually from the installed location

If you prefer to manually reference the assemblies instead referencing from NuGet, add the following assemblies in respective projects.

# Initializing text input layout
Import the SfTextInputLayout control namespace in respective page as demonstrated in the following code sample.

**[XAML]**
```
xmlns:inputLayout="clr-namespace:Syncfusion.XForms.TextInputLayout;assembly=Syncfusion.Core.XForms"
```
**[C#]**
```
using Syncfusion.XForms.TextInputLayout;
```
Add any input view control such as Entry, Editor, SfNumericTextBox, SfNumericUpDown, SfMaskedEdit, SfAutoComplete, SfComboBox, Picker,DatePicker or TimePicker and add hint label (floating label).

**[XAML]**
```
<inputLayout:SfTextInputLayout>
   <Entry />
</inputLayout:SfTextInputLayout>
```
**[C#]**
```
var inputLayout = new SfTextInputLayout();
inputLayout.InputView = new Entry();
```

# How to customize the properties of (outline border colors, hint name, helper text, error text, and char count) of TextInputLayout in Xamarin.Forms
Color customization of outline border can be achieved by setting respective color for FocusedColor (focussed state) and UnfocusedColor (unfocussed state) properties of SfTextInputLayout as shown in below code snippet.

**[XAML]**
```
<StackLayout VerticalOptions="Center" HorizontalOptions="StartAndExpand">
    <inputLayout:SfTextInputLayout Hint="Email"              ContainerType="Outlined" 
    HelperText="Enter your email" 
    FocusedColor=" DarkCyan" 
    UnfocusedColor="Gray"><Entry/>
    </inputLayout:SfTextInputLayout>
</StackLayout>

```
## Color Customization for Assistive Labels
By merging the below mentioned keys in application resources, it is possible to customize the appearance of the SfTextInputLayout without merging common theme resource and control style resource dictionaries as shown in below code snippet.

**[XAML]**
```
<Application.Resources>
        <syncTheme:SyncfusionThemeDictionary>
            <syncTheme:SyncfusionThemeDictionary.MergedDictionaries>
                <ResourceDictionary>
                    <x:String x:Key="SfTextInputLayoutTheme">CustomTheme</x:String>
                    <!--Hint Color for focused state-->
                    <Color x:Key="SyncPrimaryLightColor"> Black </Color>
                    <!--Hint Color for default state-->
                    <Color x:Key="SfTextInputLayoutHintColor">Gray</Color>
                    <!--Border Color for focused state-->
                    <Color x:Key="SyncPrimaryColor"> DarkCyan </Color>
                    <!--Border Color for default state-->
                    <Color x:Key="SfTextInputLayoutLineColor">Gray</Color>
                    <!--Helper text Color for default state-->
                    <Color x:Key="SfTextInputLayoutHelperTextColor"> BlueViolet</Color>
                    <!--Character count text Color for default state-->
                    <Color x:Key="SfTextInputLayoutCounterLabelColor"> DarkGoldenrod</Color>
                    <!--Error text Color for default state-->
                    <Color x:Key="SfTextInputLayoutErrorTextColor">Red</Color>
                </ResourceDictionary>
            </syncTheme:SyncfusionThemeDictionary.MergedDictionaries>
        </syncTheme:SyncfusionThemeDictionary>
    </Application.Resources>

```
## How to run this application?

To run this application, you need to first clone the How-to-validate-with-required-verification-in-text-input-layout-in-Xamarin.Forms repository and then open it in Visual Studio 2022. Now, simply build and run your project to view the output.

## <a name="troubleshooting"></a>Troubleshooting ##
### Path too long exception
If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.

## License

Syncfusion has no liability for any damage or consequence that may arise by using or viewing the samples. The samples are for demonstrative purposes, and if you choose to use or access the samples, you agree to not hold Syncfusion liable, in any form, for any damage that is related to use, for accessing, or viewing the samples. By accessing, viewing, or seeing the samples, you acknowledge and agree Syncfusion’s samples will not allow you seek injunctive relief in any form for any claim related to the sample. If you do not agree to this, do not view, access, utilize, or otherwise do anything with Syncfusion’s samples.