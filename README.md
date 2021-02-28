# blank-website

https://www.heroku.com/
Boilerplate website hosted on heroku free tier.

Follow the steps to start your python/Flask based website hosted on Heroku!

## Deploy Website Step List

- Create a heroku account
- Verify your email address
- Click the "New" dropdown at the top right of the page, then click "Create new app"
![image](https://user-images.githubusercontent.com/51305946/109360354-12ece380-7855-11eb-9bee-bdf04a6e5afd.png)
- Give your website a name (this will be the name of the url created) ie "blank-website" will be https://blank-website.herokuapp.com
- Now fork this repository and customize! [FLASK Tutorial](app/app_basic.md)
- Connect your GitHub account in the middle of this page
![image](https://user-images.githubusercontent.com/51305946/109361085-5431c300-7856-11eb-9d88-3c0beb666cad.png)
- Select your customized repository and click "Deploy Branch" at the bottom of the page
- Your app will be deployed and you can open your app at the top of the page by clicking "Open App"

## Heroku files

### Procfile
> This file will give the configurations of your application MUST BE NAMED EXACTLY "Procfile" 

```
##-COMMENT-$$ web app using "gunicorn" for deploying calling "run(.py)" and building "app"
web gunicorn run:app

##-COMMENT-$$ web=1 means 1 dyno (essentially free tier)
heroku ps:scale web=1
```

## Python files

### requirements.txt
> Heroku needs a requirements file for deploying to build the python environment.

### runtime.txt
> Heroku also needs a runtime file that gives a compiler (python) as well as a version (3.9.1)

### run.py
> This will build flask application (you can run this locally to test)

```bash
python3 run.py
```

You can exit the app by pressing CTRL + C