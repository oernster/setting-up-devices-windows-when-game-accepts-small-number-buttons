# setting-up-devices-windows-when-game-accepts-small-number-buttons
A description of how to configure software on Windows such that multiple hardware devices can run even when you have a limit on buttons due to the game you're playing.

# Install vjoy (must be done _before_ Joystick Gremlin
  https://sourceforge.net/projects/vjoystick/

# Install Joystick Gremlin
  https://github.com/WhiteMagic/JoystickGremlin

  To use this, you'll need to install git and clone the repo.
  Use the command 'git clone <insert repo name here for JG> on the Windows command line.
  
# Install HidHide
  https://github.com/ViGEm/HidHide/releases
  
# Setup
  === Make sure Joystick Gremlin is not running, even in the system tray === 
  1) Go into vjoy and add some devices e.g. 4 of them.  Set each one to have different numbers of buttons; the max in windows currently is 128 buttons, so for example, set each to 128, 127, 126, 125 etc since they must be unique and you want the max number of buttons available.
  For each one, set the POV hat switch to continuous and 4.
  
  2) Now, go into HidHide 'applications' tab and whitelist your hardware configuration software.  e.g. for me this is for Virpil and Joystick Gremlin.
  So, specifically, in the case of Virpil software you need to whitelist the following files:
    c:\program files (x86)\VPC Software Suite\tools\VPC_LED_Control.exe
    c:\program files (x86)\VPC Software Suite\VPC_JOY_SETUP.exe
    c:\program files (x86)\H2k\Joystick Gremlin\joystick_gremlin.exe
  The HidHide client should be auto added.
  Now, in HidHide 'Devices' tab, tick all your hardware (NOT the vjoy devices) and all 3 tick boxes at the bottom.
  Reboot your PC.
  
  3) Launch joystick gremlin.  For each hardware device (not the vjoy ones), remap all axis and all buttons to identical values but a particular vjoy device.  NOTE: you must NOT use more than 32 buttons for Elite Dangerous; your game may have a different limitation.  So, to avoid issues, when remapping, only remap 32 buttons per vjoy device starting at button 1 and then finishing at a max of button 32.  If a hardware device has 100 buttons, then you need to use multiple vjoy devices and only use 32 buttons per vjoy device.  You'll need to map the axes too.
  This is a very tiresome job and involves lots of clicking around in the Joystick Gremlin interface.  Sorry, but there's no simple way to avoid this work unless WhtieMagic, the author of the JG tool, simplifies things in the GUI using some kind of automation.  Once youv'e done it once you'll be sorted.
  Make sure that you map all of your hardware devices this way and do not accidentally duplicate vjoy devices for different pieces of hardware.
  During this process you may find you run out of vjoy devices.  If you do, then you'll need to close JG and install one or more new vjoy devices, then restart JG.
  
  4) Save your joystick gremlin profile.
  Press the gamepad button in the profile to make it go green to enable it.
  Launch your game and define all your keybindings.
  
  5) Enjoy all your hard work; now you can game in peace!
  
  6) Last but not least, I recommend you save your JG profile, save your game bindings and backup both elsewhere. 
  
  
  
