# WinForms2AvaloniaConverter

The converter allows you to convert a Windows Forms project to an Avalonia UI project. It also allows you to convert individual files instead of entire projects.

WinForms2AvaloniaConverter converts UI controls according to your rules, extracts and transfers images and localization resources, and also ______moves business logic bound to the UI controls________ ???????????????????


## Convert Individual Files or Projects

Converting individual files is handy for large projects that consist of, say, hundreds of forms. You can iteratively convert files, check the result and then safely move the converted files to your destination project.
Use individual file conversion to test the converter.

For small projects, you can use the converter to convert the entire project. After the conversion you may need to refine the application's code and ______configuration__________????
- Сложнее сочетать создание проекта с его ручной доводкой   ----??????

## What Files are Converted?
The converter converts Winforms-specific files to Avalonia UI-specific files. During the conversion, the converter extracts the business logic from the source WinForms files and moves it to separate Avalonia *.cs files.

UI and business logic: *.cs, *.Design.cs -> *.axaml, *.axaml.cs, and *.cs (View Model)
Resources: *.resx -> *.resx
Localized resources: *.<Localized>.resx -> *.<Localized>.resx

- Creates files that encapsulate Views and View Models
- Extracts localization resources
- Extracts images from resources
- Creates a layout of controls
- Creates properties in View Modesl and binds them to a View's controls





## How the Converter Works
The Converter analyzes the source application's Forms that you open at runtime. It recursively iterates through the Controls collection of opened Forms, and collects information about the names, position, size of the controls and _____their properties______.
_________свойства данных___.????? Once data is collected, 
  
## Get Started with Project Conversion

1. Download and then open the WinForms2AvaloniaConverter project in Visual Studio.
2. Customize mapping rules for types and namespaces used in your source project according to your needs.
3. Compile the WinForms2AvaloniaConverter library, or create a NuGet package for the WinForms2AvaloniaConverter library.
4. Include the created library/NuGet package into your project that needs to be converted. Alternatively, you can include the source files of the WinForms2AvaloniaConverter library into your project.
5. In your project, inherit all `System.Windows.Forms.Form` objects from the `WAConverter.WAForm` class, and inherit all `System.Windows.Forms.UserControl` objects from the `WAConverter.UserControl` class.
6. Run your application.
7. Open all forms and user controls at runtime, so the converter can analyze them.
8. Copy code that was not converted to the destination project.
   
- куда попадает результат конвертации
- 

## Get Started with Individual Project Conversion

...
- Access the result of the conversion in the `./Bin/../Converted` folder, and then copy the converted files to the destination project.

## UI Control Conversion

It uses Eremex Avalonia UI controls as a replacement for standard and third-party WinForms controls.
