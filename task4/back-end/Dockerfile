FROM ubuntu:latest

# Update and upgrade system
RUN apt-get update
RUN apt-get upgrade -y

# Install Python and pip
RUN apt-get install -y python3 python3-pip

# Fix externally managed environment issue
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip
RUN pip3 install flask

# Set working directory
WORKDIR /app

# Copy Flask app
COPY api.py /app/api.py

# Run Flask app
CMD ["python3", "api.py"]
