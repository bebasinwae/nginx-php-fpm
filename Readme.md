# Docker PHP-FPM 7.3 and Nginx on Ubuntu 16.04

My personal PHP 7.3 image for laravel and PHP projects. See the docker file for more info.

## Usage

Clone Repository:

	git clone https://github.com/bebasinwae/nginx-php-fpm.git

Build The Docker camtaimer:

	cd nginx-php-fpm
	docker build -t nginx-php73 .

Start the Docker container:

	docker run -d -p 8080:80 nginx-php73

See the PHP info on http://localhost:8080.

Or mount your own code to be served by PHP-FPM & Nginx

	docker run -p 80:8080 -v ~/public_html:/var/www/html nginx-php73
