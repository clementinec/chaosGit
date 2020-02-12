### One-time setup - Preparation
1.Install PySerial
  For mac/linux(ubuntu):
  from PyPI:
  `python -m pip install pyserial`
  from conda:
  `conda install pyserial
  or
  conda install -c conda-forge pyserial`

  For windows:
  _PySerial can be installed on windows but is relatively challenging. Check this [link](https://www.youtube.com/watch?v=Pf-cGzOQmXU) for instructions on how to install it._


2. Find your USB modem connection:
  Recommended approach:
  Through Arduino App interface:
  Connect the arduino (arduino-side pre-loaded) to the computer.
  Tools -> Port -> **/dev/cu.usbmodem**
  
  Alternative approach [here](https://www.mathworks.com/help/supportpkg/arduinoio/ug/find-arduino-port-on-windows-mac-and-linux.html).
3.Download the code and file repo folder.
**Replace the port name**(/dev/cu.usbmodem14301) **in testout.py with this new port**
  Make sure the new port name is in single quotation.
  Save testout.py after the port name has been updated.
  
### Running the code
  1. Open Terminal, move to the downloaded (file and repo) folder.
  
  Example: 
  `cd ~/Downloads/testout`
  Make sure the arduino and the sensors are connected, and 
  2. Run the file with 
  `python testout.py`
  
  The script will automatically capture the beginning time of the experiment, and start print out measured results in the terminal folder. 
  3. Saving the output
  This is done automatically. The printouts are also saved as a txt file in the meantime - and will keep on recording every single second until the python program is paused.
  **The script will not stop reporting/recording if the wires are loose, which could result in 0.00 Volts for the barrel and 1037.55 Melexis sensor.** The example code's output files clearly shows that, but goes back to normal towards the end when the wires are pushed back into place. 
  
### Upcoming tasks
  - Circuit boards, or PCM?
  - Smaller foot print? Alternative sensors?



Optional: Build your own Arduino uploads 
  Libraries including the Adafruit BNO055, Adafruit MLX90614 and Adafruit_Sensor library are necessary for the code to be compiled and loaded onto arduino. 
  This file is currently pre-loaded to arduino.