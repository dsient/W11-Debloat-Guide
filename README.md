**IF** you have just gotten a device that has windows 11, you may want to debloat it of excess garbage, such as internet explorer, preinstalled antiviruses and trials such as mcaffee, and changing the weird and horrific privacy settings that come by default.
Since im just some random guy on the internet, im not going to give you some tool i have wrote myself, and instead i will just be guiding you through using other tools and guides, in one place, to get your system working exactly how you want it to.




### Steps
First things first, we will use Chris Titus Tech's winutil to disable settings and uninstall bloatware. 
> [https://github.com/ChrisTitusTech/winutil]

Open powershell in Administator mode (right click, run as admin)
enter 'irm "https://christitus.com/win' | iex' and press enter.
  > (irm is a alias for the powershell cmdlet "Invoke-RestMethod", sending an HTTP request to the given url, and retreives the content. It accessed christitus's powershell tool. the '|' is a pipe operator, outputs the first command "irm" into the next command, and then it called iex to take the collected script andf execute it (because of the pipe operator) )
> This will begin loading the app. It does not install, so running this command everytime you use it is necessary.

You will first see something like this:
