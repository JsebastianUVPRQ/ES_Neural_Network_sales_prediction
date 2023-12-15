# ES_Neural_Network_sales_prediction_Deploy_API_ML

## Description

This project aims to deploy a machine learning model designed to forecast future sales using neural networks, specifically neural networks with embeddings. Time series forecasting is a critical task in inventory management and resource planning, and this project seeks to provide an accurate and efficient solution.

An embedding involves converting a discrete, often categorical, variable into a vector of continuous numbers. In the realm of neural networks, embeddings refer to low-dimensional, learned vectors that represent discrete variables in a continuous space. The significance of neural network embeddings lies in their ability to decrease the dimensionality of categorical variables and effectively capture the essence of categories in the transformed space.
There are three main objectives for neural network embeddings:

- Identifying nearest neighbors within the embedding space, which can be utilized for generating recommendations based on user interests or clustering categories.
- Serving as input to a machine learning model for a supervised task.
- Facilitating visualization of concepts and relationships between categories.

To serve the model, we will use Flask, a Python microframework for building web applications. Flask is easy to get started and a great way to build web sites and web applications. It is powered by a Python library called WSGI (Web Server Gateway Interface). WSGI provides a specification that describes how a web server communicates with web applications, and how web applications can be chained together to process one request. The API will be hosted on a personal server. The API will be able to receive a POST request with the data to be predicted and return a JSON with the prediction.

System Requirements
Flask
Install Anaconda on the server or on our local machine for development. (For servers, you can also use the mini-conda version.)
Test running the "conda" command in the terminal to verify that everything is in order.
Create a new environment where we will work: conda create --name my_environment python=3.6
Activate the created environment with: source activate my_environment
Install the required Python packages: pip install flask gunicorn
Steps to create the API with Flask:
Below is the code with which we will create the API and incorporate our model. It consists of the following files:

utils.py – Contains functions and common utilities used in various places within the project.

server.py – Imports the Flask class from the Flask library.

Defines routes and associated functions.
Creates an instance of the Flask application.
Starts the server.
Specifies the host and port on which the application will run.
api_train_model.py – Training and creation of the model, a neural network with embeddings.

test_api.py – Example of a POST request to test the API. An initial method is created that will be invoked from the "predict" URL.

Loads the previously trained model.
Responds to requests in JSON format.
time_series.csv – Dataset.

```bash
git clone <https://github.com/JsebastianUVPRQ/ES_Neural_Network_sales_prediction>

cd embeddings_deploy

python app.py
The API will be available at http://localhost:5000 by default.
```
