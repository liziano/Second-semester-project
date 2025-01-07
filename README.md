STEP BY STEP PROCESS USED IN CARRYING OUT THE PROJECT
Created an account with AWS on aws.amazon.com
Spinned an EC2 instance with ubuntu OS using a key pair authentication
Configured the instance by adding an inbound rule to the security group to allow ssh connection through port 22 from anywhere
Connected to the instance (ssh connection) through termius shell or any other desired terminal after locating the folder containing the public key I downloaded while creating the instance
updated the OS by running sudo apt update and as well upgraded system by running sudo apt upgrade -y
Thereafter installed the web server nginx with sudo apt install nginx -y
I added to the security group on AWS an inbound rule that allows access to http through port 80 in order to allow the webserver accessible on the internet
Purchased a domain from enrolweb.com and linked the server's IP as A record to the domain
installed certbot a tool for managing let's encrypt ssl on the server by running the following commands
sudo apt update
sudo apt install certbot python3-certbot-nginx # For Nginx
Also run sudo certbot --nginx after installation, this allow certbot to detect nginx configuration and automatically update it to use SSL. It also Obtained and installed the SSL certificate
Added an inbound rule to the security group on my instance on AWS by allowing HTTPS access through port 443 and setting the connection to everywhere
searched my domain in my browser and ensured the padlock appeared in the address bar.
I then replaced the index.html file in the /var/www/html with my the index.html file for my page
This is my public IP 16.170.249.216 linked to my domain acevividtravels.com.ng
