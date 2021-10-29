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

### v.1.9.1 (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.9.1/Eko.Windows.App.Installer.v1.9.1.msi">Link</a>) (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.9.1/Eko.Windows.App.Installer.v1.9.1.msi.zip">Zip file</a>)]

2021-10-27
New features and bugfixes
* Fixed pairing issue with Eko CORE

### v.1.9.0 (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.9.0/Eko.Windows.App.Installer.v1.9.0.msi">Link</a>) (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.9.0/Eko.Windows.App.Installer.v1.9.0.msi.zip">Zip file</a>)]

2021-06-23
New features and bugfixes
* Hardware Acceleration turned off by default for computers with Intel Xe GPU
  - A bug affecting Intel Xe GPU drivers currently prevents the application from plotting data when using hardware acceleration
* Added support for Eko DUO v4.0+
* Fixed bug affecting the login form validator when password is copied and pasted
* Fixed bug affecting the migration of user settings when the application is updated

### v.1.8.1 (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.8.1/Eko.Windows.App.Installer.v1.8.1.msi">Link</a>) (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.8.1/Eko.Windows.App.Installer.v1.8.1.msi.zip">Zip file</a>)]

2021-03-30
New features and bugfixes
* Fixed issue with auto update from 1.7.0

### v.1.8.0 (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.8.0/Eko.Windows.App.Installer.v1.8.0.msi">Link</a>) (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.8.0/Eko.Windows.App.Installer.v1.8.0.msi.zip">Zip file</a>)]

2021-03-29
New features and bugfixes
* Fixed pairing issue with Eko DUO

### v.1.7.0 (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.7.0/Eko.Windows.App.Installer.v1.7.0.msi">Link</a>) (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.7.0/Eko.Windows.App.Installer.v1.7.0.msi.zip">Zip file</a>)]

2021-03-03
New features and bugfixes
* Added support for Data Length Extension
* Improved the accuracy of the BLE device enumerator
* Fixed handling of the connection to CORE 1 using BLED dongle

### v.1.6.1 (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.6.1/Eko.Windows.App.Installer.v1.6.1.msi">Link</a>) (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.6.0/Eko.Windows.App.Installer.v1.6.1.msi.zip">Zip file</a>)]

2021-01-05
New features
* Added support for screen with 150% dpi
* Added support for DUO 4.0+

### v.1.6.0 (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.6.0/Eko.Windows.App.Installer.v1.6.0.msi">Link</a>) (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.6.0/Eko.Windows.App.Installer.v1.6.0.msi.zip">Zip file</a>)]

2020-08-18
New features and bugfixes
* Added visual c++ to the installer
* Changed App window position to top center of monitor on startup
* Changed livestream audio packet serialization
* Changed auto update workflow
  - The app will not start the auto update thread if the user is not a local admin and the app is installed for all users.
  - The app will start the auto update thread if the user is not local admin and the app is installed only for the current user.
  - The app will start the auto update thread if the user is local admin and app is installed for all users
  - Silently update the app once the latest installer is downloaded.


### v.1.5.3 (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.5.3/Eko.Windows.App.Installer.v1.5.3.msi">Link</a>) (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.5.3/Eko.Windows.App.Installer.v1.5.3.msi.zip">Zip file</a>)

2020-05-29
New features and bugfixes
* Fixed per user upgrade installer


### v.1.5.2 (<a href="https://ekodevices.github.io/windows-app-releases/Eko%20Windows%20App%20Installer%20v1.5.2.msi">Link</a>) (<a href="https://ekodevices.github.io/windows-app-releases/Eko%20Windows%20App%20Installer%20v1.5.2.msi.zip">Zip file</a>)
2020-05-05
New features and bugfixes
* Added support for pairing with DUO 3.7+

### v.1.5.1 (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.5.1/Eko.Windows.App.Installer.v1.5.1.msi">Link</a>) (<a href="https://github.com/EkoDevices/windows-app-releases/releases/download/v1.5.1/Eko.Windows.App.Installer.v1.5.1.msi.zip">Zip file</a>)
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
