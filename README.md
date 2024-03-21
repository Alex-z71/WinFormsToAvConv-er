# WinFormsToAvConv-er

The converter allows you to convert a Windows Forms application to an Avalonia UI application. 

It uses Eremex Avalonia UI controls as a replacement for standard and third-party WinForms controls.

The converter converts Winforms-specific files to Avalonia-specific files.

*.cs, *.Design.cs -> *.axaml, *.axaml.cs and *.cs (View Model)
*.resx -> *.resx
*.<Localized>.resx -> *.<Localized>.resx

- Creates files that encapsulate Views and View Models
- Extracts localization resources
- Extracts images from resources
- Creates a layout of controls
- Creates properties in View Modesl and binds them to a View's controls

  
