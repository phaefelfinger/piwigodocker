# piwigodocker

Docker compose to start a piwigo environment to quickli test some things on local docker setup.

## Setup piwigo

To start a working piwigo gallery run the following commands:

```
git clone https://git.haefelfinger.net/piwigo/piwigodocker.git
cd piwigodocker
docker compose up -d
```

All files gets created within the cloned directory and can be accessed easily from the host machine.

Beware that the mariadb is exposed to localhost on port 3306 and is accessible from tools like mysql workbench or jetbrains datagrip. If you do not like this, remove the ports from the compose file.

After everything started successful, you just enter ``https://localhost:8080`` into your browser.
Complete the setup by entering ``db`` as database host with user ``piwigo`` and password ``Asdfqwer1234`` and ``piwigo`` as database. Choose your admin account and finish the setup.

## Stop piwigo

To stop the setup:

```
cd piwigodocker
docker compose down
```

Stopping will remove the network and the containers but will keep the data in the folders below ``piwigodocker``.

## Start piwigo again

To start the installation again, you just execute the up command again. As all directories still exists, you'll find your installation where you left it.

```
cd piwigodocker
docker compose up -d
```

## Access adminer

To access a little gui for mariadb / mysql, just open a browser and enter ``https://localhost:8081``. The database credentials are the same used for the piwigo setup.