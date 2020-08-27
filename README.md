# Virtual enviorments a quick guide:

Python applications will often use packages and modules that don’t come as part of the standard library. Applications will sometimes need a specific version of a library, because the application may require that a particular bug has been fixed or the application may be written using an obsolete version of the library’s interface.

## Creating Virtual Environments:
``` python
python -m venv [path to enviorment]/[name-of-enviorment]
````
## Aactivate Enviroment:

Windows:
``` python
[name-of-enviorment]\Scripts\activate.bat
````
Linux:
``` python
source [name-of-enviorment]/bin/activate
```

##  Managing Packages with pip
You can install, upgrade, and remove packages using a program called pip. By default pip will install packages from the Python Package Index.

**Installing Modules**

You can install the latest version of a package by specifying a package’s name
``` python
(env) $ pip install [name-of-package]
``` 

You can also install a specific version of a package by giving the package name followed by == and the version number
``` python
(env) $ pip install [name-of-package] == 2.6.0
``` 

**Updating Modules**

If you re-run this command, pip will notice that the requested version is already installed and do nothing. You can supply a different version number to get that version, or you can run pip install --upgrade to upgrade the package to the latest version

``` python
(env) $ pip install -- upgrade [name-of-package] 
``` 
**Unistalling  Modules**

pip uninstall followed by one or more package names will remove the packages from the virtual environment.

``` python
(env) $ pip uninstall [name-of-package] 
``` 
