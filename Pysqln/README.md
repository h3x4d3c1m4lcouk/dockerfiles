# dockerfiles
#
Docker files to build a Docker image running Mysql Python3 and Nginx on Ubuntu

To build run 

$ docker build --rm -f "Dockerfile" -t pysqln:latest .

To run this with a persistent image for the database and storage area for code

$ docker run -it --name pysqln -v pysqln-data:/var/lib/mysql -v pysqln-code:/code pysqln:latest

This is quite a big really and would be better with a smaller image base like alpine