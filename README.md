# Windows 11 Debloat & Setup Guide

> **If you just got a Windows 11 device, you might want to debloat it—remove unnecessary software like Internet Explorer, preinstalled antiviruses (e.g., McAfee trials), and change the default privacy settings.**  
>  
> I’m not offering a custom tool here; instead, I’m guiding you through using existing tools and guides to get your system exactly how you want it.

---

## ⚠️ Disable S Mode Before Continuing

If you can’t download or run apps from the internet, your device might be locked in **S Mode**. To exit S Mode, follow these steps:  
[Turn off S Mode](https://ysu.teamdynamix.com/TDClient/2000/Portal/KB/ArticleDet?ID=164015)

---

## Table of Contents

- [Tweaks & Configurations](#tweaks--configurations)
- [Installing Applications (Optional)](#installing-applications-optional)
- [Uninstalling Unwanted Applications](#uninstalling-unwanted-applications)
- [Changing Startup programs](#changing-startup-programs)
- [Other Unwanted Programs](#other-unwanted-programs)
- [Congratulations!](#congratulations!)
- [Feedback & Support](#feedback--support)

---

## Tweaks & Configurations

### Using Winutil to Debloat Windows 11

We’ll use **Chris Titus Tech's winutil** to disable unwanted settings and uninstall bloatware.  
[Winutil on GitHub](https://github.com/ChrisTitusTech/winutil)

#### How to Run Winutil

1. **Open PowerShell in Administrator Mode**  
   Right-click the PowerShell icon and choose **Run as administrator**.

2. **Execute the Command**

   ```powershell
   irm "https://christitus.com/win" | iex
> Note:
> 
> - irm is an alias for Invoke-RestMethod, which fetches the script from the URL.
> - The pipe | passes the script to iex (Invoke-Expression) to execute it.
> - This command doesn’t “install” winutil; run it each time you use it.
> This will begin loading the app. It does not install, so running this command everytime you use it is necessary.
>


You will first see something like this:
![image](https://github.com/user-attachments/assets/da332e48-915c-4a8b-b3f2-321a42d0b5ba)

Selecting Tweaks
Navigate to the Tweaks tab in winutil and select the following options:

## Essential Tweaks:

    - Create Restore Point
      > Backup in case something goes wrong.
    - Disable Recall
      > Disables Windows 11’s AI screenshot feature. 10,000% recommend turning this off.
    - Disable Wifi-sense
      > Prevents auto-connecting to shared networks (especially important for laptops) I recommend reading this: [ https://www.techtarget.com/searchenterpriseai/feature/Privacy-and-security-risks-surrounding-Microsoft-Recall ]
    - Set Hibernation as Default
      > Good for laptop battery life.
    - Set Services to Manual
      > Stops unnecessary background processes.
    - Disable Location Tracking
    - Disable GameDVR
      > (Optional) – Skip if you need Xbox features.
    - Disable Telemetry
      > Prevents intrusive data collection (note: this may affect Edge, but you DO NOT want to be using Edge anyways.).
    - Debloat Edge
      > Removes or limits spying features in Microsoft Edge.
## Advanced Tweaks
    - Disable Background Apps
      > Stops Microsoft Store apps from running in the background.
    - Disable Microsoft Copilot
    - Disable Intel MM (vPro LMS)
      > Mitigates potential massive network security risks. [ https://christitustech.github.io/winutil/dev/tweaks/z--Advanced-Tweaks---CAUTION/DisableLMS1/ ]
    - Disable Notification Tray/Calendar
      > (Optional) – If you prefer a cleaner interface.
    - Set Display for Performance
      > (Optional) – Optimizes settings for performance.
    - Set Classic Right-Click Menu
    - Remove Microsoft Edge
      > Prevents Edge from reinstalling with updates.
    - Block Razer Software Installs (peripherals still work without the bloatware)
    - Remove OneDrive (finally)
- After making your selections, click Run Tweaks at the bottom.
- This process may take some time and might restart your computer.

## Preferences Tab:
Winutil also has a Preferences tab where you can adjust settings that apply automatically.
Here is mine incase you wanna pick my brain apart:

![image](https://github.com/user-attachments/assets/fce46e75-44a2-43a2-acdb-c7bad6b5f723)

Tip: Don’t be alarmed if your screen takes a moment to reset after a new tweak. Your computer needs time to refresh all systems after changes like these.

## Configurations
Switch to the Config tab to adjust additional settings. Recommended actions include:

  > -Disable Search Box Web Suggestions in Registry
  > -Prevents app searches from redirecting to Internet Explorer.
Under Fixes:
  > -Select Remove Adobe Creative Cloud to eliminate unwanted Adobe software.


### Installing Applications (Optional)

  > - This section is optional and reflects my personal recommendations for a fresh Windows 11 setup.

# Recommended Applications
  Browsers:
  
    > Advanced Security: Brave
    > For Speed: Chromium
    > Basic Secure Browsing: Firefox (NOT ESR)

  Communications:
  
    > Discord (as needed)

  Development Tools:
  
    > Miniconda (for Python)
    > GitHub Desktop
    > JetBrains Toolbox
    > Python Version Manager
    > Python3
    > Sublime Text
    > VS Code
  Document Editing:
  
    > Obsidian
    > LibreOffice
    > Foxit PDF Editor
  Games (Preferences):
  
    > Cemu
    > EA App
    > Epic Games Launcher
    > GeForce NOW
    > Itch.io
    > Steam
    > XEMU
  Microsoft Tools (Preferences):
  
    > Autoruns (startup manager)
    > NuGet
 
  Multimedia Tools (Preferences):
  
    > Audacity (music production)
    > FFMPEG
    > GIMP (free Photoshop alternative)
    > OBS Studio (livestreaming/recording)
    > Spotify
    > VLC Video Player
  
  Pro Tools (Preferences):
  
    > - WireGuard
  
  Utilities (Preferences):
  
    > - 7Zip
    > - Ambie White Noise
    > - Bitwarden
    > - Borderless Gaming
    > - Etcher (USB creator)
    > - Malwarebytes (Note: May show corner popups; tray notifications are disabled)
    > - WinRAR
After selecting your desired apps, click Install/Upgrade Selected.
Be patient—this installs many applications at once!

## Uninstalling Unwanted Applications
To remove bloatware that you don’t need:

Under the Install tab, select:

    > - Microsoft Edge
    > - Google Chrome
    > - Slack
    > - Signal
    > - Microsoft Teams
    > - OneDrive
    > - iTunes

Click Uninstall Selected and wait for the process to complete.


### Changing Startup Programs ###
TO view what programs run at startup, and change them, open up **Task Manger** and head to the ***"StartUp"*** tab. 
Here is a sample of what that looks like.


![image](https://github.com/user-attachments/assets/cf5e4bed-3fb1-49b0-9069-2e351ed496b6)





You can right click and disable any application you dont want to automatically open when your computer starts, from here.


### Other Unwanted Programs ###
   You may have other programs that you dont wish to have on your computer, such as McAfee The simplist way to attempt to uninstall a program is through the settings. This wont always work of course, as Edge isnt an option to uninstall here, amongst some others. (fun little fact about microsoft there)
   > Start > Settings > Apps > Apps and Features
    - Search "McAfee"
   > Right click and uninstall McAfee Antivirus (basically malware itself)


### Congratulations! ###
  Your machine should now be far cleaner and better optimized for use.
  Please open an issue or contact me if you find any problems / suggestions to add.
  Install mint xfce when you want a real computer (jk lol)


