# SocialCopsInternChallenge
This is hiring challenge of Social Cops Intern.

Refer to Problem Statement doc for Problem Statement.

Verdict : Selected

Solution Information :

  SocialCops Internship Selection Project 1 : Amnesia


	TECH STACK 

FrontEnd : AngularJs +  Javascript + CSS + BootStrap + HTML
BackEnd : ElasticSearch + Flask + Python + twilio ( helper library )

	IMPORTANT LINKS

Link to postman collection : https://www.getpostman.com/collections/37efa72b2311be599b30

Link to hosted application : https://e-slam-ee.herokuapp.com/templates/alarm.html

[ NOTE : Please open the above link with chrome browser that too Disabling CORS
Just follow the link --> "chrome.exe --user-data-dir="C:/Chrome dev session" --disable-web-security" (without quotes)

And then open application link.

This is because I was unable to handle CORS issue. ]

        OVERVIEW 

Key features are handles as follow.

1. Messaging : Messaging is handled using twilio and employing background thread to sleep every 1 hour and re run after that.
               Datetime library is used to disable messaging at night.

2. Error logging : Used Try-Exceptions to handle the issue.

3. Calculating hours elapsed : Used datetime inbuilt python library. 

** Night time is taken as 10pm to 6am IST.

Working :

Each time John(User) enters the new number on webpage, number is updated at backend
and messages are directed to that number. Page contains buttons for displaying logs and hours elapsed.
Check site link for detailed process.

Refer code for details.


	APP STRUCTURE

Schema : 

alarm 
     phone 
     number(String)		logs(List of Strings)		start_time(String)


Essential Directory : 

Backend :

SocioCops
  |
  |-app
     |
     |-AlarmApp
          |
          |-init.py
          |-credentials.py
          |-utils.py
          |-views.py

The essential code lies in the 4 files mentioned.
