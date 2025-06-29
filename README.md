# Task-4-Elevate-Labs
Windows Firewall Steps
1. Open Firewall Configuration Tool
Go to Start → Search for “Windows Defender Firewall with Advanced Security” → Open.

2. List Current Firewall Rules
Inside the GUI, click Inbound Rules and Outbound Rules to see active firewall rules.

3. Add Rule to Block Inbound Traffic on Port 23 (Telnet)
Go to Inbound Rules → New Rule…

Select Port → TCP → Specific port: 23

Choose Block the connection

Apply to all profiles (Domain, Private, Public)

Name it e.g., Block_Telnet_23

4. Test the Rule
Open Command Prompt and try:

cmd
Copy
Edit
telnet localhost 23
You should get “Could not open connection…” (rule is working).

5. (Skip SSH step on Windows)
6. Remove the Test Block Rule
In Inbound Rules, find Block_Telnet_23 → Right-click → Delete.

7. Document Commands or GUI Steps
GUI used: Windows Defender Firewall with Advanced Security

Rule Type: Inbound → Port → TCP 23 → Block

8. Summarize How Firewall Filters Traffic
Windows Firewall monitors and controls incoming and outgoing network traffic. Based on defined rules, it either blocks or allows traffic depending on source, destination IP, port, and protocol. In this task, traffic to Telnet (port 23) was blocked, which prevented external or local attempts to use that service.
