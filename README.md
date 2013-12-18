app preferences cordova plugin
-----------------------

compatible with phonegap 3.0

originally ported from:
https://github.com/phonegap/phonegap-plugins/tree/master/iOS/ApplicationPreferences

android untested (for now)

another android implementation:
https://github.com/macdonst/AppPreferences


To install this plugin, follow the [Command-line Interface Guide](http://cordova.apache.org/docs/en/edge/guide_cli_index.md.html#The%20Command-line%20Interface).

If you are not using the Cordova Command-line Interface, follow [Using Plugman to Manage Plugins](http://cordova.apache.org/docs/en/edge/guide_plugin_ref_plugman.md.html).


Extracted from another similar plugin
-------------------------------------

Plugin:

https://github.com/drpicox/cordova-ios-application-preferences


## Using the plugin ##
The plugin creates the object `window.plugins.applicationPreferences` with two methods `get(name, success, fail)` and 
`set(name, value, success, fail)`. `name` is the name of the setting you want, `value` is the value of the setting you want to set.

`success` and `fail` are callback functions. Success is passed the settings value as a string.
A full get example could be:

```javascript
    window.plugins.applicationPreferences.get('name_identifier', function(result) {
            alert("We got a setting: " + result);
        }, function(error) {
		    alert("Failed to retrieve a setting: " + error);
	    }
	);
```

A full set example could be:

```javascript
    window.plugins.applicationPreferences.set('name_identifier','homer' function() {
            alert("It is saved");
        }, function(error) {
		    alert("Failed to retrieve a setting: " + error);
	    }
	);
```

NOTE: The preference must exist in a settings bundle and Root.plist in your project. See http://developer.apple.com/library/ios/#DOCUMENTATION/Cocoa/Conceptual/UserDefaults/Preferences/Preferences.html for further details.

## Registering the plugin ##

1. Open Cordovo.plist file in Xcode
2. To the plugins Dictionary add a new String item
3. Name and value of the item would be "applicationPreferences"
