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

**Installing Packages**

You can install the latest version of a package by specifying a package’s name
``` python
(env) $ pip install [name-of-package]
``` 

You can also install a specific version of a package by giving the package name followed by == and the version number
``` python
(env) $ pip install [name-of-package] == 2.6.0
``` 

**Updating Packages**

If you re-run this command, pip will notice that the requested version is already installed and do nothing. You can supply a different version number to get that version, or you can run pip install --upgrade to upgrade the package to the latest version

``` python
(env) $ pip install -- upgrade [name-of-package] 
``` 
**Unistalling  Packages**

pip uninstall followed by one or more package names will remove the packages from the virtual environment.

``` python
(env) $ pip uninstall [name-of-package] 
``` 

**Other usefull pip commands**

```pip list ``` will display all of the packages installed in the virtual environment

``` pip show [name-of-package] ``` will display information about a particular package

```pip freeze ``` will produce a similar list of the installed packages, but the output uses the format that pip install expects. A common convention is to put this list in a requirements.txt file:

 ```
(env) $ pip freeze > requirements.txt
```

The ```requirements.txt``` can then be committed to version control and shipped as part of an application. Users can then install all the necessary packages with install -r:

```
(env) $ pip install -r requirements.txt
```

Now your eviorment is read, if you want to upload your venv to Jupyer notebooks got to the folder that contains the enviorment and apply the following code:
``` python
python -m ipykernel install --user --name=[name-of-enviorment]
```

Of course this will only work if you have Jupyter Notebooks isntalled:
```
pip install notebook
````

As an extre step you will need ipykernel 

```
pip install --user ipykernel
```
<br>
<br>
<br>
<br>

**Biblography:**

[Python](https://docs.python.org/3/tutorial/venv.html)
<br>
[Parametric thoughts](https://janakiev.com/blog/jupyter-virtual-envs/)
