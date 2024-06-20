### Basic Features of The App
    
* Register – Users can register and create a new profile
* Login - Registered users can login using username and password


To get this project up and running locally on your computer follow the following steps.
1. Set up a python virtual environment
2. Run the following commands
```
$ python manage.py migrate
$ python manage.py createsuperuser
$ python manage.py runserver
```
   
3. Open a browser and go to http://localhost:8000/


How it was created

Step 1: Create a new project (django-admin startproject login)
Step 2: cd login
Step 3: Create a new app (django-admin startapp app)
Step 4: Register the app in the project (#login/settings.py add 'app',)
Step 5: Create the following dir (#app/templates/app/index.html,login.html,register.html)
                                (#app/urls.py)
                                (#app/forms.py)
                                (#app/decorators.py)
Step 6: Include the path of the app urls to the project urls
Step 7: Create views for the three html files and urls path for each of them
Step 8: Migrate the project db (python manage.py migrate)
Step 9: Create superuser (python manage.py createsuperuser)
Step 10: In the app views.py import the following (redirect, UserCreationForm, authenticate, login, logout, messages, login_required, and all function created in decorators.py and forms.py i.e (unathenticated_user and CreateUserForm))
Step 11: Write the createuserform in views.py to save data inputed by the user and using the CreateUserForm form from forms.py to edit and choose data to be inputed by user
Step 12: For the login use authenticate to compare data inputed by the user with already existing data
Step 13: Create the logout function
Step 14: Add the login_required function to the home view to prevent unathenticated_user from viewing it 
Step 15: Create the unathenticated_user function in decorators.py
Step 16: Create the CreateUserForm function in forms.py
Step 17: Write your register,login and index html and css code