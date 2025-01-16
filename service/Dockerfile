# FROM python:3


# RUN apt-get update -y && \
#     apt-get install -y python-pip python-dev

# COPY . /src
# WORKDIR /src
# RUN pip install -r requirements.txt

# EXPOSE 5000

# CMD cd /src && python recommender_system_service.py

FROM python:3

# Install required dependencies
RUN apt-get update -y && \
    apt-get install -y build-essential libssl-dev libffi-dev python3-dev && \
    apt-get clean

# Copy the current directory contents into the container
COPY . /src
WORKDIR /src

# Install Python dependencies
RUN python3 -m pip install -r requirements.txt

# Expose the port
EXPOSE 5000

# Start the application
CMD cd /src && python recommender_system_service.py