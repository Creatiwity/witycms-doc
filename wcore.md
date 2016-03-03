# WCore 

## Files structure

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

### WRoute
WRoute calculates the route given in the URL to find out the right application to execute.

### WSession.php
WSession manages all session variables and anti flood system.

### WSystem.php
Wsystem keeps the session, template and databse instances as singletons.

### WTools.php
WTools contains some tiny helpful functions.

### WView.php
WView handles application's Views.



