PKP XML Parsing Service
=======================
Build status
------------
[![Build Status](https://travis-ci.org/MichaelThessel/xmlps.png?branch=master)](https://travis-ci.org/MichaelThessel/xmlps)

Installation
------------
* Copy the source

```
# git clone https://github.com/MichaelThessel/xmlps.git
# cd xmlps
```
* Install the dependencies

```
# php composer.phar self-update
# php composer.phar install
```
* Configure the environment

```
cp config/autoload/local.php.dist config/autoload/local.php
```
* Change local.php according to your environment

* Initialize the database

```
    # vendor/doctrine/doctrine-module/bin/doctrine-module  orm:schema-tool:update --force
```
* Run the unit tests (optional)

```
    # ./unittest.sh
```

Technical notes
---------------
* SASS compilation, CSS and Javascript compression & unification is done using Guard (http://guardgem.org)
* After making changes to Javascript (javascript/) or style files (style/scss/) recompile/recompress the style and Javascript files by running

```
    # guard
```

Module Description
------------------
* User
 * Authentication [X]
 * Registration [X]
 * New password [X]
 * Lost password retrieval
* Admin
 * Confirm registrations [X]
 * Set a user's document conversion rate [X]
 * Delete user [X]
 * Edit User [X]
 * System log viewer [X]
* Manager
 * Receives conversion jobs
 * Queues jobs for individual workers
