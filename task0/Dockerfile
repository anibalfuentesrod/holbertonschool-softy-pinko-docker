# use latest version of ubuntu as the base img
FROM ubuntu:latest

# updates APT and upgrades install software
RUN apt-get update && apt-get upgrade -y

# install python3 and pip3
RUN apt-get install -y python3 python3-pip

# install flask using the pip3
RUN pip3 install flask

# if you encounter the "this env is externally managed" error
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# set /app as the working dir()
WORKDIR /app

# cp the api.py file to the docker img
COPY ./api.py /app/api.py

# define the command that runs when the container starts
CMD ["python3", "api.py"]