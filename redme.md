sudo apt-get update
sudo apt-get upgrade
sudo apt-get install -y python3-pip
sudo apt-get install -y python3-dev libxml2-dev libxslt1-dev zlib1g-dev libsasl2-dev libldap2-dev build-essential libssl-dev libffi-dev libmysqlclient-dev libjpeg-dev libpq-dev libjpeg8-dev liblcms2-dev libblas-dev libatlas-base-dev
sudo apt-get install -y npm
sudo ln -s /usr/bin/nodejs /usr/bin/node
sudo npm install -g less less-plugin-clean-css rtlcss
sudo apt-get install -y node-less
sudo apt-get install -y postgresql
sudo su - postgres
createuser --createdb --username odoo --no-createrole --superuser --pwprompt 123456
exit
sudo adduser --system --home=/opt/odoo --group odoo
sudo wget https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.bionic_amd64.deb
   sudo wget http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1f-1ubuntu2_amd64.deb
   sudo dpkg -i libssl1.1_1.1.1f-1ubuntu2_amd64.deb
   sudo apt-get install -y xfonts-75dpi
   sudo dpkg -i wkhtmltox_0.12.5-1.bionic_amd64.deb
   sudo apt install -f
 dpkg -i <path_to_installation_package> # this probably fails with missing dependencies
 apt-get install -f # should install the missing dependencies
 dpkg -i <path_to_installation_package>
sudo nano /etc/odoo/odoo.conf
{ [options]
   ; This is the password that allows database operations:
   ; admin_passwd = admin
   db_host = localhost
   db_port = 5432
   db_user = odoo
   db_password = 123456
   addons_path = /opt/odoo/addons
   default_productivity_apps = True
   logfile = /var/log/odoo/odoo.log
   proxy_mode=True
}
systemctl enable odoo
systemctl restart odoo
