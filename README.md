## Eko Windows App Releases

Releases are available here: ekodevices.github.io/windows-app-releases/{filename}

## Installing

The build will produce a standard windows installer MSI which can be used to install a per user or per machine copy of the application. A per machine will give all users of the target computer a desktop and start menu shortcut.

**NOTE:**
To install the application per machine will require the installing user account to have administrative rights on the target computer.

### Silent Installation

The application can be installed to a target computer silently without a user interface.

#### Silent Installation Per Machine

_msiexec /i EkoWindowsSetup.msi /quiet /qn MSIINSTALLPERUSER=""_

To disable automatic updates of the application pass the parameter ENABLEAUTOUPDATE=0 on the command line. By default automatic application update is enabled.

_msiexec /i EkoWindowsSetup.msi /quiet /qn MSIINSTALLPERUSER="" ENABLEAUTOUPDATE=0_

#### Silent Installation Per User

_msiexec /i EkoWindowsSetup.msi /quiet /qn_

To disable automatic updates of the application pass the parameter ENABLEAUTOUPDATE=0 on the command line. By default automatic application update is enabled.

_msiexec /i EkoWindowsSetup.msi /quiet /qn ENABLEAUTOUPDATE=0_

**NOTE:**
To silently install the application will require the installing user account to have administrative rights on the target computer. This is regardless of whether the install is per user or per machine. The reason is that there is no UI therefore UAC cannot be rendered during the install.

## Automatic Updates

When the app launches it will check to see if a new version is available.
If there is a new version, the app will ask the user if they would like to update.
If they select YES then a new app will be silently installed and the software will close and relaunch.
If they select NO then the prompt will be dismissed (but will reappear whenever the app is launched in the future).


## Software release notes

### v.1.5.3

2020-05-05
New features and bugfixes
* Fixed per user upgrade installer


### v.1.5.2 (<a href="https://ekodevices.github.io/windows-app-releases/Eko%20Windows%20App%20Installer%20v1.5.2.msi">Link</a>) (<a href="https://ekodevices.github.io/windows-app-releases/Eko%20Windows%20App%20Installer%20v1.5.2.msi.zip">Zip file</a>)
2020-05-05
New features and bugfixes
* Added support for pairing with DUO 3.7+

### v.1.5.1 (<a href="https://ekodevices.github.io/windows-app-releases/Eko%20Windows%20App%20Installer%20v1.5.1.msi">Link</a>) (<a href="https://ekodevices.github.io/windows-app-releases/Eko%20Windows%20App%20Installer%20v1.5.1.msi.zip">Zip file</a>)
2020-03-03
New features and bugfixes
* Fix infrequent connection timeouts occurring when the app tries to connect to the Eko CORE 2

### v1.5.0 (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.5.0/Eko.Windows.App.Installer.v1.5.0.msi">Link</a>)
2020-02-06
New features and bugfixes
* Added Eko CORE 2 support
* Added an enumeration view for Littmann 3200

### v1.4.9 (<a href="https://github.com/EkoDevices/INTERNAL-Eko-Windows-App/releases/download/v1.4.9.3/EkoWindowsSetup.msi">Link</a>)
2019-11-05
New features and bugfixes
* Added Eko DUO support
* Added Littmann 3200 support
* Added in app sharing of Livestream url via email
* Removed recording button on the waveform screen

