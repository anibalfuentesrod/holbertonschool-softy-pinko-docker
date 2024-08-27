# use latest version
FROM nginx:latest

# copy the front-end files to the appropriate dir()
COPY . /var/www/html/softy-pinko-front-end

# copy the nginx config file
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf