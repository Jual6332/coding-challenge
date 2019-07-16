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

### URLS - todo/urls.py
-Each of the view functions below is called by a url. An example urlpattern: 
  path('delete/<todo_id>', views.deleteTodo, name='deleteTodo') which is called from the html page when the trash icon is selected which calls this url by {% url 'deleteTodo' %} and passes in the property <todo_id>. The deleteTodo view is then selected.

### Views - todo/views.py
-Each CRUD request is handled by a view-function in todo/views.py. The function views are addTo, deleteTodo, deleteallTodos, editTodo, saveTodo, index, landing_page. The last two are views for rendering the html files. The number of landing page visits (numLandingVisits) is a global variable that is incremented within the landingpage view and each referral link hit is handled here too.

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

## How can I test this Application?
From root directory run:
```python
python3 manage.py runserver
```
This will start the back-end server on localhost:8000.

## Other projects!
- https://github.com/Jual6332/OTheRS_IP: A repository for the code that runs the OTheRS - Optical Thermal Regulation System. This was an aerospace project built to monitor the temperature fluctuations on-board the General Atomics satellite. This software release explores image processing, computer vision, machine learning, and other advanced algorithms. **Code written in this repo will fly to _space_ this year!** Of 5 programmers, I contributed 120 commits and oversaw more commits out of 210 total commits. I've been given permission to share this code. 12-month contract.
- https://github.com/Jual6332/HarnessOnline: A repository for the code that runs a MERN full-stack mission planning software app. This was a research and development project for an aerospace company called OneWeb. They are currently racing Musk and Bezos to build a satellite constellation to bring connectivity to underprivileged areas and rural communities. I built the front-end components for this repo which was itself a component of a larger entity. I've been given permission to share this code. 3-month contract.
- https://github.com/Jual6332/TaskHub-WebApp: A computer science lab project built for our software development class. A social media-type system for work that allows managers to send task requests to employees. Keeps track of employee performance based on task history. Software developed using LAMP stack, built with PHP and MySQL. This was a team of 4 project where myself and another student wrote a majority of the back-end code in PHP and front-end code in HTML/CSS/JavaScript w/ Bootstrap. Of 172 commits, I contributed 110 commits and another student made 36 commits. See our README.md here: https://github.com/Jual6332/TaskHub-WebApp/blob/master/README.md for full project breakdown.
- https://github.com/Jual6332/Geospatial-Software-Design-Matlab: An aerospace lab project to study and model the three-body problem. The three-body problem demonstrates the physics of three entities and in this case: satellite, Earth, moon. Thihs code tracks the trajectory of a theoretical satellite as it launches from the Earth's surface and attempts to fly around the moon and back to Earth. Before optimization, the satellite does crash into the moon. Our goal was to find the required fuel to assure the satellite can successfully miss the moon and fly back to Earth. See https://github.com/Jual6332/Geospatial-Software-Design-Matlab/blob/master/Rafii_Alvey_Hw2_ASEN_4057_Report.pdf for our cool lab report and thought process. 
