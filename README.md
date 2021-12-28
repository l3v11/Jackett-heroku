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
