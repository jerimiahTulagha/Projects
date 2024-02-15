# Implementing Loadbalancers with NGINX

Load balancing is like having a teams of helpers working together to make sure a big deal gets done smoothly and efficiently. Imagine you have alot of large boxes to carry but you cant carry them all by yourself because they are too heavy.

Load balancing is when you call your friends to help you carry the boxes. Each friends takes some of the boxes and carries them to the right place. This way the work gets done easier and faster because everyone is working together.

Nginx is a versatile software, it can act like a webserver, reverse proxy and load balancer etc. All that is needed is to configure it properly to serve your use case.

in this project, we will be working you through how to configure Nginx as a load balancer.

## Apache installation.

Apache is open-source web server software that is developed and maintained by the Apache Software Foundation and is available for free.

It’s fast, reliable, and secure and runs on 31% of web servers, while an alternative, NGINX, runs on 34%. Apache can be highly customized to meet the needs of many different environments by using extensions and modules.


![apache](./img/0.1%20install-apache.png)


## status


The status shows Apache is running effectively.

![status](./img/0.2%20status.png)

## Html

Here we are to use the ip address with port number 8000 to run in our web browser.

![html](./img/0.3%20html.png)

## Nginx installation and Status

install Nginx and confirm the ststus.

![nginx](./img/0.4%20nginx-started.png)

## Nginx successfully running.

After configuration of Nginx, test to see if it is running using sudo nginx -t .

![nginx-started](./img/0.5%20nginx-successfull.png)

## Load Balancer

Paste the ip address of Nginx load balancer, you should see the same webpage served by your webservers.

![loadbalancer](./img/0.6%20loadbalancer.png)

# Load Balancing Algorithms

Load balancing algorithms are techniques used to distribute incoming network traffic or workload accross multiple servers, ensuring efficient utilization of resources and improving overall system performance, reliablity, and availability. Here are some Load Balancer Algorithms..
- Round Robin.
- Least Connection.
- Weighted Round Robin.
- Weighted Least Connection.
- IP Hash.