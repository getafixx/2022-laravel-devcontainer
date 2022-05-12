# From official php image.
FROM php:8.0-cli


# Create a user group and account under id 1000.
RUN addgroup -g 1000 -S vsuser && adduser -u 1000 -D vsuser -G user
# Install quality-of-life packages.

RUN apt-get update

RUN apt-get install --no-cache -y \
    git unzip vim wget libmcrypt-dev libreadline-dev \
    bash-completion iputils-ping build-essential git-flow \
    ssh dos2unix ssmtp rsync software-properties-common \
    bash curl git vim

RUN add-apt-repository ppa:ondrej/php
RUN apt-get update

RUN apt-get install -y --fix-missing php8.0 php8.0-curl php8.0-gd php8.0-mbstring \
    php8.0-zip php8.0-mysql php8.0-xml php8.0-fpm php8.0-imagick \
    php8.0-tidy php8.0-intl \
    php8.0-cli php8.0-common php8.0-cgi php8.0-xdebug \
    php-pear php8.0-gmp php8.0-bcmath php-soap php8.0-sqlite3     

run apt-get --no-cache nodejs npm

RUN sed -i 's/short_open_tag = Off/short_open_tag = On/' /etc/php/8.0/fpm/php.ini
RUN sed -i 's/post_max_size = 8M/post_max_size = 50M/' /etc/php/8.0/fpm/php.ini
RUN sed -i 's/upload_max_filesize = 2M/upload_max_filesize = 50M/' /etc/php/8.0/fpm/php.ini


#RUN apk add --no-cache bash curl git vim
# Install composer for php deps.
RUN apk add --no-cache composer
# Install postgres pdo driver.

# Install redis driver.
#RUN mkdir -p /usr/src/php/ext/redis; \
#    curl -fsSL --ipv4 https://github.com/phpredis/phpredis/archive/5.3.4.tar.gz | tar xvz -C "/usr/src/php/ext/redis" --strip 1; \
#    docker-php-ext-install redis
# Install nodejs and npm for frontend.
RUN apk add --no-cache nodejs npm
# Prevent container from exiting early.
CMD ["sleep", "infinity"]
