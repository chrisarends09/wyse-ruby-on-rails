# wyse-ruby-on-rails
Setup native Ruby On Rails on a Wyse 5070 thin client

I wanted to install Ruby on Rails v7.0.5 and not using docker containers on the Wyse 5070 think client
I had lots of trouble using the https://guides.rubyonrails.org/getting_started.html
    when I got to the $ gem install rails
    everytime the OS couldn't connect to download the gems and I found many people having similar errors.

# UBUNTU 22.04 server
I found a WORKING guide at https://gorails.com/setup/ubuntu/22.04
This guide uses version manager called ASDF
  https://asdf-vm.com/

# setup git
https://gorails.com/setup/ubuntu/22.04

  

# FEDORA 38 server
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

# setup git
https://gorails.com/setup/ubuntu/22.04

