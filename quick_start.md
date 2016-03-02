# Quick start

Once you have installed wityCMS you can change some of the default settings that came with wityCMS. To do this, you will need to edit some configuration files.

## How to find settings files

All configuration files are stored in the wityCMS / settings file, but if you need to change specific parts of wityCMS, continue reading for some common examples.

## URL 

By default, the installer will try to detect if you have Apache and mod_rewrite enabled and create the .htaccess file for you. However, in some cases (mainly due to server limitations) wityCMS is unable to do for you, and you'll need to do it yourself. In this case please refer to note ... describe if necessary.

## Language

WityCMS supports Multilanguage mode, meaning that you can use wityCMS in several languages and edit content in multiple languages also. To change the language, change the variable during the installation of wityCMS to set the default language. You can add as many languages as you want for your content.

However, for translations of the system, there are two translations available, you can see all the translations on the GitHub page of wityCMS, but here's a short list of available languages:

* **English (en_GB)**
* **French (en_US)**

If you want to add a new translation, thank you submit a translation request; make sure the folder name for the new translation follows ISO 639 / ISO 3166 (http://www.localeplanet.com/icu/).
