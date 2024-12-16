# Use the latest Ubuntu as the base image
FROM ubuntu:latest

# Update and upgrade the APT package lists
RUN apt-get update
RUN apt-get upgrade -y

# Install Python3 and pip3 (needed to install Flask)
RUN apt-get install -y python3 python3-pip

# Remove EXTERNALLY-MANAGED file to avoid pip installation errors
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip3
RUN pip3 install Flask

# Set the working directory inside the container
WORKDIR /app

# Copy the Flask API file into the container
COPY ./api.py /app/api.py

# Expose port 5252 for the Flask app
EXPOSE 5252

# Run the Flask app
CMD ["python3", "api.py"]
