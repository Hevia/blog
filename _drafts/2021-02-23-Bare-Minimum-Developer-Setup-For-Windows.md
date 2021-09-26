# Bare Minimum Developer setup for Windows

I really enjoy developing on Windows, throughout college I would try to adopt some flavor of Linux, and the desire to stick around never stayed. I grew up with Windows, I was really comfortable navigating & troubleshooting the OS.

The odd gatekeeping against Windows users that happens in CS education can be really off-putting for some. Making folks feel inferior for not using Arch. Hopefully this guide can get you feeling productive without having to troubleshoot your audio drivers. 

**Disclaimer:** At the time of writing this blog post I work for Microsoft. Although I liked Windows before I joined too 😊

## What this guide is not
This isn't a guide defending Windows, if you want to use Linux go ahead. This is just guide on getting the most out of Windows as a developer. Your mileage may vary.

Even if Windows is your primary workstation, it is still helpful to know how to navigate a Linux environment. Chances are it is where your code will be deployed. 

## WSL2

It is a cruel irony that to get the most out of a dev experience on Windows you have to use Linux. Windows Subsystem for Linux allows you to have a Linux developer environment that is seamless to access and use.
  
The first thing I do on any new Windows machine is get WSL2 up & running. It will come back to save you many times over. VSCode & other tools integrate nicely with WSL2 as well.   
  
WSL2 is normally not enabled by default, and some versions of Windows might not support it. [Follow this guide to enable it.](https://docs.microsoft.com/en-us/windows/wsl/install-win10) 

## Package Managers

For the uninitiated, a package manager is a software suite that automates the installation/upgrades of software on your computer.(If you use Steam, it is a lot like that!) It is a feature that has been missing from Windows for a long, and is one of the nice amenities of Linux. 

[WinGet](https://docs.microsoft.com/en-us/windows/package-manager/) is Microsoft's package manager based off of another community developed package manager [AppGet](https://appget.net/), but as of the writing of this blog it is currently in preview.   
  
I personally use a combination of [chocolatey](https://chocolatey.org/) and [scoop](https://scoop.sh/) + [scoop extras](https://github.com/lukesampson/scoop-extras). I primarily use scoop, but some software works better when installed with chocolately. The latter has a paid plan that I have never needed to use. There are some security concerns with the elevated permissions you need to run these package managers.

If you're going to install software across multiple drives, make sure you specify that before installing. 

## Software

- [VSCode]()
- [Visual Studio]()
- [Anki]()
- [Windows Terminal]()
- [Windows PowerToys]() 
- [Git]() I install Git using scoop. For a full list of commands check out the Appendix.

## Telemetry, Privacy & OS settings

Windows has telemetry & data collection settings on by default. You can disable these in settings, but it is easy to miss them. Along with some pre-installed apps that certain distributions of Windows might have (looking @ Candy Crush).

[PrivateZilla](https://github.com/builtbybel/privatezilla) makes it really easy to tweak what settings to toggle/software to uninstall. Read the README.md first! I don't turn off much, but I do use it to get rid of some pre-installed apps primarily.


## Languages

I don't use many languages outside of work, but here are a few I make sure I install on every run. 

- [Python]() I use the .exe installer. I've run into the odd bug when using package managers.
- [Rust]() You need to install some prereqs before hand, I install Rust to both Windows & WSL
- [Node.js](https://nodejs.org/en/) Install using whatever method you like. 
- [Docker]()  


## Conclusion

For those who stuck around, I hope this guide was of some use. This guide was meant to bring some awareness to a lot of the features that make Windows a lot more enjoyable to use as a developer. 


### Appendix A: List of commands
I don't have any automation setup yet, but here is my current setup. Open a Powershell instance in admin. You might need to restart your shell after installing a package manager.
```
> Set-ExecutionPolicy RemoteSigned -scope CurrentUser
> Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')
> Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
> choco install anki -y
> choco install powertoys -y
> scoop install git
> scoop bucket add extras
> scoop install calibre flux dopamine ghostwriter 

```

### Appendix B: About Macs...
No comments on Macs, if you want to release a product on their platforms at this point you are required to have one. 



