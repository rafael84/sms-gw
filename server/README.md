Preparing the database:

1. Create a new user

	createuser smsgw -W

2. Allow the user smsgw to create a new database

	psql -U postgres
	alter user smsgw createdb;

3. Create the database

	createdb -O smsgw -h localhost -U smsgw -W -E utf8 smsgw


Synchronizing the database with django:

    python  manage.py syncdb
