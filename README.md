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


