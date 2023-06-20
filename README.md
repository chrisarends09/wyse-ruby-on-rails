# wyse-ruby-on-rails
Setup native Ruby On Rails on a Wyse 5070 thin client

I wanted to install Ruby on Rails v7.0.5 and not using docker containers on the Wyse 5070 thin client
I had lots of trouble using the https://guides.rubyonrails.org/getting_started.html
    when I got to the $ gem install rails
    everytime the OS couldn't connect to download the gems and I found many people having similar errors.

# Installed UBUNTU 22.04 server
I found a WORKING guide at https://gorails.com/setup/ubuntu/22.04
This guide uses version manager called ASDF
  https://asdf-vm.com/

# setup git and setup Postgres
https://gorails.com/setup/ubuntu/22.04

  

# Installed FEDORA 38 server
The steps worked for Fedora 38 server using RVM
# 1st these steps
https://tutorialforlinux.com/2023/03/12/rvm-fedora-38-installation-step-by-step-guide/2/
# 2nd 
https://tecadmin.net/install-ruby-on-fedora/
  $ rvm requirements run 
    Checking requirements for fedora.
    Requirements installation successful
  $ rvm install 3.2.2
  $ ruby -v
  $ rvm list
  $ gem install bundler
# 3rd
https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-with-rvm-on-ubuntu-20-04
  $ gem search '^rails$' --all
  $ gem install rails -v 7.0.5
  $ \curl -sSL https://deb.nodesource.com/setup_18.x -o nodejs.sh
  $ nano nodejs.sh
  $ sudo dnf install nodejs
# 4th
  create new rails app and start
  $ rails new tutorial
  $ cd tutorial
  $ rails s --binding=0.0.0.0
# ALSO SET THE FEDORA FIREWALL TO ALLOW PORT 3000 IN FROM EXTERNAL SOURCE

# 5th
https://guides.rubyonrails.org/getting_started.html
general into modifying Ruby on Rails app

# setup git and setup Postgres
https://gorails.com/setup/ubuntu/22.04

setup Postgress
# Add REPO https://computingforgeeks.com/install-postgresql-database-fedora-linux/
sudo dnf -y install https://download.postgresql.org/pub/repos/yum/reporpms/F-38-x86_64/pgdg-fedora-repo-latest.noarch.rpm
then
# https://www.itzgeek.com/how-tos/linux/fedora-how-tos/how-to-install-postgresql-on-fedora.html
    1. sudo dnf update --refresh
    2. sudo dnf install -y postgresql15-server
    3. sudo /usr/pgsql-15/bin/postgresql-15-setup initdb
    4. sudo systemctl enable --now postgresql-15
    5. sudo systemctl status postgresql-15
    6. $ sudo su -l postgres
    7. $ psql
    8. postgres=# \password  "for dev env used postgres"
    9. sudo su - postgres -c "chris"
    10. sudo su - postgres -c "createdb testdb"
    11. sudo -u postgres psql
    12. GRANT ALL PRIVILEGES ON DATABASE tetdb TO chris;
    13. paql testdb
    14. \du
    
# INSTALL https://docs.fedoraproject.org/en-US/quick-docs/postgresql/
sudo -i -u postgres
