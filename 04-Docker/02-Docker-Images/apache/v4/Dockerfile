# Base Image 
FROM amitvashist7/devops-netmagic-08-aug-2022-myapache:v1

# Maintainer of this Image 
MAINTAINER Amit Vashist <amitvashist7@outlook.com>

# Make APT Ready 
RUN apt-get update 

# Install Apache Packages 
RUN apt-get install apache2 -y

# Deploy Custom Web Page
COPY index.html /var/www/html/index.html
 
# Expose Port 
EXPOSE 80
EXPOSE 8080
EXPOSE 3306 

# Start Apache Service 
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND" ] 
