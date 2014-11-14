Template.php function inheritance

Anything defined in the parent theme's template.php file will be inherited. This includes theme function overrides, preprocess functions and anything else in that file. Each sub-theme should also have its own template.php file, where you can add additional functions or override functions from the parent theme.

There are two main types of functions in template.php: theme function overrides and preprocess functions. The template system handles these two types in very different ways.

Theme functions are called through theme('[hook]', , ...). When a sub-theme overrides a theme function, no other version of that theme function is called.

On the other hand, preprocess functions are called before processing a .tpl file. For instance, [theme]_preprocess_page is called before page.tpl.php is rendered. Unlike theme functions, preprocess functions are not overridden in a sub-theme. Instead, the parent theme preprocess function will be called first, and the sub-theme preprocess function will be called next.

There is no way to prevent all functions in the parent theme from being inherited. As stated above, it is possible to override parent theme functions. However, the only way to remove a parent theme's preprocess function is through hook_theme_registry_alter().

Page, node, block and other template (.tpl.php) file inheritance

Drupal provides a large set of files that themes can use to inherit properties. By specifying a particular file name and or structure, this allows the theme to override or inherit a template. For more information on this review working with template suggestions

Drupal 7 Any .tpl.php files from the parent theme will be inherited. You can add template files with more specificity — for instance, node--blog.tpl.php building on an inherited node.tpl.php.

A single hyphen is still used to separate words: for example, "user-picture.tpl.php" or "node--long-content-type-name.tpl.php", so the double hyphen always indicates a more targeted override of what comes before the "--". See Converting 6.x themes to 7.x for more info.

Overriding inherited .tpl.php templates: Add a template file with the same name in your sub-theme folder to have it override the template from the parent theme.
