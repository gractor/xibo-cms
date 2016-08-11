# install
sudo apt-get update

sudo apt-get install apache2 mysql-server php5 php5-curl php5-gd php5-mysql php5-mcrypt


sudo mv xibo-cms-1.7.8/ /var/www/html/xibo-server

cd /var/www/html/xibo-server

sudo chown www-data:www-data -R /var/www/html/xibo-server

sudo mkdir /media/xibo-library

sudo chown www-data:www-data -R /media/xibo-library


##locate mcrypt.ini
sudo nano /etc/php5/mods-available/mcrypt.ini

sudo ln -s /etc/php5/mods-available/mcrypt.ini /etc/php5/cli/conf.d/20-mcrypt.ini

sudo ln -s /etc/php5/mods-available/mcrypt.ini /etc/php5/apache2/conf.d/20-mcrypt.ini

sudo service apache2 restart

 sudo php5enmod mcrypt
 
