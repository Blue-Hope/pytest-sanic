pytest-sanic
============

.. image:: https://travis-ci.org/yunstanford/pytest-sanic.svg?branch=master
    :alt: build status
    :target: https://travis-ci.org/yunstanford/pytest-sanic

.. image:: https://coveralls.io/repos/github/yunstanford/pytest-sanic/badge.svg?branch=master
    :alt: coverage status
    :target: https://coveralls.io/github/yunstanford/pytest-sanic?branch=master


A pytest plugin for `Sanic <http://sanic.readthedocs.io/en/latest/>`. It helps you to test your code asynchronously.

This plugin provides:

* very easy testing with async coroutines
* common and useful fixtures
* test_client for Sanic application
* test_server for Sanic application


-------
Install
-------

.. code::

    pip install pytest-sanic


-----------
Quick Start
-----------

You don't have to load `pytest-sanic` explicitly. pytest will do it for you. Just write tests like,

.. code::
	
	async def test_sanic_db_find_by_id(app):
		"""
		Let's assume that, in db we have,
			{
				"id": "123",
				"name": "Kobe Bryant",
				"team": "Lakers",
			}
		"""
		doc = await app.db["players"].find_by_id("123")
		assert doc.name == "Kobe Bryant"
		assert doc.team == "Lakers"


--------
Fixtures
--------

Some fixtures for easy testing.

``loop``
~~~~~~~~




``unused_port``
~~~~~~~~~~~~~~




``test_server``
~~~~~~~~~~~~~~




``test_client``
~~~~~~~~~~~~~~



-------
Example
-------



-----------
Development
-----------

`pytest-sanic` accepts contributions on GitHub, in the form of issues or pull requests.


Run unit tests.

.. code::

    ./uranium test


---------
Reference
---------

Some pytest plugins:

* `pytest-tornado <https://github.com/eugeniy/pytest-tornado>`
* `pytest-asyncio <https://github.com/pytest-dev/pytest-asyncio>`
* `pytest-aiohttp <https://github.com/aio-libs/pytest-aiohttp>`
