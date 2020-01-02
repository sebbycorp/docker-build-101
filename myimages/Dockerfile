#Download base image ubuntu 16.04
FROM ubuntu:latest

# Update Ubuntu Software repository
RUN apt-get update


# The line below states we will base our new image on the Latest Official Ubuntu 
FROM ubuntu:latest

#
# Identify the maintainer of an image
LABEL maintainer="sebastian@maniak.io"

#
# Update the image to the latest packages
RUN apt-get update && apt-get upgrade -y

#
# Install NGINX to test.
RUN apt-get install nginx -y

# Install curl
RUN app-get install curl -y

RUN apt-get install libsqlite3-dev libxslt-dev libxml2-dev zlib1g-dev gcc -y

#
# Expose port 80
EXPOSE 80

#
# Last is the actual command to start up NGINX within our Container
CMD ["nginx", "-g", "daemon off;"]

