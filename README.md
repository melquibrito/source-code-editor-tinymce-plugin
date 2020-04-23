# Source Code Editor
Advanced Source Code Editor plugin for [Tinymce WYSIWYG Editor](https://www.tiny.cloud/) built alongside [ACE](https://ace.c9.io/#nav=about&api=editor)

![preview](/Preview.png)

To use this plugin copy the folder "codeeditor" and paste it into tinymce "plugins" folder in its source directory.
Here's the path for tinymce_5.2.0 self-hosted production release -> tinymce_5.2.0/tinymce/js/tinymce/plugins

Download any of tinymce self-hosted releases [here](https://www.tiny.cloud/get-tiny/self-hosted/).

## Tutorial
### Initializing
In order to have it in your editor, after including _codeeditor_ folder in your tinymce plugins directory, you must tell tinymce to inlcude the plugin as well as its toolbar button as demonstrated bellow...
```javascript
tinymce.init({
    selector: "#target-element", // change this value according to your HTML target element selector
    toolbar: ["codeeditor"],
    plugins: ["codeeditor"],
});
```
### Plugin configuration
The following configuration options are provided:
  1. __codeeditor_themes_pack__ -> EITHER a __string__ with a set of words matching _ACE_ theme names with a space inbetween them OR an __array__ of strings, each matching any _ACE_ theme name. Default is _"twilight merbivore dawn kuroir"_.

Check out _ACE_ available themes [here](https://github.com/ajaxorg/ace/tree/master/lib/ace/theme). Preview [here](https://ace.c9.io/build/kitchen-sink.html).

  2. __codeeditor_wrap_mode__ -> Boolean. Default is __true__. If set to __false__, long lines won't be wrapped automatically to fit modal view size and therefore horizontal scrolling will be available.

  3. __codeeditor_font_size__ -> Number representing height in pixels. Default is __12__.
    
```javascript
      tinymce.init({
          selector: "#target-element", // change this value according to your HTML target element selector
          toolbar: ["codeeditor"],
          plugins: ["codeeditor"],
          codeeditor_themes_pack: "twilight merbivore dawn kuroir", // or ["twilight", "merbivore", "dawn", "kuroir"]
          codeeditor_wrap_mode: true,
          codeeditor_font_size: 12
      });
```

## Author
* [Melqui Brito](https://github.com/melquibrito)
    
## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for more details.
