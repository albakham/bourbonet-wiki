# Seafile

## Update Seafile

First stop seafile services

- `systemctl stop seafile && systemctl stop seahub`

Go to https://www.seafile.com/en/download/ and download latest server edition

- `cd /opt/seafile`
- `wget https://s3.eu-central-1.amazonaws.com/download.seadrive.org/seafile-server_8.0.2_x86-64.tar.gz`

Extract it

- `tar -xf seafile-server_*`

Now check for additionnal upgrade notes on https://manual.seafile.com/upgrade/upgrade/

Run the upgrade script

- `cd seafile-server-8.0.2/upgrade`
- `./upgrade_7.1_8.0.sh`

Change permissions

- `chown -R seafserver. *`

Start the services back again

- `systemctl start seafile && systemctl start seahub`
