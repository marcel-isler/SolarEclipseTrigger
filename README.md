Application that remote controls a Nikon D850 during a Solar Eclipse.  The software features the ability to configure different phases in relation to C1 - C4 that can take different sets of photos, including in-camera brackets.  It uses a CH340 USB Relay as a remote shutter trigger.  Instructions on how to create the shutter trigger are in the attached document.

Pre-Requisite:
Install the latest USB Relay Driver:
https://github.com/marcel-isler/SolarEclipseTrigger/blob/main/USB%20Relay/Driver/CH341SER%20v3.8.zip
Install the latest C++ Redistributable:
https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170

Get the executable from the Release Link:
https://github.com/marcel-isler/SolarEclipseTrigger/releases/tag/v0.9.4

These are the steps I'm taking during a run:
1. Format the memory cards in the Camera
2. Set the Camera to LiveView and move the zoom rectangle near the center (the Nikon SDK doesn't have a method to change the location of that rectangle)
3. Clear out the directory where the computer will write the images
4. Connect Camera and USB Relay to Computer (I'm using a USB Hub on the tracker that is connected to the Computer of USB 3.2)
5. Connect the USB Relay to the Remote Shutter Cable on the D850
6. Power on the Camera, verify that you can see the camera from the Computer's File Explorer
7. Start SolarEclipseTimer application
8. Click on the 'Event Info' tab and make sure your event times are correct for your location.  Use a phone app like Solar Eclipse Timer to find the correct contact times for your exact location.  If you had to make any changes, close SolarEclipseTrigger and go back to Point 7.
9. Click on the 'Full Log', then 'Session', then 'Full Log' and 'Session' tab once more (there is a bug with the logging showing up I still have to figure out)
10. Click on 'Set Camera Date Time' in the upper left corner of the application
11. Click on 'Set Focus' tab
12. Click 'Start Focus Procedure' and frame the sun and set the focus.
13. Click 'End Focus Procedure'
14. If this is the REAL run, that's all that should be necessary and the application will countdown to the different phases.
15. If you're running a simulation, uncheck the 'Use System Time' in the Session tab
16. Enter the date and time you want to simulate and press Start.  To do a full run, start 2 minutes before your C1 time, if you just want to test totality, start 2 minutes before C2.

Make sure you run at LEAST one full run with all the equipment setup exactly how you will do it to make sure batteries hold up, timings are ok etc.  Preferably do a full run with the event date in Event Info changed to the current date and the use the actual even times as if it was April 8th.

Camera Settings:
- Camera set to not review photos after they are taken
- Set Live View Photography to CL1
- Just use the XQD / CFExpress card and set the second card to overflow.  Writing to both cards makes the camera slower and can cause issues with the timing of the sequence.
- Disable WiFi and Bluetooth
- Set Camera to Airplane Mode
- Set Camera to Auto Focus and Lens to A/M (needed for software controlled focus drive to work)
- Set Camera to use Back Button Focusing (don't want to trigger autofocus when we take an exposure)
