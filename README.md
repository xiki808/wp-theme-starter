# wp-theme-starter

A WordPress theme starter to use as a starting template to build a custom theme. The template encourages the use of namespaces as specified by [PSR-4](https://www.php-fig.org/psr/psr-4/)

![Template](https://media.giphy.com/media/26ufhYjBs6C4Q5SJG/giphy.gif?style=centerme)

## Getting Started

The template uses a namespace prefix `WTS\`, this can be changed to any other prefix you would like for your theme, hence it needs to be replaced and used in every class file.

1. Replace the prefix `WTS\` in `functions.php` with your custom one.
2. Replace the prefix in file `Includes/Init.php`.

A sub namespace can be used simply by adding a folder in the `Includes` folders, and add the path to the containing classes' namespace.

If a new namespace is needed, create the folder and add the namespace in `functions.php` before the `$loader->register();` call.

```
$loader->addNamespace('{MYPREFIX}\{MYNAMESPACE}', __DIR__.'/Path/To/Folder');

// Before the register call
$loader->register();
```

### Credits

- [PSR-4: Autoloader](https://www.php-fig.org/psr/psr-4/)
