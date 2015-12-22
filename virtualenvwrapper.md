# Virtualenvwrapper tutorial
## Install
    sudo pip install virtualenvwrapper

## Configuration
Add following codes into shell profile, such as ~/.zshrc

    # virtualenvwrapper configuration
    # use python3 instead of python
    export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
    # specify virtualenv path
    export VIRTUALENVWRAPPER_VIRTUALENV=/usr/local/bin/virtualenv
    # virtualenvs path
    export WORKON_HOME=$HOME/virtualenv
    # projects path
    export PROJECT_HOME=$HOME/Projects
    # activate virtualenvwrapper on startup shell
    source /usr/local/bin/virtualenvwrapper.sh

After that, execute `source ~/.zshrc` to make configuration work.

## Use virtualenvwrapper
### Create virtualenv
    mkvirtualenv envname
Then it will create a virtualenv in the $WORKON_HOME path
### Activate virtualenv
    workon envname
use `deactivate` to exit virtualenv
### List all virtualenv
    lsvirtualenv
### Execute command on all virtualenvs
    allvirtualenv command
such as:

    # update pip for all virtualenvs
    allvirtualenv pip install -U pip
