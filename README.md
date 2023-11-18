# flask_7_auth

[assignment](https://github.com/hantswilliams/HHA_504_2023/blob/main/WK7/assignment7.md): This week, you'll be delving into the core of application security: user sessions and authentication. Utilizing Flask and an external identity provider like Google Cloud, ensure your Hospital Priceline application is both user-friendly and secure.

# Set up:
1. Create a a `templates` folder with `dashboard.html` and `index.html`
2. Use given [code1](https://github.com/hantswilliams/HHA_504_2023/blob/main/WK7/google_flask_app/templates/dashboard.html) and [code2](https://github.com/hantswilliams/HHA_504_2023/blob/main/WK7/google_flask_app/templates/index.html) to insert into `dashboard.html` and `index.html`
3. Create an `app.py` file with this [code](https://github.com/EugeneHsiung/flask_7_auth/blob/main/app.py`) inside
4. Create a `db_functions.py` with this [code](https://github.com/EugeneHsiung/flask_7_auth/blob/main/db_functions.py) inside
5. Create a `requirements.txt` for packages, `.gitignore` that hides confidential information in `.env`, and `.env` file to put in confidential information
6. Follow this [guide](https://github.com/hantswilliams/HHA_504_2023/blob/main/WK7/google_flask_app/readme.md) for Setting up API Signin.
   1. First need to create a project
   2. Then need to create a generic oauth consent screen
    - call it whatever you want
    - need to have support email
    - can add in a logo or photo if you want
    - authorized domains: 
        - `cloudshell.dev`
    3. Then can go into credentials -> create credentials 
    - should create - 'oAuth client' --> 'for Web Server/Application'
    - add javascript origins: 
        - `https://5000-cs-213132341638-default.cs-us-east1-pkhd.cloudshell.dev`
    - add redirect URIs: 
        - need to make sure that the redirect has `/google/auth/` to match the route in the app.py file
        - be sure to include the final `/` in there
        - `https://[yousertroutegeneratedhere].cloudshell.dev/google/auth/`
7. Following the API set up, add in `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` information in the `.env` file.
8. In the `app.py` file, make sure to edit and uncomment the `redirect_uri`
9. Screenshots of what the application looks like can be found [here](https://github.com/EugeneHsiung/flask_7_auth/tree/main/screenshots)
