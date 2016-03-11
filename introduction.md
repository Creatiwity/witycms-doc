# Overview

wityCMS uses its own templating system, named [WTemplate](https://github.com/Creatiwity/WTemplate), developed as [a separate GitHub project](https://github.com/Creatiwity/WTemplate) but included here as a submodule.

Theming in wityCMS is easy; all you need is some basic knowledge of HTML, CSS, and PHP. With our functions, it’s easy making a theme.

## Theme definition

All wityCMS theme are contents in a same folder "**themes**". When you want to create a new theme it is important to create a new folder in the name of your "theme name" (e.g: "grafx"), in the right path .../themes.

![](02-witycms-folders-theme.png)

You also need to edit the file who defines the main configuration values for wityCMS: "config.default.php". Replace "grafx" by your theme name. This file is located in .../system/config/default. 

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