# HEROKU-commands

# Heroku CLI Commands

This document provides a list of commonly used **Heroku CLI** commands for managing Heroku applications, deployments, logs, and more.

---

## **Authentication & Setup**

- **Login to Heroku**
  ```bash
  heroku login
  ```
- **Check installed Heroku version**
  ```bash
  heroku --version
  ```
- **Logout from Heroku**
  ```bash
  heroku logout
  ```

---

## **App Management**

- **List all apps in your account**
  ```bash
  heroku apps
  ```
- **Create a new Heroku app**
  ```bash
  heroku create app-name
  ```
- **Rename an app**
  ```bash
  heroku apps:rename new-app-name --app old-app-name
  ```
- **Delete an app**
  ```bash
  heroku apps:destroy --app app-name
  ```

---

## **Deployment**

- **Deploy code from Git**
  ```bash
  git push heroku main
  ```
- **Rollback to the previous release**
  ```bash
  heroku releases:rollback
  ```
- **View recent releases**
  ```bash
  heroku releases --app app-name
  ```

---

## **Dyno (Process) Management**

- **Restart all dynos**
  ```bash
  heroku restart --app app-name
  ```
- **Restart a specific dyno**
  ```bash
  heroku restart web --app app-name
  ```
- **Scale dynos (increase or decrease the number of running instances)**
  ```bash
  heroku ps:scale web=2 --app app-name
  ```
- **Check dyno status**
  ```bash
  heroku ps --app app-name
  ```

---

## **Logs & Monitoring**

- **View real-time logs**
  ```bash
  heroku logs --tail --app app-name
  ```
- **View last 100 log lines**
  ```bash
  heroku logs --num 100 --app app-name
  ```
- **Check application metrics**
  ```bash
  heroku metrics --app app-name
  ```

---

## **Configuration & Environment Variables**

- **Set an environment variable**
  ```bash
  heroku config:set VAR_NAME=value --app app-name
  ```
- **View all environment variables**
  ```bash
  heroku config --app app-name
  ```
- **Remove an environment variable**
  ```bash
  heroku config:unset VAR_NAME --app app-name
  ```

---

## **Database Management**

- **View database credentials**
  ```bash
  heroku config | grep DATABASE_URL
  ```
- **Run database migrations**
  ```bash
  heroku run python manage.py migrate --app app-name
  ```
- **Connect to the database console**
  ```bash
  heroku pg:psql --app app-name
  ```

---

## **Running Commands on Heroku**

- **Run a command inside a Heroku dyno (useful for running scripts, migrations, or debugging)**
  ```bash
  heroku run bash --app app-name
  ```
- **Run a one-off command (e.g., checking Python version in a Django app)**
  ```bash
  heroku run python --version --app app-name
  ```

---

## **Add-ons & Plugins**

- **List all add-ons installed on your app**
  ```bash
  heroku addons --app app-name
  ```
- **Add a new add-on**
  ```bash
  heroku addons:create heroku-postgresql:hobby-dev --app app-name
  ```
- **Remove an add-on**
  ```bash
  heroku addons:destroy heroku-postgresql --app app-name
  ```

---

## **Git & Remote Repository**

- **Add Heroku as a remote repo (if missing)**
  ```bash
  heroku git:remote -a app-name
  ```
- **Check the Heroku remote URL**
  ```bash
  git remote -v
  ```
- **Remove the Heroku remote**
  ```bash
  git remote remove heroku
  ```

---

These commands should help you manage your Heroku applications efficiently. 🚀

