# flaskWebForms

To Run it Locally 
- Create Virtual Environment 
- Venv will be activated
```
- virtualenv venv
- source venv/bin/activate
- pip install flask
- pip freeze > requirements.txt
- pip install -r requirements.txt
- export FLASK_APP=run
- export FLASK_ENV=development
- flask run
```

SQLite runs in memory, and backs up its data store in files on disk. While this strategy works well for development, Heroku’s Cedar stack has an ephemeral filesystem. You can write to it, and you can read from it, but the contents will be cleared periodically. If you were to use SQLite on Heroku, you would lose your entire database at least once every 24 hours.

Even if Heroku’s disks were persistent running SQLite would still not be a good fit. Since SQLite does not run as a service, each dyno would run a separate running copy. Each of these copies need their own disk backed store. This would mean that each dyno powering your app would have a different set of data since the disks are not synchronized.


## Flask WebApp with CRUD operations 
- Home Page
 
![Screenshot](Screenshots/Home.png)

- Item Page

![Screenshot](Screenshots/Item.png)

- Add New Item Page 

![Screenshot](Screenshots/AddNewItem.png)

- Delete Item

![Screenshot](Screenshots/Delete.png)

- Edit Item

![Screenshot](Screenshots/EditItem.png)
