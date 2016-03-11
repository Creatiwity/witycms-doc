# Helpers (PHP)
Helpers are PHP libraries located in the /helpers/ directory of wityCMS.

## Add a helper
1. Create a folder with the name of the library (such as /helpers/testlib/)
2. Within /helpers/testlib/, create a file helper.json with this content:
```json
{
	"file": "testlib.php", // Main file of the lib
	"class": "TestLib", // Main class of the lib
	"params": ["param1"] // Name of the parameters to be given to the constructor (array of strings in JSON)
}
```

## Use a helper in PHP
To load a helper in an application, there is a sample code:
```php
$testLibHelper = WHelper::load('TestLib', array('param1 value'));
```