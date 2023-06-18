<h1>Setting up Lima Charlie<h/1>


<h2>Description</h2>
This project demonstrates how to setup up Lima Charlie.
<br />


<h2>Environments Used </h2>

- <b>VMware Fusion</b>
- <b>Windows 11</b>
- <b>Lima Charlie</b>

<h2>Program walk-through:</h2>

<!-- <p align="center"> --!>
1 - In your web browser navigate to https://app.limacharlie.io/signup choose create an account. <br/>
<img width="900" alt="1" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/52df47ea-c4c3-4002-98c8-098a2c4b5699">
<br />
2	- Enter your details. <br/>
<img width="900" alt="2" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/115bb2ae-1d07-42f9-b123-538cb6b4ea6a">
<br />
3	- Fill in the following details. <br/>
<img width="900" alt="3" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/f7e94803-d513-42f9-995a-13bea9a22229">
<br />
4 - Click Create Organization. <br/>
<img width="900" alt="4" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/a7d6fe53-b860-4ab2-acf4-53867be815e2">
<br />
5 - Fill in the following details. <br/>
<img width="900" alt="5" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/233fc647-0b1f-4f95-8c68-3da0a5dceb62">
<br />
6 - Click Add Sensor. <br/>
<img width="900" alt="6" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/6d057935-8512-4ce8-ada4-aa74ab314306">
<br />
7 - Scroll down and click Windows.  <br/>
<img width="900" alt="7" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/c9d87107-2161-4e51-adb5-d3d6899f0587">
<br />
8 - In the description enter Windows VM lab then select Create.   <br/>
<img width="900" alt="8" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/11f46e38-c500-49aa-bb3c-f18c307f1bb4">
<br />
9 - In the drop down select Windows VM lab and then click on select.  <br/>  
<img width="900" alt="9" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/db1f81cb-3a4b-46fe-b58d-4ae641c7a47b">
<br />
10 - Select x86-64.exe <br>
<img width="900" alt="10" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/93821efc-69c7-44aa-a638-7fe66909913a">
<br />
11 - On your Windows 11 VM on the search bar search for PowerShell and click on Run as Administrator. <br/>
<img width="900" alt="11" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/c1cbd783-33f2-4b57-bb5e-a642e0a19d8a">
<br />
12 - Select Yes. <br/>
<img width="900" alt="12" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/073ab6b3-cb51-4a7c-9ecf-3c6034b13be9">
<br />
13 - Run the following commands. cd C:\Users\User\Downloads > Invoke-WebRequest -Uri https://downloads.limacharlie.io/sensor/windows/64 -Outfile C:\Users\User\Downloads\lc_sensor.exe > cmd.exe  <br/>
<img width="900" alt="13" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/8ae3ed74-dfee-455b-8b14-a6044b3e49f9">
<br />
14 - Back on the web browser copy the command to run the installer in the PowerShell.  <br/>
<img width="900" alt="14" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/2284a4ed-0137-4469-a2f0-ded0aae50cdf">
<br />
15 - Run the command in PowerShell after completing you will get a message saying that the agent installed successfully. <br/>
<img width="900" alt="15" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/92af301d-b59d-4113-8b64-c3d6e815c727">
<br />
16 - Back on the web browser select Finish. <br/>
<img width="900" alt="16" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/6abb5318-5ca5-47ff-b8cb-b1e3145cf144">
<br />
17 - On the left side select Artifact Collection. <br>
<img width="900" alt="17" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/f8422a5e-afaa-4101-b391-75d89b3dee8a">
<br />
18 - Select Add Artifact Collection Rule. <br/>
<img width="900" alt="18" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/9f2e2a35-cff8-4b24-b98e-f23a65c5f347">
<br />
19 - Enter the following details then click Save Rule. <br/>
<img width="900" alt="19" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/6acd7045-5ebe-4203-b417-6bcf7cc68fda">
<br />
20 - Confirmation that the rule has been created. <br/> 
<img width="900" alt="20" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/94f69b89-aea5-4070-822c-30b1f3e88868">
<br />
21 - Open your virtual machine library, right click on the Windows 11 VM and choose Snapshots. Then click on the camera logo on the top bar to name your snapshot and finally select Take. <br/>
<img width="900" alt="21" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/998b2254-f32a-4ba5-a33e-0523d66a3cb4">
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
