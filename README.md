# Wellcome to CloudBank

It is the most popular and original CloudCoin python script. The code is exceptionally portable and has been used successfully on a very broad range of ubuntu systems and hardware.

## Contact

[![Gitter](https://img.shields.io/gitter/room/nwjs/nw.js.svg)](https://gitter.im/cloudbank-github/)
[![GitHub Issues](https://img.shields.io/badge/open%20issues-0-yellow.svg)](https://github.com/omgbbqhaxx/CloudBank/issues)

- Chat in [cloudbank-github channel on Gitter](https://gitter.im/cloudbank-github).
- Report bugs, issues or feature requests using [GitHub issues](issues/new).



## Getting Started

The CloudBank Documentation site hosts the **[CloudBank homepage](http://cloudbankproject.com/)**, which
has a Quick Start section.

Operating system | Status
---------------- | ----------
Ubuntu and macOS | [![TravisCI](https://img.shields.io/badge/build-passing-brightgreen.svg)](https://travis-ci.org/cloudbank/cloudbank-github)
Windows          | [![AppVeyor](https://img.shields.io/badge/build-passing-brightgreen.svg)](https://ci.appveyor.com/project/cloudbank/cloudbank-github)


```shell
sudo apt-get update -y && sudo apt-get upgrade -y && sudo apt-get install vim -y && sudo apt-get install python-dev -y && sudo apt-get install libevent-dev -y &&  sudo apt-get install python-virtualenv -y && apt-get install git -y
```



## Install python last version..

```shell
sudo add-apt-repository ppa:fkrull/deadsnakes
sudo apt-get update
sudo apt-get install python3.4
sudo apt-get install python3-pip
pip install --upgrade virtualenv
```

## Other configurations..

```shell
virtualenv -p python3 venv
pip install pytz
pip install netifaces
pip install django
pip install gunicorn
pip install tornado
pip install twisted[tls]
pip install aioredis
pip install pycrypto
pip install autobahn[twisted]
pip install bson
pip install ecdsa
pip install websocket-client
pip install pipenv
pipenv install requests
```


## Circus: A Process & Socket Manager configurations
The simplest way to install it is to use pip, a tool for installing and managing Python packages:
```shell
pip install circus
pip install circus-web
pip install chaussette
```

example.ini
```shell
[watcher:startserver]
cmd = /opt/venv/bin/gunicorn_start
numprocesses = 1
[watcher:starttcpconnections]
cmd = python /opt/venv/cloudbank/server.py
numprocesses = 1
```

The file is then passed to circusd:
```shell
circusd example.ini
```

You can exist from program if already running.
```shell
circusctl quit --waiting
```


## License

[![License](https://img.shields.io/github/license/ethereum/cpp-ethereum.svg)](LICENSE)

All contributions are made under the [GNU General Public License v3](https://www.gnu.org/licenses/gpl-3.0.en.html). See [LICENSE](LICENSE).
