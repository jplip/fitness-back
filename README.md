# Fitness Tracker

> This serves serves as the backend locally running serving for our Futness Tracker Practice Tracker. 

## Idea

> The purpose of project is to serve APIs.  It is the backend piece of a Full-Stack project to get data from the frontend and create users based on that data and being able to update data (frontend) of an Fitness Practice Tracker

### Files and Directories in this Project

These are some of the key files and directories in this project

README.md: This file contains instructions for setting up the necessary tools and cloning the project (insrumet practice rrucker) A README file is a standard component of all properly set up GitHub projects.

requirements.txt: This file lists the dependencies required to turn this Python project into a Flask/Python project. It may also include other backend dependencies, such as dependencies for working with a database.

main.py: This Python source file is used to run the project. Running this file starts a Flask web server locally on localhost. During development, this is the file you use to run, test, and debug the project.

Dockerfile and docker-compose.yml: These files are used to run and test the project in a Docker container. They allow you to simulate the project’s deployment on a server, such as an AWS EC2 instance. Running these files helps ensure that your tools and dependencies work correctly on different machines. this has been succesfully deployed.

instances: This directory is the standard location for storing data files that you want to remain on the server. For example, SQLite database files can be stored in this directory. Files stored in this location will persist after web application restart, everything outside of instances will be recreated at restart.

static: This directory is the standard location for files that you want to be cached by the web server. It is typically used for image files (JPEG, PNG, etc.) or JavaScript files that remain constant during the execution of the web server.

api: This directory contains code that receives and responds to requests from external servers. It serves as the interface between the external world and the logic and code in the rest of the project. This folder has been updated to handle user data in the backend! Check out /api/users! I also added a new resource!

model: This directory contains files that implement the backend functionality for many of the files in the api directory. For example, there may be files in the model directory that directly interact with the database. This data has the tracking data!

templates: This directory contains files and subdirectories used to support the home and error pages of the website.

.gitignore: This file specifies elements to be excluded from version control. Files are excluded when they are derived and not considered part of the project’s original source. In the VSCode Explorer, you may notice some files appearing dimmed, indicating that they are intentionally excluded from version control based on the rules defined in .gitignore.

### Implementation Summary

#### July 2023

> Updates for 2023 to 2024 school year.

- Update README with File Descriptions

#### January 2023

> This project focuses on being a Python backend server.  Intentions are to only have simple UIs an perhaps some Administrative UIs.

#### September 2021

> Basic UI elements were implemented showing server side Flask with Jinja 2 capabilities.

- Project entry point is main.py, this enables Flask Web App and provides capability to renders templates (HTML files)
- The main.py is the  Web Server Gateway Interface, essentially it contains a HTTP route and HTML file relationship.  The Python code constructs WSGI relationships for index, kangaroos, walruses, and hawkers.
- The project structure contains many directories and files.  The template directory (containing html files) and static directory (containing js files) are common standards for HTML coding.  Static files can be pictures and videos, in this project they are mostly javascript backgrounds.
- WSGI templates: index.html, kangaroos.html, ... are aligned with routes in main.py.
- Other templates support WSGI templates.  The base.html template contains common Head, Style, Body, Script definitions.  WSGI templates often "include" or "extend" these templates.  This is a way to reuse code.
- The VANTA javascript statics (backgrounds) are shown and defaulted in base.html (birds), but are block replaced as needed in other templates (solar, net, ...)
- The Bootstrap Navbar code is in navbar.html. The base.html code includes navbar.html.  The WSGI html files extend base.html files.  This is a process of management and correlation to optimize code management.  For instance, if the menu changes discovery of navbar.html is easy, one change reflects on all WSGI html files.
- Jinja2 variables usage is to isolate data and allow redefinitions of attributes in templates.  Observe "{% set variable = %}" syntax for definition and "{{ variable }}" for reference.
- The base.html uses combination of Bootstrap grid styling and custom CSS styling.  Grid styling in observe with the "<Col-3>" markers.  A Bootstrap Grid has a width of 12, thus four "Col-3" markers could fit on a Grid row.
- A key purpose of this project is to embed links to other content.  The "href=" definition embeds hyperlinks into the rendered HTML.  The base.html file shows usage of "href={{github}}", the "{{github}}" is a Jinja2 variable.  Jinja2 variables are pre-processed by Python, a variable swap with value, before being sent to the browser.
