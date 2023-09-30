<p align="center">
<img width="609" alt="Screenshot 2023-09-29 at 6 41 03 PM" src="https://github.com/lucasfregoso/dns-ad-azure/assets/144977615/a982e4a9-3c3b-4481-84db-cb8380240086">
</p>

<h1>DNS - Building an intuition for DNS </h1>
This tutorial outlines the in and outs of how DNS works by taking the human readable names of various websites and convering them to computer readable and useable IP addresses.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell
- Command Prompt

<h2>Operating Systems Used </h2>

- Windows Server Datacenter 2022 Azure Edition
- Windows 10 (22H2)

<h2>DNS Building Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4

(Images going from left to right)
<h2>DNS Building Steps</h2>

Step 1
<p>
<img width="1617" alt="Screenshot 2023-09-29 at 7 31 20 PM" src="https://github.com/lucasfregoso/dns-ad-azure/assets/144977615/c8735ae4-b637-43ef-ab00-9020b0e6f673">
-------------------------------------------------------------------------------------------------------------------
<img width="1382" alt="Screenshot 2023-09-29 at 7 32 37 PM" src="https://github.com/lucasfregoso/dns-ad-azure/assets/144977615/e8b5f23b-fa1c-4109-90d7-4fe0eaf10339">
</p>
<p>
For this lab we are going to building off the Active Directory lab with our two virtual machines being DC-1 as our domain controller and Client 1 essentially as our user. In this part, we go over A reacords which essentially points a domain to the IP address of a computer hosting that domain. First, we connec to DC-1 as our admin (lucas_admin), same with Client 1, and in Client 1 we try and ping "mainframe" and notice that fails. This is because Client 1 tries to do three things, one is by checking the cache and get now result, two is checking the local host file and with no result, three by checking the DNS server and when that has no result, then the ping fails. So to correct this, on DC-1 we go to server manager, then tools, click DC-1, expand forward lookup zones, click domainexpansion.com, and add a new A Record. For the name we put "mainframe" and then for the IP address we put it as 10.0.0.4. When we ping it again, we now get a reponse back indicating to us that it works now and the reason being is because we now have a record for it. 
</p>
<br />
