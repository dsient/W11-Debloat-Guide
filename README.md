# Windows [10/11] Debloat & Setup Guide

> **If you just got a Windows 11 device, you might want to debloat it—remove unnecessary software like Internet Explorer, preinstalled antiviruses (e.g., McAfee trials), and change the default privacy settings.**  
>  
> I’m not offering a custom tool here; instead, I’m guiding you through using existing tools and guides to get your system exactly how you want it.

---

## ⚠️ Disable S Mode Before Continuing

If you can't download or run apps from the internet, your device might be locked in **S Mode**. To exit S Mode, follow these steps:  
[Turn off S Mode (Official Microsoft Guide)](https://support.microsoft.com/en-us/windows/switching-out-of-s-mode-in-windows-4f56d9be-99ec-6983-119f-031bfb28a307)

---

## Table of Contents

- [Tweaks & Configurations](#tweaks--configurations)
- [Installing Applications (Optional)](#installing-applications-optional)
- [Uninstalling Unwanted Applications](#uninstalling-unwanted-applications)
- [Changing Startup programs](#changing-startup-programs)
- [Other Unwanted Programs](#other-unwanted-programs)
- [Manual Windows Settings (Final Step)](#-manual-windows-settings-final-step)
- [Congratulations](#congratulations)
- [Feedback & Support](#feedback--support)

---

## Tweaks & Configurations

### Using Winutil to Debloat Windows 11

We'll use **Chris Titus Tech's winutil** to disable unwanted settings and uninstall bloatware.  
[Winutil on GitHub](https://github.com/ChrisTitusTech/winutil) | [Official Documentation](https://winutil.christitus.com/)

#### How to Run Winutil

1. **Open PowerShell in Administrator Mode**  
   - Press the **Windows key** on your keyboard
   - Type `PowerShell`
   - Right-click on **Windows PowerShell** and select **Run as administrator**
   - Click **Yes** if prompted by User Account Control

2. **Copy and Paste This Command**

   ```powershell
   irm "https://christitus.com/win" | iex
   ```

> **What does this do?**
> - `irm` downloads the winutil script from the internet
> - `iex` runs the downloaded script  
> - This does NOT permanently install anything - run this command each time you want to use winutil

3. **Wait for Winutil to Load**

You will see a window like this:

![image](https://github.com/user-attachments/assets/da332e48-915c-4a8b-b3f2-321a42d0b5ba)

---

## Selecting Tweaks

Click on the **"Tweaks"** tab at the top of the winutil window. This is where you'll disable unwanted Windows features.

**How to use:** Find each item listed below and **click the checkbox** next to it to select it.

### Essential Tweaks (Safe - Recommended for Everyone)

| Tweak | What it does (in plain English) |
|-------|--------------------------------|
| **Create Restore Point** | Creates a backup so you can undo changes if something goes wrong. **ALWAYS do this first!** |
| **Disable Telemetry** | Stops Windows from collecting data about how you use your computer |
| **Disable Wi-Fi Sense** | Stops Windows from auto-connecting to random shared networks |
| **Set Services to Manual** | Stops unnecessary background programs from running |
| **Disable Location Tracking** | Stops Windows from tracking where you are |
| **Disable Activity History** | Stops Windows from keeping a history of everything you do |
| **Disable ConsumerFeatures** | Stops Windows from auto-installing sponsored apps and showing ads |
| **Delete Temporary Files** | Frees up disk space by removing junk files |
| **Run Disk Cleanup** | Removes old Windows files you don't need |
| **Enable End Task With Right Click** | Adds a handy "End Task" option when you right-click apps on the taskbar |
| **Disable GameDVR** | Stops Xbox game recording feature (skip if you use Xbox features) |
| **Disable Storage Sense** | Stops Windows from automatically deleting your files |
| **Disable Powershell 7 Telemetry** | Stops PowerShell from sending usage data |
| **Prefer IPv4 over IPv6** | Can improve internet connection on some networks |


### Advanced Tweaks - AI & Cloud Features (Use with CAUTION)

> ⚠️ **Warning:** These tweaks make bigger changes to your system. Make sure you created a Restore Point first!

#### AI Features to Disable

| Tweak | What it does (in plain English) |
|-------|--------------------------------|
| **Disable Recall** | **CRITICAL!** Stops Windows from taking screenshots of everything you do. Major privacy concern - highly recommended! |
| **Disable Microsoft Copilot** | Removes Windows AI assistant completely |

#### Cloud Features to Disable

| Tweak | What it does (in plain English) |
|-------|--------------------------------|
| **Remove OneDrive** | Completely removes Microsoft cloud storage from your computer |
| **Disable Background Apps** | Stops Microsoft Store apps from syncing in the background |

#### Browser & Edge

| Tweak | What it does (in plain English) |
|-------|--------------------------------|
| **Edge Debloat** | Removes tracking features from Microsoft Edge |
| **Remove Microsoft Edge** | Completely removes Edge browser |

#### Performance & Interface

| Tweak | What it does (in plain English) |
|-------|--------------------------------|
| **Set Classic Right-Click Menu** | Brings back the full Windows 10 right-click menu |
| **Set Display for Performance** | Makes Windows look simpler but run faster |
| ⚡ **Set Hibernation as Default** | Better for laptop battery life |
| ⚡ **Disable Notification Tray/Calendar** | Removes distracting notifications |
| ⚡ **Remove Home and Gallery from Explorer** | Cleans up File Explorer sidebar |

#### Security & Privacy

| Tweak | What it does (in plain English) |
|-------|--------------------------------|
| **Disable Intel MM (vPro LMS)** | Closes a security hole in Intel computers |
| **Block Razer Software Installs** | Stops Razer bloatware |
| **Adobe Debloat** | Removes Adobe background processes |
| **Run OO Shutup 10** | Opens a tool for more privacy settings |

---

### Preferences Tab - More AI/Cloud Settings

Click the **"Preferences"** tab in winutil. These settings also help disable AI and cloud features:

| Setting | Recommendation |
|---------|---------------|
| **Bing Search in Start Menu** | Set to **Disable** - stops web searches when you use Start |
| **Widgets Button in Taskbar** | Set to **Disable** - removes the AI-powered news/weather widget |
| **Task View Button in Taskbar** | Set to **Disable** - removes timeline/virtual desktop button |

Here is an example of my preferences:

![image](https://github.com/user-attachments/assets/fce46e75-44a2-43a2-acdb-c7bad6b5f723)

---

### Running the Tweaks

1. After checking all the boxes you want, scroll to the bottom
2. Click the **"Run Tweaks"** button
3. **Wait patiently** - this may take several minutes
4. Your computer might restart automatically

> 💡 **Tip:** Don't worry if your screen flickers or goes black briefly. This is normal as Windows applies the changes.

---

## Configurations (Config Tab)

Switch to the **"Config"** tab to access additional settings:

**Features:**
     > - Enable .NET Framework 3.5 (if needed for older apps)
     > - Install Windows Sandbox (for safely testing unknown software)
     > - Install Hyper-V (for virtualization needs)
     > - Install WSL (Windows Subsystem for Linux)

**Fixes:**
     > - Run DISM and SFC scans (repairs Windows system files)
     > - Reset Windows Update (fixes stuck updates)
     > - Reset Network Settings (fixes connectivity issues)
     > - Run Adobe CC Cleaner Tool (removes Adobe Creative Cloud completely)

**Legacy Panels:**
     > - Quick access to classic Control Panel sections (Power, Sound, Network, etc.)


### Installing Applications (Optional)

     > - This section is optional and reflects my personal recommendations for a fresh Windows 11 setup.

# Recommended Applications (PREFERENCE)
  Browsers:
  
    > Advanced Security: Brave
    > For Speed: Chromium
    > Basic Secure Browsing: Firefox (NOT ESR)

  Communications:
  
    > - Discord (as needed)

  Development Tools:
  
    > - Miniconda (for Python)
    > - GitHub Desktop
    > - JetBrains Toolbox
    > - Python Version Manager
    > - Python3
    > - Sublime Text
    > - VS Code
 
  Document Editing:
  
    > - Obsidian
    > - LibreOffice
    > - Foxit PDF Editor
    
  Games (Preferences):
  
    > - Cemu
    > - EA App
    > - Epic Games Launcher
    > - GeForce NOW
    > - Itch.io
    > - Steam
    > - XEMU
    
  Microsoft Tools (Preferences):
  
    > - Autoruns (startup manager)
    > - NuGet
 
  Multimedia Tools (Preferences):
  
    > - Audacity (music production)
    > - FFMPEG
    > - GIMP (free Photoshop alternative)
    > - OBS Studio (livestreaming/recording)
    > - Spotify
    > - KDEN Live (video editor)
    > - VLC Video Player
  
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
  Install alpine linux =]

---

## Manual Windows Settings (Final Step)

Some AI and cloud features can't be disabled through winutil - you'll need to turn these off manually in Windows Settings. This is the **last step** after running all winutil tweaks.

### How to Open Settings
Press **Windows key + I** on your keyboard, or click Start > Settings

### Cloud Features to Disable

| Setting Location | What to Change |
|-----------------|----------------|
| **Settings > Accounts > Windows backup** | Turn OFF "Remember my apps" and "Remember my preferences" |
| **Settings > System > Clipboard** | Turn OFF "Clipboard history" and "Sync across devices" |
| **Settings > Privacy & security > Find my device** | Turn OFF "Find my device" |
| **Settings > Privacy & security > General** | Turn OFF all 4 toggles (advertising ID, language list, app launches, suggested content) |
| **Settings > Privacy & security > Diagnostics & feedback** | Turn OFF "Send optional diagnostic data" and "Tailored experiences" |
| **Settings > Privacy & security > Activity history** | Turn OFF "Store my activity history on this device" |

### AI Features to Disable

| Setting Location | What to Change |
|-----------------|----------------|
| **Settings > Privacy & security > Search permissions** | Turn OFF "Cloud content search" for both Microsoft and Work/School accounts |
| **Settings > Personalization > Taskbar** | Turn OFF "Copilot (preview)" if visible |
| **Settings > Apps > Startup** | Disable any AI assistants that auto-start |

> **Tip:** After making these changes, restart your computer to ensure everything takes effect.

---

### Feedback & Support ###
  - **Found a bug or outdated info?** [Open an issue](../../issues)
  - **Have a suggestion?** Pull requests are welcome!
  - **Last verified:** December 2025 (winutil v25.12.01)
  
> **Note:** This guide references [Chris Titus Tech's winutil](https://github.com/ChrisTitusTech/winutil) which is actively maintained. Check the [official documentation](https://winutil.christitus.com/) for the latest features.


