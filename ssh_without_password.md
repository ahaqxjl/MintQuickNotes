title: SSH without password
tags:
- SSH
- Linux
------
**All steps are on local machine**

# Step 1. gen ssh key
    ssh-keygen
# Step 2. pass key to server
    ssh-copy-id user@serverhost
# Test
    ssh user@serverhost