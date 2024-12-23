FROM ubuntu:latest

# Install Python dependencies
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y python3 python3-pip

RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask module
RUN pip3 install flask

# Get api code from folder to Ubuntu container
WORKDIR /app
COPY ./api.py .

# Forward port 5252
EXPOSE 5252

# Run Flask API
CMD ["python3", "api.py"]
