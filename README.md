# Source Coude Editor plugin
Advanced Source Code plugin for _Tinymce WYSIWYG Editor_ built alongside _ACE_

![preview](/Preview.png)

To use this plugin copy the folder "codeeditor" and paste it into tinymce "plugins" folder in its source directory.
Here's the path for tinymce_5.2.0 self-hosted production release -> tinymce_5.2.0/tinymce/js/tinymce/plugins

Download any of tinymce self-hosted releases [here](https://www.tiny.cloud/get-tiny/self-hosted/).

## Tutorial
### Initializing
In order to have it in your editor, after including _codeeditor_ folder in your tinymce plugins directory, you must tell tinymce to inlcude the plugin as well as its toolbar button as demonstrated bellow...
```javascript
tinymce.init({
    toolbar: ["codeeditor"],
    plugins: ["codeeditor"],
});
```
### Plugin configuration
The following configuration options are provided:
  1. __codeeditor_themes_pack__ -> EITHER a __string__ with a set of words matching _ACE_ theme names with a space inbetween them OR an __array__ of strings, each matching any _ACE_ theme name. Default is _"twilight merbivore dawn kuroir"_.

```javascript
    tinymce.init({
        toolbar: ["codeeditor"],
        plugins: ["codeeditor"],
        codeeditor_themes_pack: "twilight merbivore dawn kuroir"
    });
```

```javascript
    tinymce.init({
        toolbar: ["codeeditor"],
        plugins: ["codeeditor"],
        codeeditor_themes_pack: ["twilight", "merbivore", "dawn", "kuroir"]
    });
```

Check out _ACE_ available themes [here](https://github.com/ajaxorg/ace/tree/master/lib/ace/theme). Preview [here](https://ace.c9.io/build/kitchen-sink.html).

  2. __codeeditor_wrap_mode__ -> Boolean. Default is __true__. If set to __false__, long lines won't be wrapped automatically to fit modal view size and therefore horizontal scrolling will be available.
    
```javascript
      tinymce.init({
          toolbar: ["codeeditor"],
          plugins: ["codeeditor"],
          codeeditor_wrap_mode: true
      });
```

  3. __codeeditor_font_size__ -> Number representing height in pixels. Default is __12__.
    
```javascript
      tinymce.init({
          toolbar: ["codeeditor"],
          plugins: ["codeeditor"],
          codeeditor_font_size: 12
      });
```

I am still working on this plugin... So, if you have any suggestion, let me know. Many other configuration options will be available soon.
