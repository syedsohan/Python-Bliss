# Python Bliss

A brief description of installing **Python Packages** Using **Pip and Virtual Environments** for **WINDOWS**.

## Installing pip

`pip` is the reference [Python](https://www.python.org/downloads/) package manager. It’s used to install and update packages. You’ll need to make sure you have the latest version of `pip` installed.

The Python installers for `Windows` include pip. You can make sure that pip is up-to-date by running:

```bash
  py -m pip install --upgrade pip
  py -m pip --version
```

Afterwards, you should have the latest version of pip:

```bash
  pip 23.3 from c:\python39\lib\site-packages 
  (Python 3.12)
```

## Creating a virtual environment

'venv' (for 'Python 3') and 'virtualenv' (for 'Python 2') allow you to manage distinct package installations for various projects. They essentially allow you to construct a "virtual" isolated Python installation and install packages into that virtual installation. When switching projects, you may simply establish a new virtual environment and not worry about breaking the packages installed in the previous environments. **It is usually suggested to use a virtual environment when building Python applications**.

To create a virtual environment, go to your project’s directory and run venv. If you are using Python 2, replace `venv` with `virtualenv` in the below commands.

```bash
  py -m venv env_name
```

The second argument is the location to create the virtual environment.

`venv` will create a virtual Python installation in the `env_name` folder.

## Activating a virtual environment

Before you can start installing or using packages in your virtual environment you’ll need to `activate` it. Activating a virtual environment will put the virtual environment-specific `python` and `pip` executables into your shell’s `PATH`.

```bash
  .\envAuto\Scripts\activate
```

You can confirm you’re in the virtual environment by checking the location of your Python interpreter:

```bash
  where python
```

It should be in the `env_name` directory:

```bash
  ...\env\Scripts\python.exe
```

As long as your virtual environment is `activated` **pip will install packages** into that specific environment and you’ll be able to import and use packages in your Python application.

## Installing Packages

To install a package, use the following command:

```bash
  pip install package_name
```

##  Installing Specific Versions

Specify the version using the following syntax:

```bash
  pip install package_name==version_number
```

## Upgrading Packages

Keep packages up-to-date with:

```bash
  pip install --upgrade package_name
```

## Uninstalling Packages

Remove a package with:

```bash
  pip uninstall package_name
```

## Displaying Installed Packages

Easily view the installed packages within your environment by using the following command:

```bash
  pip list
```

This command provides a clear and concise list of all installed Python packages, along with their respective versions, giving you a quick overview of the components within your development environment.

## Freezing Requirements

Capture the exact versions of installed packages for reproducibility:

```bash
  pip freeze > requirements.txt
```

## Installing Requirements from a File

To replicate the environment, use:

```bash
  py -m pip install -r requirements.txt
```

## Deactivating the Virtual Environment

Simply use:

```bash
  deactivate
```

## Note

You should exclude your virtual environment directory from your version control system using `.gitignore`.
