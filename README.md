# Boilerplate for Flask Application

This repo provide some basic configuration for development of a new Flask Project.

It's based on the official documentation, adopting the pratices rules by the responsable
team.

The project provide some basic registration and authentication.

## Basic Configuration

It's necessary Python 3+, and recomended virtualenv, or venv package.

First create a folder, and inside folder clone this repo thus create the virtualenv:

```bash
# Create the folder
mkdir flask-project
cd flask-project

# Clone the repo
git clone https://github.com/gabrielbalog/flask-boilerplate

# Create the virtualenv
python3 -m venv venv

source venv/bin/activate
```

Next it's needed to declare some environment variables to run flask properly:

```bash
export FLASK_APP=flaskr
export FLASK_ENV=development
```

Now it's just call flask with the command run:

```bash
flask run
```

You should be able to access http://127.0.0.1:5000/hello, and see the "Hello, World" priting out.

## Initializing the Database

For default the project it's configured to run on a SQLite file, so before access any page, run:

```bash
flask init-db
```

It'll automatically create the database and the Auth table.

## Tests

The project have some tests already for covering the factory and the auth.

To run the tests, use the command below:

```bash
pytest
```

For the coverage, use the command below:

```bash
coverage report
```

## Plans for the future

I've plan to update this repo using the SQLAlchemy Extension, besides running raw SQL.
I also plan to convert the models into class Models, so that behavior like a Flask Application
with ORM.

Integration with Postgres it's in my plan, also.

And, finally, but not least, how to deploy on Heroku and some VPS.