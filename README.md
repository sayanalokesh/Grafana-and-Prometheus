# Grafana-and-Prometheus
Objective: Implement comprehensive monitoring and observability solutions for a MERN (MongoDB, Express.js, React.js, Node.js) application, integrating Prometheus metrics, MongoDB monitoring, log aggregation, distributed tracing, and advanced Grafana dashboards with alerting and anomaly detection.

Installation and Configuration Guide

1. Node.js and TravelMemory Repository Setup

1.1 Prerequisites:

    Ubuntu/Debian-based system
    Basic understanding of command line

1.2 Node.js Installation:

    Download the NodeSource setup script:
    Bash

    curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash -

    Use code with caution.

Install Node.js and npm package manager:
Bash

sudo apt install -y nodejs

Use code with caution.

Verify installation:
Bash

node -v

Use code with caution.

1.3 Clone the TravelMemory Repository:

    Install Git:
    Bash

    sudo apt install -y git

    Use code with caution.

Clone the repository:
Bash

git clone https://github.com/UnpredictablePrashant/TravelMemory.git

Use code with caution.

1.4 Create and Configure Environment File:

    Navigate to the project directory:
    Bash

    cd TravelMemory

    Use code with caution.

Create an .env file:
Bash

nano .env

Use code with caution.

    Paste the following lines into the .env file, replacing <password> with your actual MongoDB password:

    MONGO_URI='mongodb+srv://lokesh:<password>@travelmemory.3a09n5s.mongodb.net/travelmemory'
    PORT=3000

    Save and close the file.

2. Grafana and Prometheus Installation and Configuration

2.1 Prerequisites:

    Port 3000 (for Grafana) and Port 9090 (for Prometheus) opened in firewall

2.2 Grafana Installation:

    Update package lists:
    Bash

    sudo apt-get update

    Use code with caution.

Install prerequisites:
Bash

sudo apt-get install -y software-properties-common

Use code with caution.

Add Grafana repository:
Bash

sudo add-apt-repository "deb https://packages.grafana.com/oss/deb stable main"

Use code with caution.

Import Grafana GPG key:
Bash

wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -

Use code with caution.

Update package lists again:
Bash

sudo apt-get update

Use code with caution.

Install Grafana:
Bash

sudo apt-get install Grafana

Use code with caution.

Start and enable Grafana service:
Bash

sudo systemctl start grafana-server
sudo systemctl enable grafana-server

Use code with caution.

2.3 Prometheus Installation:

    Install Prometheus:
    Bash

    sudo apt-get install Prometheus

    Use code with caution.

Enable Prometheus service:
Bash

sudo systemctl enable prometheus

Use code with caution.

3. Accessing Grafana

    Open your web browser.

    Navigate to: http://<your_instance_IP>:3000 (replace <your_instance_IP> with your server's IP address).

    Initial login:
        Username: admin
        Password: admin

    Change your password after logging in for the first time.

4. Adding Prometheus as a Data Source in Grafana

    In Grafana, click the hamburger icon (≡).

    Select "Configuration" and then "Data sources."

    Click "Add data source."

    Select "Prometheus" as the data source type.

    In the "URL" field, enter http://localhost:9090 (if Prometheus is running on the same machine as Grafana) or replace localhost with the appropriate IP address if it's running on a different machine.

    Scroll down and click "Save & test."
