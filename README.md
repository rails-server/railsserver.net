## railsserver.net
Rails Server | Create and deploy your rails app in a minute

## Get Started
create an account in Rails Server complete your rails app and start to deploy your app by follow step by step in the quide line.


## Create Server
No server yet? No worry we have set and ready for you to go...

visit [ezicom.net](http://ezicom.net/ "To get hosting server").

## before started.
* Rails Server (recommeded) to use puTTY is an SSH and telnet client to start your project.

PuTTY is an SSH and telnet client, developed originally by Simon Tatham for the Windows platform. PuTTY is open source software that is available with source code and is developed and supported by a group of volunteers.


You can download PuTTY [here.](https://www.putty.org/ "download PuTTY").

* FileZilla Pro File Transfer for Windows, Mac and Linux
Transfer files from your computer via FTP/SFTP/FTPS, Amazon S3, Backblaze B2,  Box, Dropbox,  Google Cloud, Google Drive, Microsoft Azure, Microsoft OneDrive, Microsoft OneDrive for Business, Microsoft SharePoint, OpenStack Swift and WebDAV.

One tool to find, transfer and download all of your files.

FileZilla Pro, the professional tool for file transfers, allows you to focus on getting your job done. 

Free and paid pro version available. To download FileZilla [here.](https://filezilla-project.org/filezilla_pro.php "download FileZilla").

## Time to start.
## Create Your New Rails App
`$ ruby -v` To check ruby version.
>
`$ bundler -v` To check bundle version.
>
`$ rails -v` to check rails version.
>
`$ rails new [yourapp]`
>
`$ cd [yourapp]`
>
`$ rails generate controller Articles index` 
# set up routes.
Let's open config/routes.rb
   
    Rails.application.routes.draw do
      root "articles#index"

      get "/articles", to: "articles#index"
    end
 
# to run your app
>
`$ rails s -b 139.162.55.17`
or to get it works on railsserver port 80
>
`$ rails s -b 139.162.55.17 -p 80`
>

## output:

![Here Your Output App](/assets/railsserver_started.png  "You are on Rails")

## Customize your app
Ruby on Rails Guidest [rubyonrails](https://guides.rubyonrails.org/ "go to rubyonrails").
## Installing NGINX & Passenger
`$ sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 561F9B9CAC40B2F7`.
>
`$ sudo sh -c 'echo deb https://oss-binaries.phusionpassenger.com/apt/passenger focal main > /etc/apt/sources.list.d/passenger.list`.
>
`$ sudo apt-get update`.
>
`$ sudo apt-get install -y nginx-extras libnginx-mod-http-passenger`
>
`$ if [ ! -f /etc/nginx/modules-enabled/50-mod-http-passenger.conf ]; then sudo ln -s /usr/share/nginx/modules-available/mod-http-passenger.load /etc/nginx/modules-enabled/50-mod-http-passenger.conf ; fi`
>
`$ sudo ls /etc/nginx/conf.d/mod-http-passenger.conf`

# NGINX and Passenger installed Now start config...
We simply want to change the passenger_ruby line to match the following:
`passenger_ruby /usr/local/bin/ruby;`
