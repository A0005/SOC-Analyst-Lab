<h1>Creating attacks and Detecting them<h/1>


<h2>Description</h2>
In this project we are going to steal credentials on a system and detect them.
<br />


<h2>Environments Used </h2>

- <b>VMware Fusion</b>
- <b>Linux Server 22.04.2</b>
- <b>Windows 11</b>
- <b>Lima Charlie</b>

<h2>Program walk-through:</h2>

<!-- <p align="center"> --!>
1 - On your ssh client run > getprivs (to make sure the SeDebugPrivilege is available) then run > procdump -n lsass.exe -s lsass.dmp (here we are going to steal credentials on a system). <br/>
2 - This will dump the remote process from memory, and save it locally on your Sliver C2 server. (if you see a RPC error don’t worry and continue on). <br/>
<img width="900" alt="1" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/f5679195-cd77-4791-b029-33b8b58f2308">
<br />
3	- Let's detect the attack by opening Lima Charlie on the web browser and choose sensors from the left side > then your hostname > timeline from the left side > and in the Event Type Filters filter for SENSITIVE_PROCESS_ACCESS <br/>
<img width="900" alt="2" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/a8194a5f-9730-4a6b-88c9-013f79c66652">
<br />
4	- Pick any event to see what the event looks like when credential access has occurred. Then select Build D&R Rule to create a rule that alerts us anytime this activity occurs. <br/>
<img width="900" alt="3" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/e9cdb3a2-6c98-4e20-9717-293b4c54329a">
<br />
5 - In the Detect section replace the whole contents with this > event: SENSITIVE_PROCESS_ACCESS op: ends with path: event/*/TARGET/FILE_PATH value: lsass.exe (this means to detect only SENSITIVE_PROCESS_ACCESS events where the victim or target process ends with lsass.exe). <br/>
6 - In the Respond section replace the whole contents with this > - action: report name: LSASS access (this will simply generate a detection report anytime this detection occurs in Lima Charlie). <br/>
7 - Then select Target Event at the bottom. <br/>
<img width="900" alt="4" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/a7493d51-2758-4bea-89b2-53009dd4aa5f">
<br />
8 - Scroll all the way down and select Test Event. You can see that a Match and the D&R engine tells you exactly what it matched on. <br/>
<img width="900" alt="5" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/3563640e-2b5a-4f02-9194-dc76a1863298">
<br />
9 - Scroll all the way up and select Save Rule. <br/>
<img width="900" alt="6" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/b8eb4b12-7f9e-4c82-896d-8eb186daf147">
<br />
10 - Name it LSASS Accessed and make sure it is enabled. <br/>
<img width="900 alt="7" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/4b2b253e-5461-45c2-89af-9a4358b3dc26">
<br />
11 - Let's create another attack so Lima Charlie detects the rule we just created. Back in the ssh client run > procdump -n lsass.exe -s lsass.dmp <br/>
<img width="900" alt="8" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/5df0c867-fe21-40cc-bc5d-04958f14cbe1">
<br />
12 - Back on Lima Charlie select the Deceptions tab to see the threats that have been detected. <br/>  
<img width="900" alt="9" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/0338d6a6-6706-465e-8417-2482dfa97b0e">
<br />
13 - Select one of the events to see the raw details that have occurred. <br>
<img width="900" alt="10" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/02f6824f-d636-4067-ad0c-bacc1214cbed">
<br />
14 - To see the exact timeline where the detection took place select View Event Timeline. <br/>
<img width="900" alt="11" src="https://github.com/A0005/SOC-Analyst-Lab/assets/103763124/676e5dfd-60ed-45c6-acc1-61d859e4c9d1">
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
