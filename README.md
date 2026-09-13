# pwa-radar
PWA-based radar simulator using publicly-accessible data

Iniail idea: Creating a PWA-compatible webapp, which allows users to use their current (or moving) GPS or custom location, to display a realistic radar trace of air traffic in the skies around them. The app will be able to accurately simulate cathode ray tube (CRT) radar screens with beam sweeps, as well as display more modern appearances with aircraft labelled with speed and heading barbs. 

It will have a settings page containing details such as theme and location, and have twistable dials to provide range, sweep speed, and maximum altitude filtering, as well as a toggle switch between old CRT and modern radar displays.

The "old style" CRT rendered screen shall update aircraft locations only when the sweep passes. The modern display will interpolate aircraft position information for displayed aircraft in real-time. Aircraft position data shall be polled in 30 second intervals. 

The PWA wrapper shall have a full icon set to ensure full PWA-installability. The app will run as a simple webpage, in this instance from the URL jahosi.co.uk/radar 