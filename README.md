# piwigodocker

Docker compose to start a piwigo environment to quickli test some things on local docker setup.

To start a working piwigo gallery run the following commands:

```
git clone https://git.haefelfinger.net/piwigo/piwigodocker.git
cd piwigodocker
docker-compose up -d
```

All files gets created within the cloned directory and can be accessed easily from the host machine.

Beware that the mariadb is exposed to localhost on port 3306 and is accessible from tools like mysql workbench or jetbrains datagrip.
