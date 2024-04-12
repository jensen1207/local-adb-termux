# local-adb-termux
The way you can use your local ADB within Termux in your Android:

**Step 1:**
Connect your Android device with your PC via USB port

**Step 2:**
Type command in ADB of PC side

`adb tcpip 5555`  
`adb connect <your Android IP>:5555`  
`adb disconnect <your Android IP>:5555`  

**Step 3:**
Type command in ADB of Android side（Install android-tools first）

`adb connect localhost:5555`

DONE!
ENJOY! 😸☕

# SSH Accesss your termux over Internet with your own VPS
The way you can access your Termux in your Android:  

**Step 1:**
Modify following parameter in `/etc/ssh/sshd_config` in your VPS  

`GatewayPorts yes`(Default is no)  

And restart sshd  
`service ssh restart`

**Step 2:**
Run following command in your local PC (We can name it **PC A**)  

`ssh -R <your-want-to-expose-port>:localhost:<your-SSH-port or other-application-port> -N <your-vps-login-name>@<your-vps-public-IP>`  

Example:  
`ssh -R 1234:localhost:22 -N root@1.2.3.4`  

May need input your vps user password


**Step 3:**
Connect to **PC A** with any SSH client in **PC B** as following input:  

`Host:<your-vps-domain>` (You may need apply for one)  
`Port:<your-want-to-expose-port>  `  
`User:PC A user  `  
`Password: PC A user password`  

Here we go!✈️
