# Item catalog application

This project is an application that provides a list of items within a variety of categories as well as provide a user registration and authentication system. Registered users will have the ability to post, edit and delete their own items.

## Getting Started

In order to run the code go to ./catalog directory under VM /vagrant shared folder.

### Prerequisites

The script need the Database "categoryApp.db".
You can use the file provided in the catalog directory with some categories and items already in it or create a new Database.
In order to do create a new Database use the script "database_setup.py" in this way:
```
 python database_setup.py
```

After that download from https://console.developers.google.com/ and https://developers.facebook.com/ the json files with the OAuth2 personal information. The json files must have these names:
- For Google authentication = "client_secrets.json"
- For Facebook authentication = "fb_client_secrets.json"

Lastly, update the "login.html" file, inside the "template" directory by replacing the string YOUR_CLIENT_ID_GOES_HERE with your personal Google and Facebook keys.

## Running the program

For start the script, inside the catalog directory, use the command:
```
python project.py
```
The application run on URI: http://localhost:8000.

For JSON endpoints go to http://localhost:8000/JSON for the list of available categories and go to http://localhost:8000/<int:category_ID>/JSON for the items inside a specific category.