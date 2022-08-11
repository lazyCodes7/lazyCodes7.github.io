+++ 
draft = false
date = 2022-06-04T14:56:36+05:30
title = "Week-2 (Community Bonding) 27th May - 3th June"
description = "Setting up CWRU and HPC"
slug = ""
authors = ["Rishab Mudliar"]
tags = []
categories = ["Google Summer of Code"]
externalLink = ""
series = []
+++

# This week
## CWRU Accounts
The first thing that happened this week was that we got our CWRU Gmail accounts. 

## HPC Setup
After this it was time to setup CWRU's HPC(High Performing Cluster). The steps for that are following.

1. First setup CWRU's VPN by following the guide [here](https://sites.google.com/case.edu/techne-public-site/cwru-hpc-orientation/access-cwru-hpc-via-vpn?authuser=0). Make sure that Duo is setup as a 2FA option as each time a connection to the VPN occurs a subsequent push notification is sent to Duo Mobile.

2. Next we run the following ssh command to login to HPC. Here abc123 would be your username provided. And the -vv option denotes verbose as it helps in understanding what might be happening while it is connecting to the domain.

```
ssh -vv abc123@rider.case.edu
```


3. Normally it will ask your passphrase that was used while setting up CWRU account. Once you enter this you are in!

4. After this we can simply relocate to the following point to do whatever we want(not bad things though;p)

```
cd /mnt/rds/redhen/gallina/home/abc123
```

5. We are also required to set appropriate permission on directories. The command for that would be 'chmod'.Here the number is the permission we want and 'myworkspace' is the directory.

```
chmod 600 myworkspace
```

## Keys
After playing around for a bit we were also instructed to install Professor Mark Turner's public key in order to enable ssh login without passphrase I assume.

1. Login using the previous steps.
2. Create an .ssh directory.
```
mkdir .ssh
cd .ssh
```
3. Next create and write the public keys to a file called authorized_keys file.
```
nano authorized_keys
\\ Write your keys once the editor opens. Press ctrl+o, enter, ctrl+x and you are done
```

4. You are done and anyone who has private key in our case Mark would be able to login;)

# Next week
We are finally going to have a meet up so yay!
