# Use the official Python base image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the requirements.txt file into the container
COPY requirements.txt .
RUN apt-get update \
 && apt-get install --no-install-recommends -y \
      vim \
      curl \
      ca-certificates \
      gcc \
      python3-dev
# Install the dependencies from requirements.txt
RUN pip install -r requirements.txt

# List installed packages
RUN pip freeze > installed_packages.txt
