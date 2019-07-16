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
- I kept everything to a single Referral model given that we aren't keeping track of any other type of entity or relationship.
Within the Referral model, I only added the two 'Title' and 'Clicks' fields, given that the link will always just be a standard '{url}/ + title'
- I debated having the 'Clicks' increment action just be a part of the same endpoint as the GET call for the details of a single referral. However, I could think of a few other instances where that endpoint might be utilized and the customer would not want clicks incremented (IE a "details" screen, an edit screen that doesn't take the referral information directly from the rows in the list page).
- I chose instead to create a separate endpoint where a deliberate 'POST' call will increment the Clicks number for the relevant referral entry.

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
