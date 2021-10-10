1. Generate random 32 byte APP_KEY and set it in `.app_key` file:
```sh
head /dev/urandom | LC_ALL=C tr -dc 'A-Za-z0-9' | head -c 32 > .app_key
```
2. Set site owner email id in `.site_owner` file
3. Set database password in `.db_password` file
