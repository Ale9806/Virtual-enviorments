# Virtual enviorments a quick guide:

Python applications will often use packages and modules that don’t come as part of the standard library. Applications will sometimes need a specific version of a library, because the application may require that a particular bug has been fixed or the application may be written using an obsolete version of the library’s interface.

### Creating Virtual Environments:
``` python
python -m venv [path to enviorment]/[name-of-enviorment]
````
### Aactivate Enviroment:

Windows:
``` python
tutorial-env\Scripts\activate.bat
````
Linux:
``` python
source tutorial-env/bin/activate
```

###  Managing Packages with pip
You can install, upgrade, and remove packages using a program called pip. By default pip will install packages from the Python Package Index,
