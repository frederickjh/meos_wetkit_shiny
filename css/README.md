The subtheme-creator script creates css/local.css and adds the needed line to your .info file for you.

Style sheet inheritance
All style sheets defined in the parent theme will be inherited, as long as you declare at least one stylesheet in your sub-theme's .info file. You must declare at least one stylesheet in your sub-theme for any of the parent theme's stylesheets to be inherited. 

Overriding inherited style sheets: Specify a style sheet with the same filename in the sub-theme. For instance, to override style.css inherited from a parent theme, add the following line to your sub-theme's .info file:

stylesheets[all][]   = style.css

You will also need to create the style.css stylesheet file; if you simply wish to disable the imported styles, you can create an empty file.
