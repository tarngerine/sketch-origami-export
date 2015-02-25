Export for Origami
=====================

Exports and updates Sketch assets for Facebook's [Origami](https://facebook.github.io/origami) prototyping toolkit for Quartz Composer, adapted from [sketch-framer](https://github.com/bomberstudios/sketch-framer).

## Installation
You can [Download Zip](https://github.com/tarngerine/sketch-origami-export/archive/master.zip) to the right and double-click on the .sketchplugin file to install. Important note: symbols are not supported — please remove all symbols before running.

[Watch video tutorial](https://vimeo.com/120452278)

## How it works
This plugin takes all visible layers, in or out of artboards, and exports them into a temp directory for easy drag & drop into Origami (More info below). As you make changes and work back and forth between Sketch and Origami, run the plugin again and see it updated live with the Live Image patch.

Hit `Control + Command + Option + O` to run the plugin, and it will first prompt you for the export scale (e.g. if you're working @2x already, the default of 1x export scale will export @2x).

![](http://cl.ly/image/3Y0f121s3L2c/Export%20for%20Origami%20Finished.png)

![](http://cl.ly/image/2N0H0j3Z0l0u/Export%20for%20Origami%20Folder.png)

All groups and layers appended with `+` will become an individual PNG, sorted into folders with their containing artboard names.

## More info
- Drag the whole export directory, while holding `Command + Option` to automatically create Live Image patches with the paths to the assets:
![](http://cl.ly/image/3G1m1G12083o/Export-for-Origami-Live-Image.png)

- Append a group name with `*` to flatten all subgroups within (note: you do not need to flatten groups that do not have subgroups, as layers will automatically fold into the containing group)
- Append a layer name with `+` to become its own file
- Append a group or layer name with `-` to skip the layer

- Exports are stored in Sketch's temp directory due to sandboxing. Every time you run the plugin, it opens the temp directory in Finder (`Command + Option + W` to close all Finder windows).

- The plugin creates a hidden '.origamiblueprint' file that saves the scale factor you indicated on the first export for future exports without a dialog prompting every time.

## Miscellaneous
Please file an issue or post in the [Origami Community](https://www.facebook.com/groups/origami.community/) page on Facebook if there is a problem! 

Big thanks goes out to Ale Muñoz and Cemre Güngör for their work on sketch-framer.
