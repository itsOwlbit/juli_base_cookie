# j_cookie

Juli's base cookiecutter-django project.

[![Built with Cookiecutter Django](https://img.shields.io/badge/built%20with-Cookiecutter%20Django-ff69b4.svg?logo=cookiecutter)](https://github.com/cookiecutter/cookiecutter-django/)
[![Black code style](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/ambv/black)

License: GPLv3

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
      git pull git@github.com:OtterBots/capstone_phase1.git
      ```

5. Go into the cookie project directory:

      ```
      cd j_cookie
      ```

6. Create virtual environment:

      ```
      virtualenv cEnv
      ```

7. Activate the virtual environment:

      ```
      source cEnv/bin/activate
      ```

8. Install project requirements:

      ```
      pip install -r requirements/local.txt
      ```

9. Launch VSC from terminal (or just start the program):

      ```
      code .
      ```

### The following are now in VSC terminal (or stay in previous terminal)

10. Launch Docker Desktop or equivalent for your system.
11. Build project:

      ```
      docker-compose -f local.yml build
      ```

12. Run project:

      ```
      docker-compose -f local.yml up
      ```

13. Open browswer and enter the following url:

      ```
      http://127.0.0.1:8000
      ```

      or

      ```
      localhost:8000
      ```

14. You should now see the project page.

### To quit, do the following

15. Ctrl + C in the terminal that is running docker-compose (from step 11-12)
16. Deactivate the virtual environment:

      ```
      deactivate
      ```
      
17. You are now all done.

---

## Instructions created by Juli (for starting project from scratch)

[Google Doc Project Instruction](https://docs.google.com/document/d/1uXRQZkgvClViREfilYFOCVjuYPGl_HTJ2x6oTj8UpZo/edit?usp=sharing)

---
---

## Default readme file generated when creating the project is below.

### Settings

Moved to [settings](http://cookiecutter-django.readthedocs.io/en/latest/settings.html).

### Basic Commands

#### Setting Up Your Users

- To create a **normal user account**, just go to Sign Up and fill out the form. Once you submit it, you'll see a "Verify Your E-mail Address" page. Go to your console to see a simulated email verification message. Copy the link into your browser. Now the user's email should be verified and ready to go.

- To create a **superuser account**, use this command:

      $ python manage.py createsuperuser

For convenience, you can keep your normal user logged in on Chrome and your superuser logged in on Firefox (or similar), so that you can see how the site behaves for both kinds of users.

#### Type checks

Running type checks with mypy:

    $ mypy j_cookie

#### Test coverage

To run the tests, check your test coverage, and generate an HTML coverage report:

    $ coverage run -m pytest
    $ coverage html
    $ open htmlcov/index.html

##### Running tests with pytest

    $ pytest

#### Live reloading and Sass CSS compilation

Moved to [Live reloading and SASS compilation](https://cookiecutter-django.readthedocs.io/en/latest/developing-locally.html#sass-compilation-live-reloading).

### Deployment

The following details how to deploy this application.

#### Docker

See detailed [cookiecutter-django Docker documentation](http://cookiecutter-django.readthedocs.io/en/latest/deployment-with-docker.html).
