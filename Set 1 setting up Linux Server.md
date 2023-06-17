<h1>Installing Linux Server<h/1>


<h2>Description</h2>
This project demonstrates how to install a Linux Server on VMware Fusion.
<br />


<h2>Environments Used </h2>

- <b>VMware Fusion</b>
- <b>Linux Server 22.04.2</b>

<h2>Program walk-through:</h2>

<!-- <p align="center"> --!>
1 - Open Vmware Fusion and select the + sign then select New. <br/>
<img width="900" alt="1" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/08fafc5e-5b24-4ccf-9654-28eb27168c70">
<br />
2	- Select Create a custom virtual machine then continue. <br/>
<img width="900" alt="2" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/f8da634c-0443-468f-b442-5e7a36bc6436">
<br />
3	- Select Linux then Ubuntu 64-bit then continue. <br/>
<img width="900" alt="3" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/09a91bbc-d062-4f06-87a8-fb043b7fbe6e">
<br />
4 - Select Contiune. <br/>
<img width="900" alt="4" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/8a5778a3-bac1-497b-afdf-cf2696705344">
<br />
5 - Select Customize Settings. Name your VM and choose where to store it then select Save. <br/>
<img width="900" alt="5" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/f1d137a9-2339-40c5-8f00-f587e6f9bc59">
<br />
6 - Select Network Adapter. <br/>
<img width="900" alt="6" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/12cddcd3-61a4-40bd-9621-54c7ef578b75">
<br />
7 - Select Autodetect then choose Show All from the top bar.  <br/>
<img width="900" alt="7" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/423ef575-e152-4c8a-ad26-e68f9e2db442">
<br />
8 - Select Processors & Memory. Change the ram to 2GB then choose Show All from the top bar.  <br/>
<img width="900" alt="8" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/e5475988-81e3-4c5d-8520-8bbcdfdc3e2c">
<br />
9 - Select Hard Disk (SCSI). Change the Hard Disk to 14GB then choose Show All from the top bar.  <br/>  
<img width="900" alt="9" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/94790f5b-02c3-4478-ab7a-777da1addacf">
<br />
10 - Select CD/DVD (SATA). Check the box Connect CD/DVD Drive then browse to your Linux ISO and select it. Then close this box. <br>
<img width="900" alt="10" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/b69a7f78-3c04-47a5-abf3-310633786aa1">
<br />
11 - Start your Linux Server VM and select the first option. <br/>
<img width="900" alt="11" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/5e883e35-a96a-4b7f-aae6-331f98efb6fe">
<br />
12 - Choose your preferred language then hit enter. <br/>
<img width="900" alt="12" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/1b8ab687-95cb-4d73-ae91-57c0e44a257c">
<br />
13 - Choose Contiune without updating and hit enter. <br/>
<img width="900" alt="13" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/878abaab-e0d2-48f6-bc95-80f0f751c973">
<br />
14 - Keep the default and choose Done then hit enter.  <br/>
<img width="900" alt="14" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/b426cad6-ba2c-4cb1-a3d7-0da0f50747cb">
<br />
15 - Keep the default and choose Done then hit enter. <br/>
<img width="900" alt="15" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/1f24a52a-99a0-4e9b-ae17-344434e50a5b">
<br />
16 - Use your down arrow key to select your network card name enss eth. <br/>
17 - Select Manual then choose IPv4 Method. Enter your subnet mask - set an static IP - enter your gateway - for the name server enter 8.8.8.8 <br>
<img width="900" alt="16" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/a49e3d48-9d1a-4308-89b9-5a36cd1e8737">
<br />
18 - Choose done and hit enter. <br/>
<img width="900" alt="17" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/bf76b71f-4097-42cc-b1ac-3ef998bfae57">
<br />
19 - Keep the default and choose Done then hit enter.  <br/>
<img width="900" alt="18" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/3571e3c4-6cf8-458e-9f2e-c6ce22c5c3dc">
<br />
20 - Keep the default and choose Done then hit enter. <br/> 
<img width="900" alt="19" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/b98606c8-575c-4b1b-b355-f973911773bc">
<br />
21 - Keep the default and choose Done then hit enter. <br/>
<img width="900" alt="20" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/a954c142-0674-482d-997b-206a75e52b02">
<br />
22 - Keep the default and choose Done then hit enter. <br/>
<img width="900" alt="21" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/9fc57530-52e2-4bb2-87ae-9161487b23eb">
<br />
23 - Choose Contiune and hit enter. <br/>
<img width="900" alt="22" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/11b6f4ab-0756-4bc6-8aac-36a1ec1d2148">
<br />
24 - Enter the following details > user - attack - user - password - password. Then choose Done and hit enter. <br/>
<img width="900" alt="23" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/afe80fa0-86d8-4097-8ef5-a543bb03e038">
<br />
25 - Keep the default and choose Done then hit enter. <br/>
<img width="900" alt="24" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/6cf843fb-9b9a-4e6d-a04c-2f8b6c03d88c">
<br />
26 - Hit enter on Install OpenSSH server then choose Done and hit enter. <br/>
<img width="900" alt="25" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/a658de11-450b-40d2-a94a-6acf5cab1145">
<br />
27 - User your down arrow key to choose Done and hit enter. <br/>
<img width="900" alt="26" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/f7f399f9-3889-4f69-97cd-208850dc4cc6">
<br />
28 - When the installation is complete choose Reboot Now and hit enter. <br/>
<img width="900" alt="27" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/634a3b5d-62c4-4970-b26e-e7ca479a2e4b">
<br />
29 - Hit enter. <br/>
<img width="900" alt="28" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/c7800b4b-715b-4069-bc13-3629d3953d97">
<br />
30 - Enter the user name and password. <br/>
<img width="900" alt="29" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/046718a2-b01f-4f67-bdfa-ec97fc64142b">
<br />
31 - Type ping -c 2 google.com and make sure it is successful. <br/>
<img width="900" alt="30" src="https://github.com/A0005/SOC-Analyst-Fundamentals/assets/103763124/0575d644-c2fa-45cf-a7ac-6e17385f7a67">
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
