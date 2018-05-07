# FSJS Initial Setup

**Outline**

* Install/Setup git
* Install/Setup nodejs/npm || nvm
* Install/Setup mongodb || docker || mLab

**Legend**
* Difficulty of each method is indicated with :one: :two: :three: :four: :five:
* Recommended method is indicated with :white_check_mark: 

# Install/Setup git 
## macOS X :one:
1. Download https://git-scm.com/download/mac
2. Install the .dmg

## windows :one:
1. Download https://git-scm.com/download/win
2. Run the setup wizard .exe
_I recommend picking add commands to windows command line so that cmd and git bash have the same functions_

# Install/Setup nodejs/npm || nvm
## nodejs/npm Install :white_check_mark:
### macOS X :one:
1. Download https://nodejs.org/dist/v8.11.1/node-v8.11.1.pkg
2. Run the setup wizard .pkg file

### windows :one:
1. Download https://nodejs.org/dist/v8.11.1/node-v8.11.1-x64.msi or https://nodejs.org/dist/v8.11.1/node-v8.11.1-x86.msi
2. Run the setup wizard .exe file

## nvm
This tool will let you pick different versions of node which is helpful if you are doing a lot of node apps
### macOSX :three:
1. Open terminal
2. Run the following command `curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash`
3. Verify by opening terminal and running `command -v nvm`

### windows :three:
1. Download the latest installer https://github.com/coreybutler/nvm/releases
2. Run the setup wizard
3. Verify by running `nvm use 4.4.0` in git bash or command line


# Install/Setup mongodb || docker || mLab
## mongodb Community Edition :three:
### general
https://docs.mongodb.com/manual/installation/

### macOS X
Follow the directions on the follow site
https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/

### windows
Follow the directions on the follow site
https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/

### both
These will be your settings for connecting to the db, example:
```
MONGODB_URI=mongodb://localhost:<random port>/SampleDB
```

## docker :three:
Make sure to install Kitematic
### general
https://docs.docker.com/install/

### macOS X
https://docs.docker.com/docker-for-mac/install/

### windows
https://docs.docker.com/docker-for-windows/install/

### both
1. Once you have the install complete you will open Kitematic and search for `mongo`
2. Click Create on the docker container with Official and mongo  

![docker container image](https://lh3.googleusercontent.com/jDcFAjda3cufbKF-dl2fjVHkdbgG1tnqPctcho8pmyYs-0_GvTAT61QT8BrbOGb8xJZAHULCByg0mbmyrsmQVlvkXKst8QWiqgjRHdFYzSzhbGpacH7tikWlXOA92zXj3Sx0Z42yvvQEtL9tIHN7bj7njhtkLo6TjH8aR3qqAGd7_mdPdVSXfHk3phshyaWwsEJ5m9HPj8eFB49bFqgAOoF09ZORAyxED8EM-hAKNH5cnz1VHfO7iP7nrqSFWBjDIUzka3tUA8z7GzrJxraFS8sAgthkBjTbCpG_CkeVxIZMsN6MMFpH4oqs1ca63bXgcD2dVpjjbJzwaFm-HNnJ99IB4DwbbI_smYUg-Lhtp_N8AIUkTtN6HTWMjLt_LvZKvMyLXrZPv-JKoHq2jKavm1P4gNk69DjCtTLjTyz7b9Lg4UifLJFqBSZFff3OTsqCozCX70bIIv80Fadpl5sgTJYmNMU_axhIplTSI_6gqCCWbZiFyeQj21798atoHwEVPkMudhWOdwL_f9IArIUPdSM2eelC2Dn_hSKcXQnU-uXJtAhLb58B-AW49EHGsM67p3lPFU5Na0P8XS36qrrwVLGb3mq_9UalnTXnyfDN=w268-h140-no "docker container")

3. Now start the container
4. Go to settings -> Hostname/Ports
5. These will be your settings for connecting to the db, example:
```
MONGODB_URI=mongodb://localhost:<random port>/SampleDB
```
 
## mLab :one: :white_check_mark:
### both
1. Head over to [mLab](https://mlab.com/signup/) and signup/login
2. Create a new MongoDB deployment
3. Pick Amazon Web Services and Free(Sandbox)
4. Give your db a name, example `fsjs-db1`
5. Click the new deployment (give it a second)
6. Create a new collection or do it via code
7. At the top you will see the connection settings, example:
```
To connect using a driver via the standard MongoDB URI (what's this?):

mongodb://<dbuser>:<dbpassword>@ds1111111.mlab.com:17360/fsjs-db1
```

This will go into your node project!

_See it was as Easy as ABC123_