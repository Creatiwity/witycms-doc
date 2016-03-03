# File Structure

wityCMS has a fairly loose file structure — you can have as many files and folders as you want in your theme, as long as a few required theme files are present.

## Required theme files
If you don’t have these files, your theme won’t work properly, or just won’t show up at all. It’s vital you have these files.

### about.txt
This text file holds the basic details about your theme. For example:

* Theme Name: Grafx
* Theme URI: https://creatiwity.net
* Description: Theme for wityCMS
* Author: Creatiwity
* Author URI: https://creatiwity.net
* Version: 1.1.0


### WConfig.php
Wconfig loads all configuration files, manages all configuration values.

### Wcontroller.php
WController is the base class that will be inherited by all the applications.

### WDatabase.php
WDatabase manages all database interaction.

### WDate.php
WDate manages date using the user's custom timezone.

### WExport.php
WExport helps to export data.

### WHelper.php
WHelpers automatically instantiates for you small libraries.

### WLang.php
WLang manages everything about languages.

### WMain.pho
Wmain is the main class that wity launches at start-up.

### WNote.php
WNote manages all notes : stores, displaus...

### WRequest.php
WRequest manages all input variables.

### WResponse.php
WResponse compiles the final render of wityCMS that will be sent to the browser.

### WRetriever.php
WRetriver is the component to get the model or the view of an action from any wityCMS's application.

###WRoute
WRoute calculates the route given in the URL to find out the right application to execute.

### WSession.php
WSession 
