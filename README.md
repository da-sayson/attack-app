# To activate the virtual environment, use the interpreter in the virtual environment:
$ pipenv shell

# To use the current directory to start a new project 
$ django-admin startproject <project_name> .

# The file project > manage.py is a wrapper around django-admin but is aware of project settings
To run:
$ python manage.py runserver

ignore "18 unapplied migrations" for now


# To use the virtual environment's interpreter inside VS Code:
Get the virtual environment's python interpreter:
$ pipenv --venv
$ <output>

Add the interpreter to VS Code
In VS Code, click: View > Command Palette
Type: "Python: Select Interpreter"
Enter the interpreter: <output>

# If the terminal has an error like "...cannot be loaded because running scripts is disabled on this system. ...":
In VS Code: press ctrl + shift + p
Type and select: "Preferences: Open User Settings (JSON)"
Add:
    ...,
    "terminal.integrated.profiles.windows": {
    "PowerShell": {
        "source": "PowerShell",
        "icon": "terminal-powershell",
        "args": ["-ExecutionPolicy", "Bypass"]
    }
    },
    "terminal.integrated.defaultProfile.windows": "PowerShell",

# To run the server in VS Code:
In VS Code: click Terminal > New Terminal
In Terminal: type python manage.py runserver
