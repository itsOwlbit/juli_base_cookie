# j_cookie

Juli's base cookiecutter-django project.

[![Built with Cookiecutter Django](https://img.shields.io/badge/built%20with-Cookiecutter%20Django-ff69b4.svg?logo=cookiecutter)](https://github.com/cookiecutter/cookiecutter-django/)

This project was created to learn about creating a project in cookiecutter-django with docker.  The capstone project I am working on with a team is to modernize the STOQS development environment by porting the existing code base into a new project, a dockerized cookiecutter-django web application.  Since I have not worked with django, cookiecutter, or docker, the first milestone was to learn the development stack.  This repo documents what I have learned in my first milestone.

---


## Have the following installed:
* Python (I had 3.9.13 installed)
* Cookiecutter (this needed for cookiecutter-django)

      pip install cookiecutter
      
* Docker Desktop

---


## Instructions for running this cookie project on local machine

### The following are done in terminal

1. Create directory to download this repo:

      ```
      mkdir capstone_project1
      ```

2. Go into new directory:

      ```
      cd capstone_project1
      ```

3. Initialize git:

      ```
      git init
      ```

4. Pull repo (make sure your ssh is already set up):

      ```
      git pull git@github.com:itsOwlbit/juli_base_cookie.git
      ```

5. Go into the cookie project directory:

      ```
      cd j_cookie
      ```

6. Launch Docker Desktop or equivalent for your system.
7. Build project:

      ```
      docker-compose -f local.yml build
      ```

8. Run project:

      ```
      docker-compose -f local.yml up
      ```

9. Open browswer and enter the following url:

      ```
      http://127.0.0.1:8000
      ```

      or

      ```
      localhost:8000
      ```

10. You should now see the project page.


### To quit, do the following

15. Ctrl + C in the terminal that is running docker-compose (from step 11-12)
16. Deactivate the virtual environment:

      ```
      deactivate
      ```
      
17. You are now all done.

---

## The instructions on how to re-create my base project from scratch


1. Create a project directory:

      ```
      mkdir cookie_project
      ```

2. Go into new directory:

      ```
      cd cookie_project
      ```

3. Create virtual environment:

      ```
      virtualenv cEnv
      ```

4. Activate the virtual environment:

      ```
      source cEnv/bin/activate
      ```

5. Generate a cookiecutter-django project:

      ```
      cookiecutter gh:cookiecutter/cookiecutter-django
      ```

6. Enter project generation options.  The following is what I entered.

      ```
      project_name [My Awesome Project]: j_cookie
      project_slug [reddit_clone]: <optional>
      description [Behold My Awesome Project!]: Juli’s cookiecutter project.
      author_name [Daniel Roy Greenfeld]: JuliS
      domain_name [example.com]: <default>
      email [daniel-greenfeld@example.com]: <default>
      version [0.1.0]: <default>
      Select open_source_license:
      1 - MIT
      2 - BSD
      3 - GPLv3
      4 - Apache Software License 2.0
      5 - Not open source
      Choose from 1, 2, 3, 4, 5 [1]: 3
      Select username_type:
      1 - username
      2 - email
      Choose from 1, 2 [1]: <default>
      timezone [UTC]: <default>
      windows [n]: <default>
      use_pycharm [n]: <default>
      use_docker [n]: y
      Select postgresql_version:
      1 - 14
      2 - 13
      3 - 12
      4 - 11
      5 - 10
      Choose from 1, 2, 3, 4, 5 [1]: <default>
      Select cloud_provider:
      1 - AWS
      2 - GCP
      3 - None
      Choose from 1, 2, 3 [1]: 3
      Select mail_service:
      1 - Mailgun
      2 - Amazon SES
      3 - Mailjet
      4 - Mandrill
      5 - Postmark
      6 - Sendgrid
      7 - SendinBlue
      8 - SparkPost
      9 - Other SMTP
      Choose from 1, 2, 3, 4, 5, 6, 7, 8, 9 [1]: <default>
      use_async [n]: <default>
      use_drf [n]: y
      Select frontend_pipeline:
      1 - None
      2 - Django Compressor
      3 - Gulp
      4 - Webpack
      Choose from 1, 2, 3, 4 [1]: 2?
      use_celery [n]: <default>
      use_mailhog [n]: <default>
      use_sentry [n]: <default>
      use_whitenoise [n]: y
      use_heroku [n]: <default>
      Select ci_tool:
      1 - None
      2 - Travis
      3 - Gitlab
      4 - Github
      Choose from 1, 2, 3, 4 [1]: 4
      keep_local_envs_in_vcs [y]: n
      debug [n]: <default>
      ```

8. Install project requirements:

      ```
      pip install -r requirements/local.txt
      ```

9. Project is now created.  Follow instructions on how to build and run the program.

---


## After project has been created, each time you want to run the project do the following:

1. You can either use terminal or VSC's terminal.  Start virtual environment.  Also, start Docker Desktop.

2. Build project:

      ```
      docker-compose -f local.yml build
      ```

3. Run project:

      ```
      docker-compose -f local.yml up
      ```

4. Open browser and go to localhost port 8000 to view project:

      ```
      http://127.0.0.1:8000
      ```

      or

      ```
      localhost:8000
      ```

5. When closing the project.  In the terminal the project is running, press CONTROL-C to stop the program.  Then stop the virtual environment by typing:

      ```
      deactivate
      ```


