# Task7
Monitor System Resources Using Netdata


1. Install Docker (if not already installed)
Make sure Docker is installed on your system. You can follow the official Docker installation guide for your OS.

2. Pull and Run the Netdata Docker Container

Open a terminal and run the following command to pull the Netdata image from Docker Hub:
docker pull netdata/netdata
Once the image is pulled, start the Netdata container:
docker run -d --name=netdata -p 19999:19999 --restart=always netdata/netdata
-d runs the container in detached mode.
--name=netdata gives the container a name.
-p 19999:19999 maps the port 19999 of the container to the same port on the host.
--restart=always ensures the container starts automatically on system reboot.


3. Access the Netdata Dashboard

After the container is running, open a browser and go to:
http://localhost:19999
You should see the Netdata dashboard with real-time monitoring data of your system resources (CPU, RAM, disk usage, network, etc.) and app performance.

4. Screenshot and Running Metrics

Once the dashboard is live, take a screenshot of the metrics displayed. You’ll see:
System Resources: CPU, RAM, Disk, and Network usage.
Application Metrics: Metrics related to web servers, databases, and other services if they are running on your system.
The dashboard will update in real-time to reflect the performance data.

5. (Optional) Configure Netdata for Enhanced Monitoring

Netdata provides extensive configuration options. You can adjust the settings to monitor specific applications or more detailed metrics by editing the Netdata configuration files located in /etc/netdata/ within the container or by configuring via the web interface
