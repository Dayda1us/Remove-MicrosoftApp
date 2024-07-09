# Remove-MicrosoftApp
When you install a fresh copy of Windows 10/11, Windows will come with preinstalled Microsoft apps that you may not want. The script will allow you to remove any unwanted Microsoft apps that you do not use.

## ⚠️Disclaimer
It is advised not to use PowerShell 7 to run this script as you'll receive a loop of error messages as shown below:

![image](https://github.com/Dayda1us/Remove-MicrosoftApp/assets/145280599/294fce56-023b-4771-ba98-fe86c4275d6d)

These error message occur due to PowerShell 7 not imported the Appx module. Attempting to import the Appx module will output an error message stating the operation is not supported on this (PowerShell 7) platform:

![image](https://github.com/Dayda1us/Remove-MicrosoftApp/assets/145280599/bc297c68-bb27-4cde-b243-67ffac98929d)

Therefore, it is recommended that you run this script on Windows PowerShell rather than PowerShell 7. This script also requires that the execution policy is set to RemoteSigned.

## How to run the script
1. Download the Remove-MicrosoftApp.ps1 script
2. Make the necessary edits on the editable variables using Visual Studio Code (VSCode) or any other IDE of your preference
3. Run Windows PowerShell as an administrator. Enter your administrative credentials if User Account Control (UAC) requires it
4. Verify if the execution policy is set to RemoteSigned by typing this command: Get-ExecutionPolicy
![image](https://github.com/Dayda1us/Remove-MicrosoftApp/assets/145280599/248633c0-cb3c-4230-b8ac-e17c52c32ca7)
5. If the execution policy is set to RemoteSigned, please skip to step 7. Otherwise, type in the following command: Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
6. You will be prompted if you like to change the execution policy to RemoteSigned, type "A" and press "Enter". The execution policy is now set to RemoteSigned
![image](https://github.com/Dayda1us/Remove-MicrosoftApp/assets/145280599/7564adc0-fadd-4686-a03b-72adbad75ebe)
7. Change the directory to where Remove-MicrosoftApp.ps1 was downloaded
8. Type in the following: .\Remove-Microsoft.ps1
9. Wait for the script to finish removing the unwanted Microsoft apps
10. Verify if the Microsoft apps that you don't want is successfully removed
11. (Optional) Set the execution policy back to Restricted by typing the following command: Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Undefined. Type "A" and press "Enter" to apply the changes
