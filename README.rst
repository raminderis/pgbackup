pgbackup
========

CLI for backing up remote PostgreSQL Databases and store the backup file either locally or to AWS S3 service.

Preparing the Development
-------------------------

1. Ensure ``python3.6``, ``pip3.6`` and ``pipenv`` are installed.
2. Clone repository: ``git clone git@github.com:raminderis/pgbackup``
3. ``cd`` into the repository
4. Fetch development dependencies ``make isntall``
5. Activate virtualenv: ``pipenv shell``

Usage
-----

Pass in a full database URL, the storage driver, and the destination.

S3 Example w/ bucket name:

::

    This is a preformatted text block.
    $ pgbackup postgres://bob@example.com:5432/db_one --driver s3 backups-bucket

Local Example w/ local path:

::

    $ pgbackup postgres://bob@example.com:5432/db_one --driver local /var/local/db_one/backups/dump.sql

Running Tests
-------------

Run tests locally using ``make`` if virtualenv is active:

::

    $ make

If virtualenv isn't active then use:

::

    $ pipenv run make
