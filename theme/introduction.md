# Overview

All wityCMS themes are contained in the folder **themes**.

![](images/02-witycms-folders-theme.png)

The current theme is defined in the main configuration file : `system/config/config.php`. Just replace "*grafx*" by your theme name. 

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

Theming in wityCMS is easy. All you need is some basic knowledge of **`HTML`**, **`CSS`**, and **`PHP`**.