# Automating Load Balancer Configuration with Shell Scripting.

In this project, we will be streamlining our load balancer configuration with ease using shell scripting and simple CI/CD on Jenkins. This project demonstrates how to automate the setup and maintanance of our load balancer using a freestyle job, enhancing efficiency and reducing manual effort.

## Automate the Deployment of Webservers.
In this project we will be implementing load balancer and nginx. Firstly we will deploy two backend servers, with a load balancer distributing trafic accross the webservers.

## Deploying and Configuring the Webservers.
Firstly, we will provision two ec2 instances.
Then follow the process accordingly.

### installation file.
![installation-file](./img/0.1%20installation-file.png)

### Bash file

All the process we need to deploy out webservers has been codified in the shell script below.

![bash-file](./img/0.2%20bin-file.png)

### Test
Run the shell scripting after it's been editing as instructed in the file.
![test](./img/0.3%20Automation.png)
if there isnt any error sign then the webservers fully functional.

N/B run same command on both instances created.

# Deploying Nginx as a Load Balancer using Shell Script.
## Automate the Deployment of Nginx as a Load Balancer Using Shell Scipt.
Having successfully deployed and configured two webservers, we will move on to the load balancer. As a prerequisite,  we need to provisoon an EC2 instance running ubuntu 22.04 to anywhere using the security group and connect to the load balancer via the terminal.


### Deploying and Configuring Nginx Load Balancer. 
### Nginx.sh file
On the terminal open the file nginx.sh using the code below
sudo vi nginx.sh

![nginx-file](./img/0.4%20create-nginx-file.png)

### Nginx Bash file
Copy and paste the script inside the file. Ensure all instructions are followed and also ensure the IP addresses are edited as instructed in the file.

![nginx-bash-file](./img/0.5%20Nginx-file.png)

### Test & Run
Run the script with the command below.

./nginx.sh PUBLIC_IP Webserver-1 Webserver-2

![test](./img/0.6%20Automated-lb.png)

## Verify the setup

### Webserver 1
![webserver1](./img/0.7%20webserver1.png)

### Webserver 2
![webserver2](./img/0.8%20webserver2.png)

### Loadbalancer
![loadbalancer](./img/0.9%20loadbalancer.png)

