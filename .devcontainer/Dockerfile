# For more information, see https://containers.dev/guide/dockerfile
FROM mcr.microsoft.com/devcontainers/python:0-3.10

# Install system dependencies for both consumer and provider
RUN apt-get update \
    && apt-get install -y --no-install-recommends curl jq \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Set up a workspace folder
WORKDIR /workspace

# (Optional) Install additional Python dependencies for both consumer and provider
#COPY infrastructure/dataspace-components/consumer/requirements.txt /tmp/consumer-reqs.txt
#COPY infrastructure/dataspace-components/provider/requirements.txt /tmp/provider-reqs.txt
#RUN pip install --upgrade pip \
#    && pip install -r /tmp/consumer-reqs.txt -r /tmp/provider-reqs.txt

# (Optional) Expose ports for Flask, Mosquitto, etc. if you want to debug inside the container
EXPOSE 5001 1883 8081 8082 8083 8084 8085 3000

# Default user is vscode
USER vscode
