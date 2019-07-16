# Ambassador Coding Challenge

Our coding challenge is your opportunity to demonstrate your experience, skills, and aptitude by building a prototype of the web’s most minimal referral automation software.

## Alvey's Application
I'll be developing a full-stack application as instructed. Code was initially wrote on my public repo: https://github.com/Jual6332/legendary_referral_list and is available there as well. I initially built a ToDo application using Django and JavaScript to prepare for this submission that I repurposed for the solution. You'll find a lot of the code asks for a model 'todo' that could easily be renamed 'referral_link' if I had extra time in the configuration stage of this project. 

## Problem Statement:
- Tim's needs us to build a web app for his referrals. This app will feature two pages: a home page where referral links exist and a landing page where each link is redirected.
- The home page or referral links page will include the number of clicks associated with each referral link.
- The landing page will track the number of visits.

## Proposed Solution:
- My solution focuses on the full-stack.
- A REST Api will be built that allows for CRUD (Create, Read, Update, Delete) operations. This will feature a minimal backend, Browsable Api.
- A client-side app will be developed for a user interface that is easy-to-use. 

## Architecture
### Forms - todo/forms.py
- A single form was implemented called 'TodoForm' which is used for text input for each referral link title. 

### Models - todo/models.py
- A single model was implemented called 'Todo' which servses as the referral link model. As mentioned, I initially built a ToDo application using Django and JavaScript to prepare for this submission that I repurposed for the solution. This explains why 'todo' is the name of the model but the functionality is as expected.
- Within the 'todo' model are three fields: one text field 'title' for the name of the link, one boolean field 'Completed' if the link still exists, one integer field 'hits' for the number of hits. The 'title' and 'hits' are fields are the most relevant.

### Requirements - todo/requirements.txt
The requirements for this project are outlined below. Most important requirements are python==3.5.2 (or higher) and django==2.2.3 (or higher)

- beautifulsoup4==4.4.1
- chardet==2.3.0
- CppHeaderParser==2.7.4
- cycler==0.9.0
- dblatex==0.3.7.post1
- decorator==4.0.6
- defusedxml==0.4.1
- django==2.2.3
- geopy==1.11.0
- html5lib==0.999
- lxml==3.5.0
- Magic-file-extensions==0.2
- matplotlib==1.5.1
- numpy==1.11.0
- Pillow==3.1.2
- ply==3.11
- pygame===1.9.1release
- pygpgme==0.3
- pylepton==0.1.2
- pyliblzma==0.5.3
- pyparsing==2.0.3
- python==3.5.2
- python-apt==1.1.0b1+ubuntu0.16.4.2
- python-dateutil==2.4.2
- python-xlib==0.14
- pytz==2014.10
- scipy==0.17.0
- scour==0.32
- six==1.10.0
- SOAPpy==0.12.22
- virtualenv==15.0.1
- wstools==0.4.3

### Views - todo/views.py

### Webpages - todo/templates/todo
- index.html - Homepage where referral links exist and are ordered for the user.
- landing_page.html - The landing page requested where the name of the referral link appears in the title {Wolverines} are best! and in the link url: localhost:8000/landingpage/{link_id}/{link_title}/.
- edit_form.html - Decided to build a separate webpage for editing the referral link. After typing in the name of the referral, user is redirected to the index.html homepage again.

## Technical Choices: 
### Python for back-end development
- Python is fairly easy to learn and a language I already knew.
- Python has a rich community of developers.
- An in-demand skill for industry.

#### Django REST framework (DRF)
- I have a decent understanding of the MTV architectural pattern and would like to challenge myself for this project.
- "The framework for perfectionists with deadlines."
- I'm excited to build an API with Django.

## VanillaJS for front-end development
- I decided to go with "normal" JavaScript ES6 for simplicity. Basic idea for JS ES6 is write less, do more. 
- There was no requirement for real-time rendering (virtual DOM), otherwise I would have to go with ReactJS.

## Tradeoffs: 
- Editing a link deletes the old link and provides a new one. This results in the counter dropping down to 0 clicks. This made the most sense to me, as I saw the referral changing as an entirely new referral. 
- I developed the front-end with Vanilla JS. In the future I'd like to implement ReactJS components to show an even more in-depth full-stack competency.
- I perscribe to the Pythonic pillar that if you have two solutions that both accomplish the task: one complicated and one simple, choose the simple solution. 
- In the future, I'd like to implement user authentication to more closely resemble the referral links web app as a software product.
- In the future, I'd like to work on providing robust test cases. My plan was to implement more tests but I resorted to manually testing each component to make sure things worked from a user experience standpoint.
- Adding a link: Referral links are unfortunately not unique. Adding a new item that already exists will create a duplicate. I would change this by attempting to 'get' the object

## Heroku Deployment:
Did not complete in time. Coming soon!


## Other projects!
