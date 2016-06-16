# Cassandra Data Manager

Tool for installing cassandra datasets.  This is not a bulk loader.  It is intended to be used as a tool for learning and educational purposes.

This repository contains the cdm tool only, and has references to repositories which are independently maintained.

## Installation

    pip install cassandra-dataset-manager

The project is still under heavy development, a lot is changing very quickly.

## Quickstart

Let's install the movielens-small dataset.  It's a quick download at just a few MB and gives you a database you can play with.

    cdm update
    cdm install movielens-small

Open the Cassandra shell:

    cqlsh -k movielens_small
    desc tables;
    select * from movies limit 10;

Options are all available at `cdm help`

I encourage you to read through the [documentation](http://cdm.readthedocs.org/en/latest/).

### Note for OS X users

You may experience an error message like this during install

```
OSError: [Errno 1] Operation not permitted: '/var/folders/x_/g0gbsrv93bscl1z40vbqt7w00000gp/T/pip-CBMkcc-uninstall/System/Library/Frameworks/Python.framework/Versions/2.7/Extras/lib/python/six-1.4.1-py2.7.egg-info'
```    

A simple and quick solution is to install Python with [Homebrew](http://brew.sh/)

```
brew install python
```

See this [thread](http://stackoverflow.com/q/29485741/1360888) for more information.
