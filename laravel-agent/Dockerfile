FROM jenkins/ssh-agent:jdk21
# install dependencies for laravel
RUN apt update && apt install -y git php8.2 php-xml
RUN apt install php-curl php-mbstring php-zip php-bcmath php-gd php-mysql php-pdo php-tokenizer php-openssl php-fileinfo php-dom phpsimplexml php-xmlreader npm
RUN apt install npm -y

RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
RUN php -r "if (hash_file('sha384', 'composer-setup.php') === 'c8b085408188070d5f52bcfe4ecfbee5f727afa458b2573b8eaaf77b3419b0bf2768dc67c86944da1544f06fa544fd47') { echo 'Installer verified'.PHP_EOL; } else { echo 'Installer corrupt'.PHP_EOL; unlink('composer-setup.php'); exit(1); }"
RUN php composer-setup.php
RUN php -r "unlink('composer-setup.php');"


