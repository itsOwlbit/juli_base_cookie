# j_cookie

Juli's base cookiecutter-django project.

[![Built with Cookiecutter Django](https://img.shields.io/badge/built%20with-Cookiecutter%20Django-ff69b4.svg?logo=cookiecutter)](https://github.com/cookiecutter/cookiecutter-django/)

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

