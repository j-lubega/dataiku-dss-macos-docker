# <img width="2000" height="500" alt="image" src="https://github.com/user-attachments/assets/615fab9e-c792-4cd0-b8cb-14759d8c264d" />

### Deploying Dataiku DSS on macOS Using Docker Desktop

This repository contains a step-by-step guide for deploying Dataiku DSS on macOS using Docker Desktop.

### Contents

- 📄 Full deployment guide with screenshots and diagrams below

This guide provides step-by-step instructions for installing and running Dataiku Data Science Studio (DSS) locally on a MacBook using Docker Desktop. This setup is ideal for learning, development, and experimentation with Dataiku DSS in a lightweight, containerized environment.

By the end of this guide, you will have a fully functional Dataiku DSS instance accessible through your web browser.

# Prerequisites

- A MacBook running macOS
- Internet connectivity
- Administrative access to install applications
  
## Step 1: Install Docker Desktop
If Docker Desktop is not already installed on your system: Download Docker Desktop for macOS from the official Docker website below:
https://www.docker.com/products/docker-desktop/ 

# <img width="1600" height="775" alt="image" src="https://github.com/user-attachments/assets/11fa4634-31c0-408d-b92c-2ec48a8facd7" />

Follow the installation instructions and complete the setup.
Verify the installation by opening a terminal and running:

```bash
docker --version
```

## Step 2: Run the Dataiku DSS Docker Container
Open Terminal on your MacBook.
Run the following command to pull the Dataiku DSS image and start the container:

```bash
# Use this if you are running Mac - Apple Silicon (M2,M3,M4 Chip)
docker run -d --platform=linux/amd64 -p 10000:10000 dataiku/dss

# Use the following command if you are running Mac - Intel Chip
docker run -d -p 10000:10000 dataiku/dss
```

## Explanation:

- -d runs the container in detached mode

- -p 10000:10000 maps the DSS web UI port to your local machine

- dataiku/dss is the official Dataiku DSS Docker image

Run the following command in the terminal to confirm that the dataiku container is running:

```bash
 docker ps | grep dataiku
```
## Step 3: Access the Dataiku DSS Web Interface

Open a web browser.

Navigate to: http://localhost:10000

Alternatively, you may use your Mac’s IP address: http://your-mac-ip-address:10000

The Dataiku DSS welcome screen should now be visible.
# <img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/996487cf-6f03-4fed-a530-1afc559e4709" />

For more information on how to deploy dataiku dss using docker desktop on your Mac, see the resource here: https://hub.docker.com/r/dataiku/dss 

### Download guide from my dataiku-dss-macos-docker repo if interested

- Dataiku-DSS-MacOS-Deployment.docx

### Audience
- Data engineers
- Data scientists
- Platform / DevOps engineers
- Technical Support Managers
- Anyone evaluating or deploying Dataiku DSS locally

Author: Jimmy Lubega
