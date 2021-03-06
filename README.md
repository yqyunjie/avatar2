[![PyPI version](https://badge.fury.io/py/avatar2.svg)](https://badge.fury.io/py/avatar2)
[![Build Status](https://travis-ci.org/avatartwo/avatar2.svg?branch=master)](https://travis-ci.org/avatartwo/avatar2)

Welcome to avatar², the target orchestration framework with focus on dynamic
 analysis of embedded devices' firmware!

Avatar² is developed and maintained by [Eurecom's S3 Group](http://s3.eurecom.fr/).

# Building

Building avatar² is easy!

First, make sure that all the dependencies are present:

```
sudo apt-get install python-pip python-setuptools python-dev cmake
```

Afterwards, use python-pip to install avatar2:

```
pip install avatar2
```

Now you are all ready to go. Additionally, if you want to install specific
target entpoints, please run the avatar2-installer, which tries to fetch and
install the endpoints automatically.

```
python -m avatar2.installer
```

### Building manually

Avatar² can also be built manually.
The following three commands are enough to install the core.
```
$ git clone https://github.com/avatartwo/avatar2.git
$ cd avatar2
$ sudo python setup.py install
```
Afterwards, the different target endpoints can be built, such as QEmu or PANDA.
For doing so, we are providing build-scripts for Ubuntu 16.04 - while other
distributions are not officially supported (yet), the scripts are known to
work with slight modifications on other distributions as well.
```
$ cd targets
$ ./build_*.sh
```

**Please Note:** These scripts add the restricted repository to
`/etc/apt/sources.list` for fetching the dependencies. If you are not comfortable
with this, please consider building avatar² in a VM/Container or install the 
dependencies manually and adjust the scripts.

# Getting started
For discovering the power of avatar² and getting a feeling of its usage,
we recommend highly checking out the 
[handbook](https://github.com/avatartwo/avatar2/tree/master/handbook) here on
github.
Additionally, a documentation of the API is provided 
[here](https://avatartwo.github.io/avatar2-docs/) and some exemplary
avatar²-scripts can be found 
[here](https://github.com/avatartwo/avatar2-examples).
Additionally, another good way to get started with avatar² is to read the official
[avatar² paper](http://s3.eurecom.fr/docs/bar18_muench.pdf) or to watch the
[34c3-talk](https://media.ccc.de/v/34c3-9195-avatar).

For further support or follow-up questions, feel free to contact us via IRC
in #avatar2 on freenode, or to send a mail to avatar2 [at] lists.eurecom.fr, 
our public mailing list.

Additionally, you can subscribe to the list 
[here](https://lists.eurecom.fr/sympa/subscribe/avatar2).


# Publications
1. M. Muench, D. Nisi, A. Francillon, D. Balzarotti. "Avatar²: A Multi-target Orchestration Platform." Workshop on Binary Analysis Research, San Diego, California, February 2018.
    - [Paper](http://s3.eurecom.fr/docs/bar18_muench.pdf) - [Code](https://github.com/avatartwo/bar18_avatar2)
2. M. Muench, J. Stijohann, F. Kargl, A. Francillon, D.avide Balzarotti. "What You Corrupt Is Not What You Crash: Challenges in Fuzzing Embedded Devices." Network and Distributed System Security Symposium, San Diego, California, 2018.
    - [Paper](http://www.s3.eurecom.fr/docs/ndss18_muench.pdf) - [Code](https://github.com/avatartwo/ndss18_wycinwyc)
