# oscommerce 2.3.4

## Usage
1. Unpack an oscommerce installation into this directory, such that the `catalog` directory is available.
2. Create a `.env` file, as described below.
3. Edit the working-directory defined within `oscommerce.service`.
4. Create a symlink from `/etc/systemd/system/oscommerce.service` to the `oscommerce.service` file. 
5. Reload systemd with `systemctl daemon-reload`.
6. Now run osCommerce `systemctl start oscommerce.service`.
7. You will now have an osCommerce instance running somewhere within your 172.x.0.x network, on port 2015. 

## Who is this project intended for
Mostly me. Didn't want the hassle of creating a new clean osCommerce instance every time.

## .env file
The following variables are required:
- `MYSQL_ROOT_PASSWORD`
- `MYSQL_PASSWORD` (for the `osc` user)

The following variables are optional:
- `VIRTUAL_PATH` (the part of the URL after the hostname)

