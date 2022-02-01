### Jackett on Heroku
> Host your very own [Jackett](https://github.com/Jackett/Jackett) on Heroku

### Deploying with CLI
- Clone the [repo](https://github.com/l3v11/Jackett-heroku)
- Install [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)

```
cd Jackett-heroku
heroku login
heroku apps:create $APP
heroku stack:set container -a $APP
heroku git:remote -a $APP
git push heroku main --force
```

### Deploying with Workflow
- Fork the [repo](https://github.com/l3v11/Jackett-heroku)
- On the forked repo, go to *Settings* -> *Secrets* and click on the *New repository secret* button
- Now enter the vars one by one with value
1. `HEROKU_API_KEY`: Get the API Key from Heroku [Account Settings](https://dashboard.heroku.com/account)
2. `HEROKU_EMAIL`: Email address of your Heroku Account
3. `HEROKU_APP_NAME`: Name of your Heroku App. It must be unique on Heroku.
- Then go to the *Actions* tab on your repo
- Select *Deploy to Heroku* from the *All workflow* list
- Click on *Run workflow* -> *Run workflow*
- After that turn on the app dyno


### Updating Jackett
- Scheduled to update at 12:00 on every Sunday
- If you don't like to update automatically, go to *Settings* -> *Actions* -> *General* on the forked repo and select *Disable Actions*
> **Note:** For [Deploying with Workflow](https://github.com/l3v11/Jackett-heroku#deploying-with-workflow) method only
