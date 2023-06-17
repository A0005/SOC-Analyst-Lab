<h1>Setting up Win 11 VM<h/1>


<h2>Description</h2>
This project demonstrates how to setup Windows 11 virtual machine for this lab.
<br />


<h2>Environments Used </h2>

- <b>VMware Fusion</b>
- <b>Windows 11</b>

<h2>Program walk-through:</h2>

<!-- <p align="center"> --!>
1 - Open Vmware Fusion and select the + sign then select Import. <br/>
<img width="900" alt="1" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/35522098-2f7a-4cef-b732-7c888145c8c2">
<br />
2	- Select Choose File... <br/>
<img width="900" alt="2" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/facff241-332c-4c5c-b5e8-53898774b5cf">
<br />
3	- Browse to the WinDev2305Eval.ovf that you downloaded and select it. <br/>
<img width="900" alt="3" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/81e372b3-96be-45c2-ab03-f36660834dfd">
<br />
4 - Select Contiune. <br/>
<img width="900" alt="4" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/5fabdda8-a49a-421e-b7cf-f7bea56fb48d">
<br />
5 - Give the VM a name and choose where to store it. <br/>
<img width="900" alt="5" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/36f79c1e-e356-4297-87c0-020c113e6db6">
<br />
6 - Depending on your host machine, you can edit some of these settings by click on Customize Settings or if you are okay with it select Finish. <br/>
<img width="900" alt="6" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/a78601bc-3e30-4569-9902-8eec5e4a01f0">
<br />
7 - Start up your Windows 11 machine and after it goes through the installation process it will log in and this is what you will see.  <br/>
<img width="900" alt="7" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/b43a1b89-2761-4c80-8663-86b6fec8c76c">
<br />
8 - Click the start menu icon and select settings.   <br/>
<img width="900" alt="8" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/3194ac85-76c5-466e-9a53-3fa5f55d7144">
<br />
9 - Select Privacy & security on the left.  <br/>  
<img width="900" alt="9" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/0d0bf4eb-58f9-4783-86c5-7cb6eba2463d">
<br />
10 - Select Windows Security. <br>
<img width="900" alt="10" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/109c184b-5bf5-4daa-89ce-de0ec40436ef">
<br />
11 - Select Virus & threat protection. <br/>
<img width="900" alt="11" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/8a0bffe3-ff25-4b58-98aa-5490b37e4851">
<br />
12 - Under Virus & threat protection settings select Manage settings. <br/>
<img width="900" alt="12" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/3b63dc27-f9bd-421f-bf6d-fb27109468b9">
<br />
13 - Toggle OFF the Real-time protection, Cloud-delivered protection, Automatic sample submission, & Tamper Protection switch.  <br/>
<img width="900" alt="13" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/d99da241-6829-41d3-baa1-e9b933d92d02">
<br />
14 - When prompted, click “Yes” for all. <br/>
<img width="900" alt="14" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/3a1f9bab-4ae7-4d83-9543-7c3a28c9ca5a">
<br />
15 - Search cmd on the search bar and select Run as administrator. <br/>
<img width="900" alt="15" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/e0a11c97-865c-430d-8f2b-e2a4a7efe6e9">
<br />
16 - Click Yes. <br/>
<img width="900" alt="16" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/f998b53b-984e-432e-a23f-194001d81e7e">
<br />
17 - Run the following command gpedit.msc and then inside the Local Group Policy Editor open Computer Configuration > Administrative Templates > Windows Components > Microsoft Defender Antivirus and double-click Turn off Microsoft Defender Antivirus. <br>
<img width="900" alt="17" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/68b45c29-2058-4faf-a73d-7ede414b5aa5">
<br />
18 - Select Enabled then click on Apply and OK. <br/>
<img width="900" alt="18" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/6723ec36-82aa-4815-acdc-2b193ab3ac75">
<br />
19 - Back in the cmd run the following command > REG ADD "hklm\software\policies\microsoft\windows defender" /v DisableAntiSpyware /t REG_DWORD /d 1 /f  <br/>
<img width="900" alt="19" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/60ae998d-8631-4258-bdee-7faf44978427">
<br />
20 - Search msconfig on the search bar and select System Configuration. <br/> 
<img width="900" alt="20" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/2e2fbe3f-87ee-4ee3-a919-d237591cf805">
<br />
21 - Go to Boot tab and check the box for Safe boot and minimal. Then click Apply and OK. <br/>
<img width="900" alt="21" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/15f27fc2-cc1b-48cd-b1db-53e868d10d47">
<br />
22 - Select Restart. <br/>
<img width="900" alt="22" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/5a46ae2c-0dd9-4cc2-a664-c30c4c55a01c">
<br />
23 - Search regedit on the search bar and select Registry Editor. <br/>
<img width="900" alt="23" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/f45e33ea-2f3f-4c00-a009-36d1d9f1a9ef">
<br />
24 - Browse to Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Sense and set the value to 4. <br/>
<img width="900" alt="24" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/e9b4267f-4438-4bbf-934a-bb53767abe56">
<br />
25 - Browse to Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\WdBoot and set the value to 4. <br/>
<img width="900" alt="25" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/33d1c194-3c0d-468f-a10d-8aa80b1fa33d">
<br />
26 - Browse to Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\WdNisDrv and set the value to 4. <br/>
<img width="900" alt="26" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/0ebda0d0-30c7-4f0d-a5ee-dd9d3ab32df2">
<br />
27 - Browse to Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\WdNisSvc and set the value to 4. <br/>
<img width="900" alt="27" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/148d3fbe-531d-4ff3-97ba-0cc0a59f92b3">
<br />
28 - Browse to Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\WdFilter and set the value to 4. <br/>
<img width="900" alt="28" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/caa54f1b-d8a5-41ed-8309-4e893f582ed0">
<br />
29 - Browse to Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\WinDefend and set the value to 4.<br/>
<img width="900" alt="29" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/c51cc961-7ddf-4b43-9178-a2b53b6e1448">
<br />
30 - Search msconfig on the search bar and select System Configuration. <br/>
<img width="900" alt="30" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/089db2f5-70fe-49e0-818c-4a1c51b46aa0">
<br />
31 - Go to Boot tab and uncheck the box for Safe boot and minimal. Then click Apply and OK. When prompted select restart. <br/>
<img width="900" alt="31" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/b52c609d-bb40-40ef-8692-b35b6dc2c68a">
<br />
32 - Open cmd and run the following commands > powercfg /change standby-timeout-ac 0 > powercfg /change standby-timeout-dc 0 > powercfg /change monitor-timeout-ac 0 > powercfg /change monitor-timeout-dc 0 > powercfg /change hibernate-timeout-ac 0 > powercfg /change hibernate-timeout-dc 0 <br/>
<img width="900" alt="32" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/e52d4d49-2287-4daf-b398-384c1d13f21e">
<br />
33 - Search powershell on the search bar and select Run as Administrator. <br/>
<img width="900" alt="33" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/ddc7df5b-9f5b-4c53-bb65-20451866028d">
<br />
34 - Select Yes. <br/>
<img width="900" alt="34" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/2f6cba9e-9fa1-4ab0-98ba-fc826e3a7a01">
<br />
35 - Download Sysmon with the following command > Invoke-WebRequest -Uri https://download.sysinternals.com/files/Sysmon.zip -OutFile C:\Windows\Temp\Sysmon.zip <br/>
36 - Unzip Sysmon.zip > Expand-Archive -LiteralPath C:\Windows\Temp\Sysmon.zip -DestinationPath C:\Windows\Temp\Sysmon <br/>
37 - Download SwiftOnSecurity’s Sysmon config > Invoke-WebRequest -Uri https://raw.githubusercontent.com/SwiftOnSecurity/sysmon-config/master/sysmonconfig-export.xml -OutFile C:\Windows\Temp\Sysmon\sysmonconfig.xml <br/>
38 - Install Sysmon with Swift’s config > C:\Windows\Temp\Sysmon\Sysmon64.exe -accepteula -i <br/>
39 - Validate Sysmon64 service is installed and running > Get-Service sysmon64 <br/>
40 - Check for the presence of Sysmon Event Logs > Get-WinEvent -LogName "Microsoft-Windows-Sysmon/Operational" -MaxEvents 10 <br/>
<img width="900" alt="35" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/90237ac8-04b0-4c2b-b4f3-a56a8f81d1aa">
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
