<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://youtu.be/O3ISo0YCi5Q?si=_V8ZIBeRs5Tc_9kN)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create Virtual Machines
- Remote Desktop into VMs
- Install & Run WireShark
- Test Connectivity Between VMs

<h2>Actions and Observations</h2>


![image](https://github.com/Tsteele8/Network-Security/assets/149441408/25d5bf17-b271-4122-8bdc-1abe1b4cfc82)


<p>
 Create two Vitrual Machines in Azure: Log into the Microsoft Azure Portal with your Microsoft Account --> search "resource groups" in the search bar --> "create" resource group --> search "Virtual Machines" in the search bar --> "create" two Virtual Machines with the following OS: Windows 10 OS for VM1 & Ubuntu OS for VM2) --> Make sure both VMs are in the same "resource group". *When setting up the VMs remember the username and password that you use.
</p>
<br />


![image](https://github.com/Tsteele8/Network-Security/assets/149441408/ddc951bb-7ebb-4cb9-9fb8-878ec7a8c219)


<p>
 Remote Desktop into each "Virtual Machine". Go to --> VM1 settings --> copy "public IP address" --> search "remote desktop connections" in start menu search bar --> Open "Remote Desktop Connection" & paste copied IP address from VM1 --> click connect --> Use the Username & Password created in step 1 to sign in to the VM. Repeat the same steps to log into VM2.
</p>
<br />


![image](https://github.com/Tsteele8/Network-Security/assets/149441408/b3b259b3-5f7f-4c67-ad75-b6f8e3c0930b)


![image](https://github.com/Tsteele8/Network-Security/assets/149441408/4690bf5a-6d2c-4fff-8a06-2c1e3f4c9ead)


<p>
download WireShark. Search "WireShark" on google --> click Wireshark's official site --> "Windows Installer (64-bit)" download --> Install WireShark and go through installation prompts --> Open WireShark --> click "Ethernet 2" --> next select "shark symbol" in upper left hand corner to start network traffic monitoring
</p>


![image](https://github.com/Tsteele8/Network-Security/assets/149441408/7849e019-b09b-455c-b861-f2c08169f56f)


![image](https://github.com/Tsteele8/Network-Security/assets/149441408/41f51fcc-115d-47b2-9205-f9a66e140080)


![image](https://github.com/Tsteele8/Network-Security/assets/149441408/48015b7c-c602-46ec-9c67-74f7082bbaa4)

Search "PowerShell" in the start menu search bar & open it --> Type "ping -t" then paste VM2's private IP address into "PowerShell" to start a "perpetual ping" (WireShark will now show the two VMs pinging back and forth, allow the ping to continue).
