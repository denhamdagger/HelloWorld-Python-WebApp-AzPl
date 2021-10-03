https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops

python.exe
   The command "python.exe" refers to the Python executable of the default Python installation.
   Technically, the path of this version is stored inside the PATH environment variable where your OS will search for the executable when processing any command.
py.exe
   The command "py.exe" refers to the Python launcher, a utility that’s automatically installed into C:\Windows\ for any Python installation on Windows.
   All files in the Windows folder are accessible without needing to modify the PATH environment variable. 
   Thus, the Python launcher automatically delegates the work to the latest Python version installed in your environment. 
   However, you can also specify the used installation by means of a flag argument such as in py -3.6 to specify Python version 3.6.

#############################
Running from the Command Line
#############################

From Powershell

# Create Virtual Environemt called (Folder .env) 
# https://docs.python.org/3/library/venv.html
py -3 -m venv .env

# Setup env variables
.env\scripts\activate

# Ensure the Modules in "requirements.txt" are installed
pip install -r requirements.txt

# Set name of this app in FLASK_APP
$env:FLASK_APP = "hello_app.webapp"

# Launch website
python -m flask run

# Open a browser and navigate to http://localhost:5000 to view the app. 
# When you're finished, close the browser, and stop the Flask server with Ctrl+C
