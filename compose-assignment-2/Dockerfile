# create your custom drupal image here, based of official drupal
FROM drupal:9

# RUN the apt package manager to install git
# Cleanup after the apt install
RUN apt-get update && apt-get install -y git \
    && rm -rf /var/lib/apt/lists/*

# Change the working directory to the /var/www/html/themes
WORKDIR /var/www/html/themes

# Use git to clone the theme
RUN git clone --branch 8.x-4.x --single-branch --depth 1 https://git.drupalcode.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap

# Change the working directory back to its default 
WORKDIR /var/www/html




