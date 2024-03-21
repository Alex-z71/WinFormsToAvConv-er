# WinFormsToAvConv-er

The converter allows you to convert a Windows Forms application to an Avalonia UI application. 

It uses Eremex Avalonia UI controls as a replacement for standard and third-party WinForms controls.

The converter allows you to migrate invdividual files and projects to Avalonia UI.

## 


## Convert Individual Files

Converting individual files is handy for large projects that consist of, say, hundreds of forms.
+ Удобны при отладке конвертера ----??????
After conversion, you need to manually add converted files to your Avalonia project.

## Convert Projects

For small projects, you can use the converter to convert the entire pproject. 
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

  
