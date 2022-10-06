Procedure to run the application:

Step 1: Open the folder in any ide and set up python virtual environment
        run in terminal- python3 -m venv venv
        then, activate venv: mac/linux: . venv/bin/activate
                        windows: venv\Scripts\activate

Step 2: Install Flask, hashids, sqlite3 if not installed previously.

Step 3: Run the following commands in terminal:
        export FLASK_APP=app
        export FLASK_ENV=development
        flask run

This will create a localhost link like: http://127.0.0.1:5000/, click on the link and the application will be opened in the
web browser.


Explanation:

First we need to set up the dependencies-
Create a python virtual environment, then install flask, hashids, sqlite, etc.

Then we create our flask app , inside which we create a hash id, Hashids is a library that generates a short unique ID from integers.
Here I have used Hashids to generate unique strings for URL 


A salt is a random string that is provided to the hashing function (that is, hashids.encode()) so that the resulting hash is shuffled based on the salt. This process ensures the hash you get is specific to your salt so that the hash is unique and unpredictable


Then we have a index route in which we get the url entered by the user and make it short 
Then we insert the link into database 


We then construct the short URL using request.host_url, which is an attribute that Flask’s request object provides to access the URL of the application’s host. This will be http://127.0.0.1:5000/ in a development environment and our_domain


Redirect Route:
This new route accepts a value id through the URL and passes it to the url_redirect() view function. For example, visiting http://127.0.0.1:5000/KJ34 would pass the string 'KJ34' to the id parameter.


Statistics Route: 
 In this view function, you open a database connection. Then you fetch the ID, the creation date, the original URL, and the number of clicks for all of the entries in the urls table. You use the fetchall() method to get a list of all the rows.

