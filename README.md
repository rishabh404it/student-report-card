# student-report-card
Generating STUDENT REPORT CARD


This mini backend only project contains the following:

         1. CRUD endpoints for students, subjects and marks.

         2. An endpoint for scheduling a job that will prepare a report card for a specific student and then send the prepared report card to the student using email.

         3. An endpoint to check the status of the job using the job id returned from the previous endpoint.

         4. Used Celery / Crontab for asynchronous job processing.


Name of project - mysite

Name of app - myapp

Local Endpoint : http://127.0.0.1:8000/

Query 1 - How to get the app running ?

         1. Create an virutal env.
         
         2. RUN the following commands:
                     > pip3 install -r requirements.txt 
                     > python3 manage.py runserver


Query 2 - How to test the assigned task ?

         1. Run server & go to http://localhost/ (Containing all the required URLS in route)
         
         2. Right now, I have added data of 2 students namely Rishabh & Mradhul in local db. You have to update/change their emails to the email you want to send report to.  
                     > Goto URL: http://127.0.0.1:8000/student-data/
                     > Use Update Operation in API to update the email of student by http://127.0.0.1:8000/student-data/{id}/
                     > Do this for both students data        
         
         3. In settings.py, on Line 141 & 142, please add the email and password from which you want the email to be sent to
                     > EMAIL_HOST_USER = '' # Enter Your Email from which you want to send email to students
                     > EMAIL_HOST_PASSWORD = '' # Enter Your GMail Password
                     
         4. Ok now you are all set for testing, Hit the following URL in sequence listed below to get your report sent to email.
                     > Initialise Celery by hitting: http://127.0.0.1:8000/initialise-celery/ (Click on next URL as this URL starts loading)
                     > Generate & Mail Report by hitting: http://127.0.0.1:8000/generate-student-report/
                     > Report Sent to mail successfully
                     
Query 3 - Find CRUD APIs for Student, Subject & Marks Data in the following URLS:                   
         1. http://127.0.0.1:8000/student-data/         
         2. http://127.0.0.1:8000/subjects/      
         3. http://127.0.0.1:8000/student-marks/

Query 4 - Find endpoint for finding the status of Task/Job:
         > http://127.0.0.1:8000/check-job-status/
                     
Please let me know if you have any queries 

Rishabh Mishra

mishrarishabh404it@gmail.com
