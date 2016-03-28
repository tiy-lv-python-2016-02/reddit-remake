## Description

Create an interface in Django to the [MovieLens dataset](http://grouplens.org/datasets/movielens/).

## Normal Mode

### Models
You will need to create the following models for the dataset:

Movie:
* id
* title
* genre

Rater:
* id
* gender
* age
* occupation
* zip_code

Rating:
* id
* rater (to Rater)
* movie (to Movie)
* rating
* timestamp

### Views

* The top 20 movies rated. This list of movies should have their average rating,
  and each movie listed should have a link to its individual page.

* Each individual movie. This page should have the movie, its average rating,
  and each person who rated it. The list of people should have the rating
  with each person and should have a link to that person's page.

* Each individual user. This page should have their demographic data, and a
  list of all movies they've rated, with the rating they gave it. Each movie
  listed should have the rating they gave it beside it and should have a link
  to that movie's page.

## Hard Mode

### Migrate the system over to your local postgres database.  

This will be similar
 to what needs to happen with a new production database.  You can find the information on this
[here](https://docs.djangoproject.com/en/1.8/ref/settings/#std:setting-DATABASES).  The second code example shows
the configuration for postgres.  You will need to create the database like last week
then run migrations on it. 

### Import data
Take [the script to turn MovieLens 1M data into fixtures](https://github.com/tiy-lv-python-2016-02/django-movies-part-2/blob/master/convert_ml_1m_data.py)
and modify it to turn your CSV data into fixtures, then load those fixtures
with `python manage.py loaddata <fixture_file>`.

## External Links
* [Django URLs](https://docs.djangoproject.com/en/1.8/topics/http/urls/)
* [Django Views](https://docs.djangoproject.com/en/1.9/topics/http/views/)
