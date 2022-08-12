# Run the container
    docker run -d --rm --name mariadb -p 3306:3306 -e MARIADB_PASSWORD=bananas  mariadb

# Logon to the DB
    mysql -h127.0.0.1 -P 3306 -utestuser -pbananas

# Get root password
    docker logs mariadb | grep "GENERATED ROOT PASSWORD"