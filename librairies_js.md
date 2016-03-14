# Librairies (JavaScript)
Libraries are JavaScript libraries only located in the `/libraries/` directory of wityCMS.

## Add a library
1. Create a folder with the name of the library (such as /libraries/testlib/)
2. Declare it in the libraries.json file, within the path key without the .js extension:
```json
"testlib": "testlib/testlib",
```

## Use a library in a template
wityCMS uses `requireJS` to manage JS libraries.

To load a library, it must be declared in the view.php of an application:
```php
$this->assign('require', 'testlib/testlib');
```