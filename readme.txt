Name: Gaurav Garwa
Reg. No.: 20BCE10530

Procedure to run the application:

Step 1: Open the folder in any ide and set up python virtual environment
        run in terminal- python3 -m venv venv
        then, activate venv: mac/linux: . venv/bin/activate
                        windows: venv\Scripts\activate

Step 2: Install Flask, hashids, sqlite3 if not installed previously.

Step 3: Run the following commands in terminal:
        export FLASK_APP=app.py
        export FLASK_ENV=development
        flask run

This will create a localhost link like: http://127.0.0.1:5000/, click on the link and the application will be opened in the
web browser.


