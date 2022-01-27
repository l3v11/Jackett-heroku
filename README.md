### Deploy
- Clone the repo
- Install [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)

```
cd Jackett-heroku
heroku login
heroku apps:create APP
heroku stack:set container
git push heroku main --force
```

### Deploying with Github Workflow

1. Go to Repository Settings -> Secrets

2. Add the below Required Variables one by one by clicking New Repository Secret every time.

  - HEROKU_EMAIL: Heroku Account Email Id in which the above app will be deployed
  - HEROKU_API_KEY: Your Heroku API key, get it from https://dashboard.heroku.com/account
  - HEROKU_APP_NAME: Your Heroku app name, Name Must be unique and in **NO CAPS**

4. After adding all the above Required Variables go to Github Actions tab in your repository

5. Then click on Run workflow

