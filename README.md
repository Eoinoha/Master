# READ ME 

Read Me for Dynamic Dublin Bikes by The Awake, The Asleep, and the Groggy.

Please read this file before exploring or using this repository. 
This Read Me give details about the environment needed to run the flask app and the files, as well as where files can be found in the repo.
It also contains information about files that are needed, and where to place them on your machine, what they should contain, and why they are not stored here.


Environment:
------------------------
The following are the specifications for the Virtual Environment.

Environment Name = SEP
Python Version 3.8.5

List of pip installs required:
    sqlalchemy
    jupyter
    mysql-connector
    requests
    pandas
    flask
    jninja2
    functools
    datetime
    unittest
    pickle
    sklearn
    
    
Untracked:
------------------------
The repository uses .gitignore to track files that should not be shared. Most of these are caching files that are automatically generated when the flask app is running. Of note though is the file APID.py.

The file APID.py is expected both in the root of the repository and in the folder flaskapp. It is untracked for security reasons. This file is expected to contain access details for the database, as well as personal API keys and details for both JCDecaux and AccuWeather. These details are expected under the following variables:

Database:
  engine = database connection details

JCDecaux:
  APIKEY = Your API key to JCDecaux
  NAME = The city name
  STATIONS = Url to the api
  
AccuWeather:
  ACCUAPIKEY =  Your API key to JCDecaux
  ACCULOCATIONKEY = Location code
  RESOURCEURL = Url to the api
  

Layout:
------------------------
Flask App:

  The flask app, and related files, can be found in the folder flaskapp and its children. Inside you will fide the app itself, app.py, as well as test_app.py and finalized_model.sav. The latter file you will find a copy of in the root directory also to prevent issues with where the app recognises as the root directory when it is run. test_app.py contains the unittests for the flask app.
  In the templates you will find the html files for all the site pages. The static folder contains the CSS javascript files for the app. It also contains all the gif and image files, most of them contained in the child folders stationsListIcons and weatherIcons although two are storred in the static folder inself.


API Scrapers:

The JCDecaux and both AccuWeather API scrapers can be found as .py files in the root of the repository. The stations table in the database only needed to be generated once, which was created as a seperate scraper to the current availability scraper, can be found in the folder bikeStationsScraper. The notebook used to create both bike scraper can also be found in the .ipynb_checkpointsfolder, although they where seperated into two python files for execution. 
  

.gitignore:
  This contains the location of files and folders not to be tracked by git. These are not tracked either as they are cache files that are automatically generated by the flask app whe it runs, or for security. 
  
  
  
Best of luck.
