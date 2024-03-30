Application that remote controls a Nikon D850 during a Solar Eclipse.  The software features the ability to configure different phases in relation to C1 - C4 that can take different sets of photos, including in-camera brackets.  It uses a CH340 USB Relay as a remote shutter trigger.  Instructions on how to create the shutter trigger are in the attached document.

Get the executable from the Release Link:
https://github.com/marcel-isler/SolarEclipseTrigger/releases

These are the steps I'm taking during a run:
1. Format the memory cards in the Camera
2. Clear out the directory where the computer will write the images
3. Connect Camera and USB Relay to Computer (I'm using a USB Hub on the tracker that is connected to the Computer of USB 3.2)
4. Connect the USB Relay to the Remote Shutter Cable on the D850
5. Power on the Camera, verify that you can see the camera from the Computer's File Explorer
6. Start SolarEclipseTimer application
7. Click on the 'Full Log', then 'Session', then 'Full Log' and 'Session' tab once more (there is a bug with the logging showing up I still have to figure out)
8. Click on the 'Event Info' tab and make sure your event times are correct for your location.  Use a phone app like Solar Eclipse Timer to find the correct contact times for your exact location.  Restart the SolarEclipseTrigger application if you had to change values and start from point 7 again.
9. Click on 'Set Camera Date Time' in the upper left corner of the application
10. Click on 'Set Focus' tab
11. Click 'Start Focus Procedure' and frame the sun and set the focus.
12. Click 'End Focus Procedure'
13. If this is the REAL run, that's all that should be necessary and the application will countdown to the different phases.
14. If you're running a simulation, uncheck the 'Use System Time' in the Session tab
15. Enter the date and time you want to simulate and press Start.  To do a full run, start 2 minutes before your C1 time, if you just want to test totality, start 2 minutes before C2.

Make sure you run at LEAST one full run with all the equipment setup exactly how you will do it to make sure batteries hold up, timings are ok etc.  Preferably do a full run with the event date in Event Info changed to the current date and the use the actual even times as if it was April 8th.

Camera Settings:
I have my camera set to not review photos after they are taken.  I also just use the XQD / CFExpress card and set the second card to overflow.  Writing to both cards makes the camera slower and can cause issues with the timing of the sequence.
