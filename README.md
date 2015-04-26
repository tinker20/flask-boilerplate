===============================
tinnker-boilerplate
===============================

A boilerplate which helps you to build websites in minutes. This boilerplate is designed for people who believe in DRY principle.

Usage:

Install pip via terminal - wget https://bootstrap.pypa.io/get-pip.py

Now run $python get-pip.py via the terminal
The above command installs pip on your system.

Now you can install all the dependencies by pip install -r requirements.txt

Before that make sure you have created a virtualenv, because all the dependencies must be in a separate environment.


Quickstart
----------

First, set your app's secret key as an environment variable. For example, example add the following to ``.bashrc`` or ``.bash_profile``.

.. code-block:: bash

    export FLASKSTARTER_SECRET='something-really-secret'


Then run the following commands to bootstrap your environment.


::

    git clone https://github.com/tinker20/boilerplate-flask
    cd FlaskStarter
    pip install -r requirements.txt
    python manage.py server

You will see a pretty welcome screen.

Once you have installed your DBMS, run the following to create your app's database tables and perform the initial migration:

::

    python manage.py db init
    python manage.py db migrate
    python manage.py db upgrade
    python manage.py server



Deployment
----------

In your production environment, make sure the ``FLASKSTARTER_ENV`` environment variable is set to ``"prod"``.


Shell
-----

To open the interactive shell, run ::

    python manage.py shell

By default, you will have access to ``app``, ``db``, and the ``User`` model.


Running Tests
-------------

To run all tests, run ::

    python manage.py test


Migrations
----------

Whenever a database migration needs to be made. Run the following commmands:
::

    python manage.py db migrate

This will generate a new migration script. Then run:
::

    python manage.py db upgrade

To apply the migration.

For a full migration command reference, run ``python manage.py db --help``.
