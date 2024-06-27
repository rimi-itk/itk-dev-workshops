# SQL for begyndere

``` shell
# Start the show
docker compose up --pull always --detach
# Connect to database
docker compose exec mariadb mariadb --user=db --password=db db
```

Talk to the database:

``` shell
# Interactively
docker compose exec mariadb mariadb --table --user=db --password=db db
```

``` shell
docker compose exec --no-TTY mariadb mariadb --table --user=db --password=db db <<< 'SHOW TABLES'
docker compose exec --no-TTY mariadb mariadb --table --user=db --password=db db < examples/select-customers.sql
```
