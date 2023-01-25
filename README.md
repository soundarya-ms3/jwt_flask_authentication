# jwt_flask_authentication

## What are JSON Web Tokens?

JSON Web Tokens (JWT) is a secure and compact way to transmit data between two parties with the help of JSON objects.

JSON web token consists of three parts-

+ Payload
+ Header
+ Signature

## Steps to Implement Flask JWT Authentication

### Install packages


1. Create a requirements.txt file and listing all the packages into it. You can also declare the versions of the packages wherever necessary. 

      ```
      flask==1.1.2
      pyjwt==2.0.0
      datetime
      uuid
      Flask-SQLAlchemy

      ```
      + Now, use this file to install all the listed packages with pip.

        ``` pip install -r requirements.txt ```


2. Create a new file named “app.py” in the jwt(project folder name) directory.

      + Now, paste the following code inside the python file named app.py:
      
      
        ```
        from flask import Flask, request, jsonify, make_response, request, render_template, session, flash
        import jwt
        from datetime import datetime, timedelta
        from functools import wraps

        ```

      + Now configure settings inside the app.py file using the below code.
      

        ```
        app = Flask(__name__)
        app.config['SECRET_KEY'] = 'd21c28a1039c47a396f13aae6cfd1a56'

        ```

        Here, the value assigned to the config variable ‘SECRET KEY’ can be auto-generated using a python libraries. We can simply run the following code         in           your terminal to generate this value, as shown below.

         <img src="https://user-images.githubusercontent.com/70798723/214523611-933e3f45-2171-4572-8b76-c2af65aef7f7.png" width="580" height="300">
         
  ### Start App
  Now run the app.py file by using the following command inside the vs code in the appropriate directory.
  
  ``` python app.py ```
  
  + Server running on http://127.0.0.1:5000/
  + By visiting the app in the browser localhost:5000 we should see the login page!.

## Demo link
https://drive.google.com/file/d/1is2NmoTRtAhWig6rkwkB37ZB9u5ZRcg4/view?usp=share_link
