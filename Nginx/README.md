# Implementing Loadbalancers with NGINX

introduction to Load Balancer and Nginx.

![loadbalancer](./img/0.7%20loadbalancer.png)

Load balancing is like having a teams of helpers working together to make sure a big deal gets done smoothly and efficiently. Imagine you have alot of large boxes to carry but you cant carry them all by yourself because they are too heavy.

Load balancing is when you call your friends to help you carry the boxes. Each friends takes some of the boxes and carries them to the right place. This way the work gets done easier and faster because everyone is working together.

Nginx is a versatile software, it can act like a webserver, reverse proxy and load balancer etc. All that is needed is to configure it properly to serve your use case.

in this project, i will be working you through how to configure Nginx as a load balancer.

## Apache installation.

Apache is open-source web server software that is developed and maintained by the Apache Software Foundation and is available for free.

It’s fast, reliable, and secure and runs on 31% of web servers, while an alternative, NGINX, runs on 34%. Apache can be highly customized to meet the needs of many different environments by using extensions and modules.


![apache](./img/0.1%20install-apache.png)


## status

After successfully installing Apache, we will verify if it is working effectively using by checking its status using the command highlighted in the image below.

The status below shows Apache is running effectively.

![status](./img/0.2%20status.png)

## Configure Apache to server.

We will start by configuring Apache webserver to serve content on port 8000 instead of it's default port which is port 80. Then we will create a new index.html file. The file will contain code to display the public IP of the EC2 instance. We will the override apache webserver's default html file with our new file.

To do this, we will Vi into /etc/apache2/ports.conf and make it listen to 8000.

![configuration-of-apache](./img/0.8%20port.png)

Next, we will open the file /etc/apache2/sites-available/000-default.conf and change port 80 ton the virtual host to port 8000.

![virtualhost](./img/0.9%20virtualhost.png)

## Html
Creating our index.html file, we will vi into index.html and paste this code below.

![index.html](./img/10.%20index.png)

Aftrerwards restart apache then we will run the Public IP with port 8000 in our web browser.

![html](./img/0.3%20html.png)

## Nginx installation and Status
Configure Nginx as a Load balancer.

Provision a new EC2 instance running on ubuntu 22.04. Open Port 80 to accept traffic from anywhere. Install Nginx into the instance and confirm it's status.

![nginx](./img/0.4%20nginx-started.png)

After confirming the status of Nginx, Open Nginx Configuration file and input your webserver IP address and Port number 8000, and also edit your Load balancer public IP. with the code below vi /ect/nginx/conf.d/loadbalaner.conf

![lb](./img/11.%20Lb.png)

*Upstream backend_servers* defines a group of backend servers. The server line inside the *Upstream block* list the addresses and port of your backend proxy. *Proxy_pass* inside the *location* sets up the load balancing, passing the requests to the backend servers. The *Proxy_setheader* lines pass necessary headers to the backend servers to correctly handle the request.

## Test

After configuration of Nginx, test to see if it is running using sudo nginx -t .

![nginx-started](./img/0.5%20nginx-successfull.png)

## Load Balancer

Paste the ip address of Nginx load balancer, you should see the same webpage served by your webserver.

![loadbalancer](./img/0.6%20loadbalancer.png)

# Load Balancing Algorithms

Load balancing algorithms are techniques used to distribute incoming network traffic or workload accross multiple servers, ensuring efficient utilization of resources and improving overall system performance, reliablity, and availability. Here are some Load Balancer Algorithms..
- Round Robin.
- Least Connection.
- Weighted Round Robin.
- Weighted Least Connection.
- IP Hash.