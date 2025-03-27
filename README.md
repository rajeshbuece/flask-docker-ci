# flask-docker-ci

🚀 Detailed Explanation of Your Flask App
python
Copy
Edit
from flask import Flask
✅ This line imports the Flask module.
Flask is a lightweight Python web framework used to create web applications and APIs.

python
Copy
Edit
app = Flask(__name__)
✅ Here, you're creating a Flask application instance named app.
__name__ is a Python special variable that holds the name of the current module.

When you pass __name__, Flask will know:

Where to find templates and static files.

Whether the app is running standalone or being imported.

python
Copy
Edit
@app.route('/')
def home():
    return "Hello, CI/CD with Jenkins and Docker!"
✅ This is your first route.
The @app.route('/') is a decorator in Flask.

It means:

When someone accesses the URL / (Root URL like http://localhost:5000/), this function will be executed.

home() is the function that returns a plain text response:

csharp
Copy
Edit
Hello, CI/CD with Jenkins and Docker!
This is the output you will see when you open the app in your browser.

python
Copy
Edit
if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)
✅ This is the main entry point of your Python script.

__name__ == '__main__' ensures that the app runs only if this script is executed directly, not when imported as a module.

app.run() is used to start the Flask development server.

Options used:

Parameter	Purpose
host='0.0.0.0'	Exposes the Flask app on all network interfaces (So you can access from outside the server)
port=5000	Runs the app on port 5000
🌐 How it Works
When you run:

bash
Copy
Edit
python app.py
You will see output like:

csharp
Copy
Edit
 * Running on http://0.0.0.0:5000/
If you open your browser and visit:

cpp
Copy
Edit
http://<your-server-ip>:5000/
You will see:

csharp
Copy
Edit
Hello, CI/CD with Jenkins and Docker!


