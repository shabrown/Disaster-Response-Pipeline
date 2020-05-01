# Disaster Response Pipeline 

### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)
6. [Instructions](#instructions)

## Installation <a name="installation"></a>

sikit-learn   
nltk    
Flask   
numpy   
pandas   
sqlalchemy   


## Project Motivation<a name="motivation"></a>

In this project we will be analyzing disaster data from [Figure Eight](https://appen.com/) to build a model for an API that classifies disaster messages.

In the Workspace folder, there is a data set containing real messages that were sent during disaster events. A data processing pipeline and a machine learning pipeline will be created to clean the data and then to categorize these events so that we can send the messages to an appropriate disaster relief agency.

A web app is included where an emergency worker can input a new message and get classification results in several categories. The web app will also display visualizations of the data. 

## File Descriptions <a name="files"></a>

Inside the workspace folder, there are three main foleders:

1. data
    - disaster_categories.csv: dataset including all the categories 
    - disaster_messages.csv: dataset including all the messages
    - process_data.py: ETL pipeline scripts to read, clean, and save data into a database
    - DisasterResponse.db: output of the ETL pipeline, i.e. SQLite database containing messages and categories data
    
2. models
    - train_classifier.py: machine learning pipeline scripts to train and export a classifier
    - classifier.pkl: output of the machine learning pipeline, i.e. a trained classifer
    
3. app
    - run.py: Flask file to run the web application
    - templates contains html file for the web applicatin

## Results<a name="results"></a>

1. An ETL pipeline (process_data.py) was built to:
    *Read data from two csv files*
    *Clean data*
    *Save data into a SQLite database.*
    
2. A machine learning pipepline (train_classifier.py) was developed to train a classifier to performs multi-output classification on the 36 categories in the dataset.

3. A Flask app was created to show data visualization and classify the message that user enters on the web page.

An example of how the app classify the message.
Original message "Please, we need tents and water. We are in Silo, Thank you!"


<img src="app message screeshot.png" width="80%" alt="disaster response project web app">



## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Credits must be given to Udacity for the starter codes and FigureEight for provding the data used by this project. 

## Instructions:<a name="instructions"></a>

1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`   

2. Run the following command in the app's directory to run your web app.   
    `python run.py`

3. Go to http://0.0.0.0:3001/   
