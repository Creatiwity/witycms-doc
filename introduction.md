# Introduction

wityCMS uses its own templating system, named [WTemplate](https://github.com/Creatiwity/WTemplate), developed as [a separate GitHub project](https://github.com/Creatiwity/WTemplate) but included here as a submodule.

Theming in wityCMS is easy; all you need is some basic knowledge of HTML, CSS, and PHP. With our functions, it’s easy making a theme.

## Theme

1. First you need to define a name for your theme.
2. Go to: .../system/config/default/config.default.php to edit the theme name (This file defines the main configuration values for wityCMS).

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



## Nom du theme = nom du dossier

The best point of reference is usually the default theme bundled with your wityCMS installation, since it’s always kept up to date, and it’s a fairly minimal theme. Just duplicate the folder, remove the CSS, and adjust markup as needed.

Alternatively, you can check out some themes made by the community, or create your own from scratch. It‘s up to you.

![](02-witycms-folders-theme.png)