# GitLab Docker Demo
A demo showing GitLab running with
 * GitLab Server
 * GitLab Runners
   * Shell executor, for building docker images
   * Docker executor, for building web projects
 * Private Docker Registry

# Dependencies
Before running this, install
 * Docker
 * Docker Compose

# Running
**Start gitlab**

    docker-compose -f docker-compose.gitlab.yml up -d

Go to http://127.0.0.1:8080 and login as root/5iveL!fe.

**Add the registration token**
 * Go to http://127.0.0.1:8080/admin/runners and note the registration token.
 * Add the token to gitlab_runner.env
 
    REGISTRATION_TOKEN=XXXXXXXXXXXXXXXXXXXXX

**Start the runner**

    docker-compose -f docker-compose.runners.yml up -d

# License
This demo is distributed using the MIT License. For more information please 
see LICENSE.

# Author
 * Sean Gillespie <sean@mistersg.net>

# Acknowledgements
This demo uses several open source tools
 * GitLab
 * Docker
 * Docker Compose
