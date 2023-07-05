# Selenium New Project Guide

## Background:
When I first started learning Selenium, I faced similar challenges. Existing beginner guides often left gaps in their explanations, assuming prior knowledge or skipping steps. This motivated me to create a guide that fills those gaps and provides a comprehensive learning guide.

## Operating System: macOS
## Web Browser: Google Chrome
<br/>

## Getting Started

### IN TERMINAL:
1. Make a directory for your project: 
```mkdir <your_app_name>```

2. ```cd <your_app_name>```

3. Open VSCode in current directory: 
```code .```

### IN VSCode TERMINAL:
1. Install Virtual Environment: 
 ```python3 -m venv <your_env_name>```

2. Activate the virtual environment: 
```source <your_env_name>/bin/activate```

3. Select Interpreter on VSCode:
- Press ```Cmd+Shift+P``` to open the Command Palette.
- In the Command Palette, type ```Python: Select Interpreter``` and select the corresponding option that appears.
- A list of available Python interpreters will be displayed. Choose the interpreter that you installed in the previous step. It should look something like this: ```Python 3.9.6('<your_env_name>': venv)```

4. Install the Selenium package:
```pip install selenium```
<br/><br/>

### WEB DRIVER:
#### Download ChromeDriver
1. On your Google Chrome:
go to ```https://sites.google.com/chromium.org/driver/downloads/version-selection?authuser=0```
2. Find out which version of ChromeDriver to download: 
- On the top right corner of your Google Chrome, 
go to ```kebab menu (vertical three-dot menu)``` → ```help``` → ```About Google Chrome``` → look for something like ```Version 114.0.5735.198 (Official Build) (arm64)```
- Take the Chrome version number, remove the last part, and append the result to URL "https://chromedriver.storage.googleapis.com/LATEST_RELEASE_". For example, with Chrome version 72.0.3626.81, you'd get a URL "https://chromedriver.storage.googleapis.com/LATEST_RELEASE_72.0.3626". 
- You will get soomething like ```72.0.3626.69```
- Append the result from previous step to URL:
https://chromedriver.storage.googleapis.com/index.html?path=```72.0.3626.69```
- Download the corresponding ChromeDriver 

#### Set Up ChromeDriver
1. Locate your downloaded ChromeDriver
2. Unzip & Open the folder
3. Inside the folder, there are two files: ```LICENSE``` & ```chromedriver```
4. You only need ```chromedriver```, figure out where to put it. I put it inside my project folder, other ppl put it elsewhere. Just make sure you know the path to the file because you will need it later.
5. Make sure the web driver executable has the appropriate permissions to be executed
```chmod +x /path/to/chromedriver```
<br/><br/>

### WEBDRIVER-MANAGER - simplifies the management of WebDriver binaries for Selenium:
- Install webdriver manager: 
 ```pip install webdriver-manager```
 <br/><br/><br/>

*OPTIONAL: I wanted a live-server, so I did this step*
### Live Server
1. Go to https://nodejs.org and download ```Node.js```
2. In VSCode terminal: ```sudo npm install -g nodemon\n```
3. Set up live server: 
- Activate: <br/>
```nodemon --exec python <your_py_file>\n```
- Quit: 
Press <br/>
```Ctrl + C``` in the terminal where nodemon is running
<br/><br/>

### Voila! This is what my starter code look like:
![Starter Example](https://github.com/KZKS01/catcollector/assets/109245976/4f4e075e-15a2-4980-8352-74f48e33ad79)
