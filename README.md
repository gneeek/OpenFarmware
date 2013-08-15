OpenFarmware
============

demonstration code for monitoring an Aquaponic or Hydroponic Garden

Getting Started
===============

This is a demonstration, prototype only system.  Requires specific hardware to use, which is not yet documented.  

There is an arduino script, used to collect data from a set of sensors, and transmit it wirelessly through an XBee radio.
GardenMonitor is a python module that connects to another XBee radio and collects this data. 

GardenMonitor is designed to be run using pip + virtualenv + virtualenvwrapper.
Tested with python 2.7.3.

To get up and running:

* install pip (if it is not already there)
* install virtualenv

::

    $ pip install virtualenv

* install virtualenvwrapper

::

    $ pip install virtualenvwrapper

* add some environment variables to your shell startup script, such as .bashrc.  

This allows pip and virtualenv and virtualenvwrapper to do their magic.
The exact location of the virtualenvwrapper.sh script might be different on your system.

::

    export WORKON_HOME=$HOME/Envs
    export PIP_VIRTUALENV_BASE=$WORKON_HOME
    export PIP_RESPECT_VIRTUALENV=true
    export PROJECT_HOME=$HOME/UrbanStream/projects
    source /usr/local/bin/virtualenvwrapper.sh

* create and configure the virtualenv, and add source code

::

    export WORKON_HOME=~/Envs
    mkdir -p $WORKON_HOME
    source /usr/local/bin/virtualenvwrapper.sh
    mkproject openfarmware
    mkvirtualenv openfarmware
    setvirtualenvproject $VIRTUAL_ENV $(pwd)
    cd ..
    git clone 
