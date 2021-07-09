## railsserver.net
Rails Server | Create and deploy your rails app in a minute

## Get Started
create an account in Rails Server complete your rails app and start to deploy your app by follow step by step in the quide line.


## Create Server
No server yet? No worry we have set and ready for you to go...


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
