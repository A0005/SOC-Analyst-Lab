<h1>Performing an attack then blocking it<h/1>


<h2>Description</h2>
In this project we are going to perform an attack and then create a rule to block it when executed.
<br />


<h2>Environments Used </h2>

- <b>VMware Fusion</b>
- <b>Linux Server 22.04.2</b>
- <b>Windows 11</b>
- <b>Lima Charlie</b>

<h2>Program walk-through:</h2>

<!-- <p align="center"> --!>
1 - On your ssh client run > shell when prompted with This action is bad OPSEC, are you an adult? type Y and hit enter. <br/>
2 - Run > vssadmin delete shadows /all (the output is not important) then run > whoami (to verify we still have an active system shell). <br/>
<img width="900" alt="1" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/c090112c-cf4f-40b4-9a37-3c86039b2ac6">
<br />
3	- On Lima Charlie select the Detection tab from the left side to see if it picked up any of our attacks. <br/>
<img width="900" alt="2" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/59e7b50e-fd8d-4cf9-89ac-59999530a681">
<br />
4	- Select the event named Shadow Copies Detection... to see the metadata contained within the detection itself. <br/>
<img width="900" alt="3" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/4d898c29-5e45-40fa-a99f-e0740d2d43f8">
<br />
5 - Click View Event Timeline (to see the raw event that generated this detection) then select Build D&R Rule (to create a rule). <br/>
<img width="900" alt="4" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/df2d191f-7b72-4afa-8642-23558436b0a1">
<br />
6 - In the Respond section add - action: report > name: vss_deletion_kill_it > - action: task > command: > - deny_tree > - <<routing/parent>> <br/>
7 - Then select Save Rule. <br/>
<img width="900" alt="5" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/1dfdbbb6-5675-4706-abf7-7cc45a16787f">
<br />
8 - Name it (vss_deletion_kill_it) then select Save. <br/>
<img width="900" alt="6" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/6cb68e41-b298-4867-b9dd-09ae00d099b2">
<br />
9 - Back in your ssh client run > vssadmin delete shadows /all <br/>
10 - Now run > whoami (to test if your D&R rule properly terminated the parent process). <br/>
11 - If your D&R rule worked the system shell will hang or exit and fail. <br/>
<img width="900" alt="7" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/e96d7f3c-f0e4-4aa2-8448-c54f2dbf9244">
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
