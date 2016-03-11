# Architecture and Workflow
The next slide describes the workflow of the v0.5:

![](wityCMS-workflow.jpg)

All wityCMS kernel is located in the files system/WCore.

The rendering mechanism when a URL is called is quite simple:
1. The WMain class will handle the whole workflow;
2. The WRetriever class will have the responsability to deal with applications (composed with a Controller, a Model and a View);
3. The application output is given to WResponse which will send it to the browser in HTML or JSON format.

## WTemplate
WTemplate is the templating engine of wityCMS.
Its files are located in system/WTemplate.

## WSystem
WSystem is a factory that contains instance of some core classes :
- WTemplate: templating engine
- WDatabase: extension of PHP PDO clas to interact with the MySQL database
- WSession: class that manages the user session

## Tools
wityCMS offers some class tools in its kernel:
- WRequest: a class to deal with user input ($_POST, $_GET, $_REQUEST variables)
- WConfig: a class to get and store configuration (route, database, config)
- WRoute: a class to manage the URL
- WLang: a class to manage i18n (internationalization)
- WNote: a class to display notes to the user (info, success, danger)
- WDate: extension to PHP DateTime to handle dates coming from the database
- WTools: some useful functions
- WExport: a class to export data into CSV