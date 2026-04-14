Task 1
1. Get IP address of a domain (guvi.in)
Command:  **nslookup guvi.in**
Purpose:Retrieves the IP address of the domain.


2. Check CPU and Memory Usage
Command:  **top**
Purpose:
Displays real-time CPU and memory usage of the server.

3. Test Connectivity Between Two Nodes
Command: **ping guvi.in**
Purpose:
Checks whether the target node is reachable.


Task 2
Problem:
Application is deployed on guvi.com:9000 but not accessible.
1. Check if Application is Running Locally
Command: **curl http://localhost:9000**
Purpose:
Verifies if the application is working on the server.


3. Check if Port is Listening
Command: **sudo ss -tulpn | grep :9000**
Purpose:
Checks whether any service is listening on port 9000.

4. Scan Port Using Nmap
Command: **nmap -p 9000 guvi.com**
**Observed Output:**
9000/tcp filtered

Inference:
Port 9000 is filtered (blocked by firewall or proxy).
4. Check Port Connectivity Using Netcat
Command: **nc -zv guvi.com 9000**
Purpose:
Tests whether port 9000 is reachable.
