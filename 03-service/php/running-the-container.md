# To run normally
    docker run -d -it --name php -p 8000:8000 php-simple

# To run modified
    docker run -d -it --name php -p 8000:8000 php-simple /site/info.php
