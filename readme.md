# Welcome to the Anythink Market repo

To start the app use Docker. It will start both frontend and backend, including all the relevant dependencies, and the db.

Please find more info about each part in the relevant Readme file ([frontend](frontend/readme.md) and [backend](backend/README.md)).

## Development

When implementing a new feature or fixing a bug, please create a new pull request against `main` from a feature/bug branch and add `@vanessa-cooper` as reviewer.

## First setup

# Docker Ubuntu

Got to docker docs! 

Here:
https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository

Linux can be a bit more challenging than other OS's, so go slow and follow the docs precisely! You may have to venture out and update something (Like a PPA)

SAMPLE CASE:

    E: The repository 'http://ppa.launchpad.net/armagetronad-dev/ppa/ubuntu bionic Release' does not have a Release file. 
    N: Updating from such a repository can't be done securely, and is therefore disabled by default. 
    N: See apt-secure(8) manpage for repository creation and user configuration details.

to fix this you will need to use:

    sudo apt-add-repository -r ppa:armagetronad-dev/ppa

    *note the ppa is in our error

then:

    sudo apt update -q

After a complete installation, we need to check our versions and make sure we are up-to-date!

    docker -v
    docker-compose -v

these commands will give you a running version.

Then, inside our git repo. run:

    docker-compose up

This will start building everything and when it is complete, run: http://localhost:3000/api/ping

Lastly, when our backend is up and running. Create a new account at http://localhost:3000/api/ping

For all the next quests
run all scripts in one of the containers craeted by 
    docker-compose up

Use
    docker exec

to run commands on a running container.