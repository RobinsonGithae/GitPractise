# GitPractise
A repo for learning git.
**## Connecting to your GitHub Account with SSH - STEP BY STEP SETUP WITH GIT BASH**
Open Git Bash

## Generating SSH Keys with SSH-KeyGen
Generate ssh key pair(One public key i.e id_rsa.pub and the  other private key
**ssh-keygen -t rsa -b 4096 -C "xyz@abc.com"** <br>
-t - key algorithm
-b - block size
xyz@abc.com - your email.

## Add the public key string remotely onto your github under settings> Developer Options>SSH

## register your private key with the ssh authentication agent locally on your PC
To add on windows use eval 

eval `ssh-agent -s`

**Why do we need to use eval instead of just ssh-agent**
SSH needs two things in order to use ssh-agent: an ssh-agent instance running in the background, and an environment variable set that tells SSH which socket it should use to connect to the agent (SSH_AUTH_SOCK IIRC). If you just run ssh-agent then the agent will start, but SSH will have no idea where to find it.

## Add the path to the private key location
ssh-add ~/.ssh/ssh2/id_rsa_robinsonprivate_key_personal_github









