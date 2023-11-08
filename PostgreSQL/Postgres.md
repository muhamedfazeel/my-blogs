# **PostgreSQL**

![Postgres Logo](postgres.png)

## **Postgres Installation**

[Reference Link](https://www.digitalocean.com/community/tutorials/how-to-install-postgresql-on-ubuntu-22-04-quickstart)

1. In order to install any new packages/softwares, check for the updates first:
    ```
    sudo apt update
    ```
2. Install the postgres package and postgres-contrib package for some additional utilities:
    ```
    sudo apt install postgres postgres-contrib
    ```

-   **After installation: default username will be _postgres_ with default role `postgres`**

## **PgAdmin4 Installation**

[Reference](https://www.pgadmin.org/download/pgadmin-4-apt/)

1. Install the public key for the repository, if not done yet:

```
curl -fsS https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo gpg --dearmor -o /usr/share/keyrings/packages-pgadmin-org.gpg
```

2. Create the configuration file for repository:
    ```
    sudo sh -c 'echo "deb [signed-by=/usr/share/keyrings/packages-pgadmin-org.gpg] https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'
    ```
3. Install PgAdmin (Web version and Desktop version):
   `sudo apt install pgadmin4`
4. If you need only the desktop version, use:
    ```
    sudo apt install pgadmin4-desktop
    ```
5. For web version, use:
    ```
    sudo apt install pgadmin4-web
    ```
6. To configure webserver, use:
    ```
    sudo /usr/pgadmin4/bin/setup-web.sh
    ```

## **PostgreSQL Password Reset**

#### **In a case when you are not able to connect to PostgreSQL from PgAdmin, you need to reset your postgres password. In such a case, use the following commands:**

1. Login to postgres using terminal:
    ```
    sudo -u postgres psql
    ```
2. Change your password:
    ```
    \password
    ```
3. Enter new password and confirm the same.
