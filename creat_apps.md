# Applications
wityCMS works with applications (or app) that are all stored in the /apps/ folder.

Each application is composed with two sides:
- a front (located in /apps/sample-app/front/)
- an admin (located in /apps/sample-app/admin/) for the management of business objects in the administration panel

Each of the admin and the front can contain different kind of files:
- main.php: this file contains the app Controller
- model.php: this file contains the model and interaction with the database
- view.php: this file prepares the template files to be rendered by assigning variables into them

## Manifest
The manifest is a XML file that describes the whole application and the actions accessible in the app (the URLs) both for the admin and for the front.

Here is a sample file for the news application:
```xml
<?php defined('WITYCMS_VERSION') or die('Access denied'); ?>
<?xml version="1.0" encoding="utf-8" ?>
<app>
	<!-- Application name -->
	<name>News</name>

	<version>0.5.0-11-02-2016</version>

	<!-- Last update date -->
	<date>02-05-2015</date>

	<!-- Permissions -->
	<permission name="writer" />
	<permission name="category_manager" />
	<permission name="moderator" />

	<!-- Front actions -->
	<action default="default">listing</action>
	<action>detail</action>
	<action>preview</action>

	<!-- Admin actions -->
	<admin>
		<action default="default" description="News">news</action>
		<action requires="writer" menu="false">news-add</action>
		<action requires="writer" menu="false">news-edit</action>
		<action requires="writer" menu="false">news-save-preview</action>
		<action requires="moderator" menu="false">news-delete</action>
		<action requires="category_manager" description="Categories">categories</action>
		<action requires="category_manager, moderator" menu="false">category-delete</action>
	</admin>
</app>
```

This XML contains several information about the application:
- Name
- Version
- Date of modification
- Permissions (to be use for access rights management)
- Action: front actions that can be triggered from the URL (/sample-app/action). The front actions are located directly in the root tag <app> of the XML.
- Admin actions: it is the same purpose as front actions but for the administration panel. They are store in the <admin> tag to be distinguished from front actions.

## Controller
The Controller stored in the main.php file is the most important file of an application. Without this file, and the class it contains, wityCMS will not be able to use the application.

This file must contain a class with a specific name: "NameOfYourApp" (in camL case if the application names contains spaces) + "Controller". In our case: *SampleAppController* is the name of our controller class.

For instance:
```php
/**
 * SampleApp Application - Front Controller
 */

defined('WITYCMS_VERSION') or die('Access denied');

/**
 * SampleAppController is the Front Controller of the SampleApp Application
 *
 * @package Apps\SampleApp\Front
 * @version 1.0.0
 */
class SampleAppController extends WController {
    protected function action(array $params) {
        $data = array();
        
        // Calculate data from model here for instance
        
        return array(
            'data' => 'test'
        );
    }
}

?>
```

Each controller has a reference to its model in $this->model and to his view in $this->view.

**Admin Controller**
For the admin case, it is similar to the front controller, but the extension in the class name is AdminController instead of Controller: *SampleAppAdminController*.

## Model
The model.php file is not mandatory but very usefull if the application needs to interact with the database.

Here is the minimal implemention of a front model:
```php
<?php
/**
 * SampleApp Application - Front Model
 */

defined('WITYCMS_VERSION') or die('Access denied');

/**
 * SampleAppModel is the Front Model of the SampleApp Application
 *
 * @package Apps\SampleApp\Front
 * @version 1.0.0
 */
class SampleAppModel {
    /**
	 * @var WDatabase instance
	 */
	protected $db;

	public function __construct() {
		$this->db = WSystem::getDB();

		// Declare table
		$this->db->declareTable('sample_app_table');
	}
}

?>
```

Very important: if you want to use a table of the database in the model, you must declare the table in the constructor (`$this->db->declareTable('sample_app_table');`) so wityCMS knows where to add the prefix before the table name.

**Admin Model**
For the admin case, just add AdminModel for the prefix: *SampleAppAdminModel*.

## View
The view.php file is not mandatory. It contains a class that will be the interface between the PHP and the HTML template.

Minimal implementation:
```php
<?php
/**
 * SampleApp Application - Front View
 */

defined('WITYCMS_VERSION') or die('Access denied');

/**
 * SampleAppView is the Front View of the News Application
 *
 * @package Apps\SampleApp\Front
 * @version 1.0.0
 */
class SampleAppView extends WView {
	public function action($model) {
		$this->assign('data', $model['data']);
	}
}

?>
```

**Admin View**
For the admin case, just add AdminView for the prefix: *SampleAppAdminView*.

## Templates
The application may contain HTML templates, all located in the /templates/ subdirectory of the front or admin folders of the app.

The templates files must be named according to the action being executed (in our case: action.html).

```html
<div class="wity-app wity-app-sample-app wity-action-action">
    {$data}
</div>
```

Templates use the WTemplate syntax to deal with variables, loops, conditions, etc.

## Language
The application may need to be translated in several languages configured in the administration of wityCMS.

To translation of application is done based on XML files located in the /lang/ subdirectory of the front or admin folder of the app. The XML must be named according to the ISO name of the lang, such as fr.xml.

```xml
<?xml version="1.0" encoding="utf-8" ?>
<lang value="fr">
	<item id="Sentance in English.">Phrase en français.</item>
</lang>

```

We advise to use plain English in your app by default, so you won't need to do an en.xml file. And all the keys in fr.xml will be plain english to translate in French. This will be very simple for translators to do the job.