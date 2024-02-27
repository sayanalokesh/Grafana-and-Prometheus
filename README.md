# Grafana-and-Prometheus
Objective: Implement comprehensive monitoring and observability solutions for a MERN (MongoDB, Express.js, React.js, Node.js) application, integrating Prometheus metrics, MongoDB monitoring, log aggregation, distributed tracing, and advanced Grafana dashboards with alerting and anomaly detection.

# Installation of NodeJs

```bash
curl -s https://deb.nodesource.com/setup_18.x | sudo bash
sudo apt install nodejs -y
node -v
```
![image](https://github.com/sayanalokesh/Grafana-and-Prometheus/assets/105637305/cc1beb11-4b4c-4608-92c1-8bf71720934b)
![image](https://github.com/sayanalokesh/Grafana-and-Prometheus/assets/105637305/79300223-edfe-46fb-8e40-70cc965059ea)
![image](https://github.com/sayanalokesh/Grafana-and-Prometheus/assets/105637305/40d602f6-6bc8-4fa5-8b7b-f12a83a9d0e9)

# Clone the Git repo
```bash
git clone https://github.com/UnpredictablePrashant/TravelMemory.git
```
![image](https://github.com/sayanalokesh/Grafana-and-Prometheus/assets/105637305/6308d089-77ac-4a7e-b345-2a859102d974)

Create nano .env
```
MONGO_URI='mongodb+srv://lokesh:<password>@travelmemory.3a09n5s.mongodb.net/travelmemory'
PORT=3000
```
# Installation of Grafana and Prometheuswget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
Before this, you need to open the ports of 3000 (Grafana) and 9090 (Prometheus). Please make sure to run the commands one by one:
```
sudo apt-get update
sudo apt-get install -y software-properties-common
sudo add-apt-repository "deb https://packages.grafana.com/oss/deb stable main"
wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
sudo apt-get update
sudo apt-get install grafana
```
Now that Grafana is installed, let’s start and enable it by executing the following commands:
```
sudo systemctl start grafana-server
sudo systemctl enable grafana-server
```
In the next step, we will be installing Prometheus which is a monitoring tool.
```
sudo apt-get install prometheus
sudo systemctl enable prometheus
```
# Accessing Grafana:
We can access Grafana via browser by using our instance IP:3000. The initial credentials if logging in for the first time are admin for both username and password. You will then get prompted to change the password in the next step.
## Adding Prometheus as a data source:
On the Grafana home page, click on the hamburger icon, Connections then Data sources.
![image](https://github.com/sayanalokesh/Grafana-and-Prometheus/assets/105637305/3daa492b-3df7-4d32-8883-926be7f3ed42)
![image](https://github.com/sayanalokesh/Grafana-and-Prometheus/assets/105637305/dcc8101a-95bb-41bf-ba7a-398d0080796c)
![image](https://github.com/sayanalokesh/Grafana-and-Prometheus/assets/105637305/f75f9a82-3a13-47dd-85f8-ed0c7ef5f48a)
For URL, use http:/<ec2ipaddress>:9090 then scroll down and click on Save & test.
![image](https://github.com/sayanalokesh/Grafana-and-Prometheus/assets/105637305/f1428813-12c8-40ab-a816-bef9aa933d88)
![image](https://github.com/sayanalokesh/Grafana-and-Prometheus/assets/105637305/8d94acdf-3e2b-4b0f-838d-22c0f11ffba5)
![image](https://github.com/sayanalokesh/Grafana-and-Prometheus/assets/105637305/b0419ae2-a47a-4371-99f1-ac0c05212965)



