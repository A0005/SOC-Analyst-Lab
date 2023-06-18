<h1>Setting up an Attack System <h/1>


<h2>Description</h2>
This project demonstrates how to setup Sliver Linux on Ubuntu Server.
<br />


<h2>Environments Used </h2>

- <b>VMware Fusion</b>
- <b>Ubuntu Server 22.04.2</b>

<h2>Program walk-through:</h2>

<!-- <p align="center"> --!>
1 - Start your Ubuntu Server VM. <br/>
<img width="900" alt="1" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/d10d3b56-8e2a-4249-a03f-ba3a63c00f72">
<br />
2	- Open your preferred ssh tool and run > ssh user@[Linux_VM_IP]. When prompted login into your user account. <br/>
<img width="900" alt="2" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/be5e9729-9158-4a1e-bbd5-82edc69b6a36">
<br />
3	- Run > sudo su then run > # Download Sliver Linux server binary wget https://github.com/BishopFox/sliver/releases/download/v1.5.34/sliver-server_linux -O /usr/local/bin/sliver-server # Make it executable chmod +x /usr/local/bin/sliver-server # install mingw-w64 for additional capabilities apt install -y mingw-w64 <br/>
<img width="900" alt="3" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/a7dc8116-b848-4c11-9bfa-2316ab7cabfc">
<br />
4 - Run > # Create and enter our working directory mkdir -p /opt/sliver <br/>
<img width="900" alt="4" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/9eddf39c-305a-45e9-8178-570ad26c8984">
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
