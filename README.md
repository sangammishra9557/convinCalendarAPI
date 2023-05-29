
# Convin Backend Intern Assignment By Sangam Mishra


In this assignment you have to implement google calendar integration using django rest api. You need to use the OAuth2 mechanism to get users calendar access. Below are detail of API endpoint and corresponding views which you need to implement

    /rest/v1/calendar/init/ -> GoogleCalendarInitView()
This view should start step 1 of the OAuth. Which will prompt user for his/her credentials

    /rest/v1/calendar/redirect/ -> GoogleCalendarRedirectView()
This view will do two things
- Handle redirect request sent by google with code for token. You need to implement mechanism to get access_token from given code
- Once got the access_token get list of events in users calendar


## Run Locally

Clone the project

```bash
  git clone 
```


Create Project

 ```bash
  Go to console.cloud.google.com
  Add Calendar API from Services
```  

Generate Credentials

```bash
  Go to generate credentials
  step1 Web Application in app type
  step2 add url in Authorized JavaScript origins as http://localhost:8000
  step3 add urls in Authorized redirect URIs
         URL1 ->http://localhost:8080/
         URL2 ->http://localhost:8000/rest/v1/calendar/init/
        Save 
  step4 download credentials.json in base project directory
```


Install dependencies

```bash
  pip install requirements.txt
```

Start the server

```bash
  python manage.py runserver
```
