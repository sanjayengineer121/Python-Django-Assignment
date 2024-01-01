# Python-Django-Assignment

# --------Login Page using djangi rest framewoork

<img src="https://i.postimg.cc/43T92KyM/01-01-2024-21-45-33-REC.png">

# ------New User sign up authentication

<img src="https://i.postimg.cc/Dfg38R1b/01-01-2024-21-46-03-REC.png">

# ------Logout after that only authentication (it is not a refresh token)

<img src="https://i.postimg.cc/gkxpQN6X/01-01-2024-21-45-15-REC.png">

# ----------------------------------------------------------------------

# ---------------I have connected mangodb database -----------------

----- Frame work used

- Werkzeug==2.3.7
- django-auth-framework==2.0.7
- WTForms==3.0.1
- djongo==1.3.6
- pymongo==4.6.1
- Django==5.0
- djangorestframework

<br>

#-------------How to run

@ First run command

pip install -r requirements.txt

@ second open mongo db graphical application and start server-

- setp 1
  <img src="https://i.postimg.cc/X7DsD6RF/01-01-2024-23-43-58-REC.png">
- step 2
- after press on connect i can se it is connected
  <img src="https://i.postimg.cc/3w6yPnKt/01-01-2024-23-44-22-REC.png">
- step 3
- press on plus icon to create a database(schema)
  <img src="https://i.postimg.cc/gr9HmGmB/01-01-2024-23-44-22-REC.png">
- step 4
- after submitting database and collection name
  <img src="https://i.postimg.cc/Nj2vd4zs/01-01-2024-23-44-40-REC.png">
  <img src="https://i.postimg.cc/vTSHVmc3/01-01-2024-23-44-55-REC.png">
- step 5
  enter detail below and update in settings.py
  <img src="https://i.postimg.cc/q7Rr8rHF/01-01-2024-23-46-57-REC.png">
- setp 6
  after that
  we have to migrate that changes
  1. python manage.py migrate
  2. python manage.py makemigrations

- step 7
  check in mongo db
  <img src="https://i.postimg.cc/NGy1d2xs/01-01-2024-23-46-27-REC.png">

- step 8
  run command to run django server

  loginproject>python manage.py runserver



APIs
- Login API
-
  1. #akes phone number and password
  2. Create the user if it does not exist
  3. Validate the credentials and generate the user auth token
  4. Returns the response in the JSON format
  
# Profile API
- 
  Takes the user auth token as input in the headers
  Returns the user profile information in JSON format

# Logout API
 - Takes the user auth token as input in the headers
- Logs out and clears all the sessions and token information for that user
- Returns the response
 - Post logout, if we try profile API, it should not work as the user is logged
out

