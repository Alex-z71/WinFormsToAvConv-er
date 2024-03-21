# WinForms2AvaloniaConverter

The Converter allows you to convert a Windows Forms project to an Avalonia UI project. It also allows you to convert individual files instead of entire projects.

WinForms2AvaloniaConverter converts UI controls according to your control mapping rules, generates View and View Model classes, transfers images and localization resources, and also extracts ______business logic bound to the UI controls________ ???????????????????

The Converter analyzes the source application's Forms that you open at runtime. It recursively iterates through the Controls collection of opened Forms, and collects information about the names, position, size of the controls and _____their properties______.
_________свойства данных___.????? Once data is collected, it generates the destination project/files.


## Convert Individual Files or Projects

Converting individual files is handy for large projects that consist of, say, hundreds of forms. You can iteratively convert files, check the result and then safely move the converted files to your destination project.
Also, you can use individual file conversion to test the converter.

For small projects, you can use the Converter to convert the entire project. After the conversion you may need to refine the application's code and ______configuration__________????
- Сложнее сочетать создание проекта с его ручной доводкой   ----??????

## Converting UI and Business Logic

_____WinForms *.cs and *.Design.cs____
откуда конвертер знает про файлы, если он запускается в рантайме????????????????
files are converted to Avalonia UI *.axaml, *.axaml.cs, and *.cs files.

View classes are created for Form and UserControl classes. During the conversion, the Converter extracts the business logic from the source WinForms files, and generates *.cs files that contain View Models implementing this logic.

The Converter uses customizable control mapping rules that determine which controls to convert to which controls. You need to adjust these rules to perform the correct conversion.

According to the position and size of controls in the source application, the Converter creates a corresponding layout of controls in the destination project/files.

_________If controls are bound in the source file, the Converter binds the destination control to a correposnding property in a View Model.___________

## Converting Resources

The *.resx files are processed to transfer text properties of controls. The "Text" and "Caption" properties are transferred by default, while other properties (for instance, Name, Parent, ZOrder, and Type) saved in source *.resx files are skipped.

The converter extracts images stored in *.resx files and saves them as standalone image files in the destination folder.

## Converting Localized Resources

The *.&lt;Localized&gt;.resx files are converted to _________Avalonia UI format_________ ??????????

  
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
