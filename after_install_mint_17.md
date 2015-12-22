title: Actions After Installed Linux Mint 17.2
tags:
- Linux
- Mint
----
# Actions After Installed Linux Mint 17.2
1. Update package source list with Software Sources
1. Download and install Sogou Pinyin (logout and then config)
1. Install Google Chrome
1. Install curl with apt-get
1. Install virtualenv & Django
1. Install Gvim with spf13

## Install Google Chrome
    wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
    sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
    sudo apt-get update 
    sudo apt-get install google-chrome-stable 
    
## Install virtualenv
    wget https://bootstrap.pypa.io/get-pip.py
    sudo python3 get-pip.py 
    sudo pip install virtualenv

## Configure virtualenv & Install Django
    virtualenv ./virtualenv/py3
    cd virtualenv/py3/
    source bin/activate
    pip install Django
    
## Install Gvim with spf13
    sudo apt-get install vim-gnome 
    curl http://j.mp/spf13-vim3 -L -o - | sh
