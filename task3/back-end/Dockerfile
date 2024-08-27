# Use the latest version of Ubuntu as the base image
FROM ubuntu:latest

# Update APT and upgrade installed software
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Remove the EXTERNALLY-MANAGED marker
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask and Flask-CORS using pip3
RUN pip3 install flask flask-cors

# Set /app as the working directory
WORKDIR /app

# Copy the api.py file to the Docker image
COPY ./api.py /app/api.py

# Define the command that runs when the container starts
CMD ["python3", "api.py"]