JavaScript inheritance

All JavaScripts defined in the parent theme will be inherited.

Overriding inherited JavaScript: Specify a JavaScript file with the same filename in the sub-theme's .info file. For instance, to override script.js inherited from a parent theme, add the following line to your sub-theme's .info file:

scripts[] = script.js

You will also need to create the script.js file; if you simply wish to disable the imported scripts, you can create an empty file.
