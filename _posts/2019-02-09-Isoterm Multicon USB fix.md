# Isoterm Multicon USB interface not transmitting or appearing in software

*Written 09/02/2019 by Harley Glover-Newson - [harleygn.net](https://harleygn.net)*

This guide explains how solve the issue of your USB interface not transmitting or appearing as a COM port in desktop software. The root cause of this issue appears to be incompatible drivers, perhaps due to operating system upgrades. Follow the steps below to install and setup alternative drivers.

**Note: This has guide assumes you are running Windows 10 and using an Isoterm Multicon USB interface. While it may work with other versions of Windows and other USB devices, it has not been tested.**

**Disclaimer: While it is a fairly safe process, I (Harley Glover-Newson), do not take responsibility for any adverse effects that may occur as a result of follow this guide.**

### Step 1: Check connections

Firstly, ensure that the device is connected to your PC correctly via USB, and that it powers up in some way, with illuminated LEDs on the front. You may need to try other USB ports if this does not work first time.

### Step 2: Open Device Manager

If the device is properly connected and powered up, it should appear in the Windows device manager. To check this, open Device Manager by either searching 'Device manager' in the Start menu, or right clicking on the Start menu button and selecting 'Device Manager'. The following window should appear:

![device](/Users/harleygn/Downloads/guide/device.png)

Open the sub-list named 'Ports (COM & LPT)' by clicking on the arrow to the left of it. If the device is connected, it will appear as 'Prolific USB-to-Serial Comm Port', as shown above, although the specified COM number may be different.

There should also be a small yellow triangle next to this device, indicating there is an error with it, hence the issue you are facing: the next steps should remedy this.

### Step 3: Install new drivers

Included with this guide is a ZIP file named `PL2303_HXA_Driver_V10518.zip`. This contains the installer for version 3.3.5.122 of the Prolific USB-to-Serial drivers, from 17/07/2009. Extract this and run the `PL2303_Prolific_DriverInstaller_v10518.exe` located inside. Follow the steps to install the drivers.

### Step 4: Choose the new drivers

Right click on the device name and select 'Update drivers'. The window below should appear, asking how you would like to find the new drivers. Choose 'Browse my computer for driver software'.

![update](/Users/harleygn/Downloads/guide/update.png)

You will be given the option to browse for driver software on your computer, however this is not necessary as we have already installed the alternative drivers. Instead, choose 'Let me pick from a list of available drivers on my computer'.

![browse](/Users/harleygn/Downloads/guide/browse.png)

If the drivers in the previous step have been installed correctly, they will now appear in the list of available drivers.

![choose](/Users/harleygn/Downloads/guide/choose.png)

It is likely that you will see multiple drivers available for you to choose from. Select the driver named `Prolific USB-to-Serial Comm Port Version: 3.3.5.122 [7/17/2009]` which we installed in Step 3, and click Next. Windows will configure the device with this driver, and give you a success message.

### Step 5: Check Device Manager again

Go back to Device Manager and find the device again. The yellow triangle should now have disappeared. If it hasn't, repeat steps 3 and 4. If the yellow triangle persists, the issue is caused by something else.

### Step 6: Setup device in desktop software

Navigate to your desktop Amateur Radio software (e.g. Airlink Express, DigiPan etc.) and find the option to setup your PTT Serial Port. The image below shows this in Airlink Express. When choosing a port, you should now have the option to select the COM port of your USB interface. If you do not know which COM port your USB interface is connected to, go back to the Device Manager. The COM port is written in brackets at the end of the device name, COM3 in this case.

![airlink](/Users/harleygn/Downloads/guide/airlink.png)

### Step 7: Test

If the setup has been completed correctly, the Transmit/TX light should illuminate on the USB device when you choose to transmit in the desktop software.