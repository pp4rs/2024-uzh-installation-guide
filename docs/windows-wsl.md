<!-- markdownlint-disable MD033 -->
<!-- see https://github.com/DavidAnson/markdownlint for code to enable or disable rules -->

# Windows Subsystem For Linux

!!! tip "Windows Users Only!"

    This page is only for those who are using Windows. Those with Mac or Linux operating systems can proceed to 'Command Line Tools.'

Windows Subsystem for Linux (WSL) is a feature in Windows 10 that enables you to use Linux command-line tools on your Windows system.
By installing this feature, everyone in the course will be able to run the same commands, and get the same output - an essential aspect of reproducibility.
We hope that you will continue to use the WSL features we introduce over the next three weeks after the course is over for your own research related computing.

The process for installing everything we need here is quite order dependent - follow the steps in the order they appear below.

!!! tip "Want More Information?"

    For more information about the Windows Subsystem for Linux, look [here](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

!!! warning "Up to Date Windows 10 Required!"

    To go further with this Installation Guide you need to have an up to date installation of Windows 10. 
    IT Services in the Econ Department have assured us, if you update Windows to the latest version in your UZH laptop everything that follows will work. 

    If you do not have a Windows 10 machine, [Contact us!](../contact/#questions-or-comments)

## Install the Windows Subsystem for Linux

1. Join the Windows Insider Program [here][windows-insiders]
2. Check that you have a recent build of Windows 10 (Build 20262 or above)
      * Open up the run command with the `Win + R` key combo
      * Type `winver` into the run command text box and hit `OK`.
      * You should now see a dialogue screen with a OS build number.
      * If the build number is older than 20262, update your windows to a later build.
3. Open PowerShell as an administrator and type

```bash
wsl --install
```
The --install command performs the following actions:

* Enables the optional WSL and Virtual Machine Platform components
* Downloads and installs the latest Linux kernel
* Sets WSL 2 as the default
* Downloads and installs the Ubuntu Linux distribution (reboot may be required)

You will likely be asked to restart your machine during this installation process.

If you get error messages, you can check the [troubleshooting pages][wsl-trouble].
This can be a little daunting, come see us if you need in person help.

!!! warning "WSL installation issues"

    When we were trying this ourselves using Windows laptops provided by the University of Zurich we frequently got error messages saying the installation could not continue followed by an error code.
    The missing piece is a need to change a setting in the [BIOS][wsl-bios].
    Changing the 'Intel Virtualization Technology' setting to 'Enabled' fixed it for us.

    If you don't feel comfortable making this kind of BIOS change yourself, we'll help you if you come and see us. 

## Set up your Linux user info

Once the install is complete:

* Open the distribution using the start menu.
* You will be asked to create a username and password. Do so, and press `Enter` after each step. 
    * You might not see anything change as you type the password, that's OK -- it is recording what you write.
* Update and Upgrade your packages. In the shell that is open, use the command:

```bash
sudo apt update && sudo apt upgrade
```

## Set up Windows Terminal

Windows Terminal is our preferred terminal for Windows. 

1. Open the Microsoft Store
2. Search for Windows Terminal
3. Choose the first option - either Windows Terminal or Windows Terminal (Preview)
4. Install it by clicking 'Get'
5. Once installed, you will see it under 'Recently Added' in the Windows menu
6. Open Windows Terminal
7. To get access to your Ubuntu system, click the down arrow in the menu bar
8. Select Ubuntu-xx.xx, and your Ubuntu terminal will open

## The Way Forward

As you proceed through the remainder of the Installation Guide, you will generally follow the steps for 'Linux Users' and enter the commands into the Ubuntu Terminal we just installed.

Occasionally there will be differences between Linux and Windows steps - these will be clearly marked by a separate header 'Windows Users.'

[windows-insiders]: https://insider.windows.com/getting-started
[wsl-trouble]: https://docs.microsoft.com/en-us/windows/wsl/install-win10#troubleshooting-installation
[wsl-bios]: https://appuals.com/wsl-register-distribution-error-0x80370102-on-windows-10/