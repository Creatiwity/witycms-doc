# Overview

All wityCMS themes are contained in the folder **themes**.

![](02-witycms-folders-theme.png)

The current defines the main configuration values for wityCMS: "config.default.php". Replace "grafx" by your theme name. This file is located in .../system/config/default. 

```php
$config = array(
  'base'             => 'https://www.mysite.com',
  'name'             => 'wityCMS',
  'page_title'       => 'wityCMS',
  'page_description' => '',
  'theme'            => 'grafx',
  'timezone'         => 'Europe/Paris',
  'email'            => 'contact@mysite.com',
  'debug'            => true
);
?>
```

wityCMS uses its own templating system, named [WTemplate](https://github.com/Creatiwity/WTemplate), developed as [a separate GitHub project](https://github.com/Creatiwity/WTemplate) but included here as a submodule.

Theming in wityCMS is easy; all you need is some basic knowledge of HTML, CSS, and PHP. With our functions, it’s easy making a theme.