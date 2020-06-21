# Building an App

+ Install the latest version of Python.
+ Install latest Cloud SDK version.
+ Create a Google project.
+ Structure your web service files/ Upload links and files needed.
+ Testing your web service.

## 1. Install the latest version of Python.
This can be done by going to the [python](https://www.python.org/downloads/) website. Make sure you select Add my path before installing the python program.

If you have python already installed, there are a couple of ways to check.
Use the following command to start the latest python version you have in your environment.
```
py     
```
Use this command to start the latest python 3 you have installed
```
py -3
```
Use this command to verify the version of python you have
```
pip --version  
```

## 2. Install latest Cloud SDK version to run
Open PowerShell and run the following commands.

```
(New-Object Net.WebClient).DownloadFile("https://dl.google.com/dl/cloudsdk/channels/rapid/GoogleCloudSDKInstaller.exe", "$env:Temp\GoogleCloudSDKInstaller.exe")

& $env:Temp\GoogleCloudSDKInstaller.exe
```
Once the download is finished, start Cloud shell.
Run ```gcloud init ``` to log in.

## 3. Create a Cloud Project
Use the following command in the Cloud Shell to create a Cloud Project.
```
gcloud projects create PICK_A_NAME
```
Run the following command to enable App Engine and create the associated application resources
```
gcloud app create
```
Enable billing for your project. Running only the sample app in this topic does not exceed the free quotas.

## 4. Structure your web service files
Clone the project into your directory
```
git clone https://github.com/GoogleCloudPlatform/python-docs-samples
```

Change your directory to open the folder where the application lies
```
cd python-docs-samples/appengine/standard_python37/building-an-app/building-an-app-1
```

## 5. Testing your web service.

Create a python environment by inputting the following command line PowerShell
```
python -m venv env
env\Scripts\activate
```

If you receive an error trying to create the python environment. Use this command.
```
Set-ExecutionPolicy Unrestricted -Scope Process
```

Move to the App folder and install the requirements for the app.
```
cd YOUR_PROJECT or  cd python-docs-samples/appengine/standard_python37/building-an-app/building-an-app-1      
pip install -r requirements.txt
```

Run the app by using the following command.
```
python main.py
```

In your web browser enter the following command.
```
http://localhost:8080
```
