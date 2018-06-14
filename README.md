Karma Core
==============
* [Getting Started](#getting-started)
* [License](#license)

Karma Core is the Karma blockchain implementation and command-line interface.

Visit [karma.red](https://karma.red/) to learn about Karma.

**NOTE:** The official Karma git repository location, default branch, and submodule remotes were recently changed. Existing
repositories can be updated with the following steps:

    git remote set-url origin https://github.com/Karma-blockchain/karma-core
    git checkout master
    git remote set-head origin --auto
    git pull
    git submodule sync --recursive
    git submodule update --init --recursive

**Build and launch the docker container**

    git clone https://github.com/Karma-blockchain/karma-core
    cd karma-core
    git checkout master
    docker build -t karma_node:m0.52 .
    docker run -v $(pwd)/docker/default_config.ini:/var/lib/bitshares/config.ini -d --name karma_node_testnet_19 -p 5719:5719 -p 8090:8090 karma_node_0:m0.52

 
License
-------
Karma Core is under the MIT license. See [LICENSE](https://github.com/Karma-blockchain/karma-core/blob/master/LICENSE.txt)
for more information.
