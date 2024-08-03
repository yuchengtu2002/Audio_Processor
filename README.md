# Audio_Processor
A simple audio processor coded in C and Assembly, and runs on FPGA.

**Functions:** Record audio input using a microphone, add sound effects to the recorded audio, and output it through a speaker. Sound effects include original, reverse, chipmunk (fast & high-pitch), monster (slow & low-pitch), echo, chorus, grow, and fade.

**Control and UI:** The system uses VGA and LEDs to display the interface and show the current state. KEYs and SWITCHes are used for control.

**To operate the project on the DE1-SoC board:**

After running the project in the monitor program, begin by observing the current state on the display, which will be IDLE by default. This is indicated by a neutral screen display (no specific words indicating other states) and LED1 being turned on.

<p align="center">
  <img src="https://github.com/user-attachments/assets/6d23faa3-067c-4c1c-b189-0d95a392c718" alt="image"/>
</p>


To start recording audio, press Button 0. The state will change to RECORDING, which is indicated by a corresponding message on the display and an LED pattern (LED2 turned on). Audio input is captured in real-time and stored in a buffer until Button 0 is pressed again, signaling the end of recording and reverting the system to IDLE. 

By default (in the submitted code), the user can record up to 12.5 seconds or 100,000 samples. This can be adjusted by changing the SAMPLE_MAX parameter defined at the beginning of the code.

Audio effects can be applied by adjusting the first three switches on the board (SW). The value of these switches (0-7) corresponds to the eight different sound effects. There is visual feedback on the VGA when a sound effect is selected. The program may take some time to load the effect, as indicated by the display showing "LOADING" or all LEDs being turned on.

To play the recorded audio, press Button 1 to switch to the PLAYING state. Audio playback will commence, and once completed, the system will return to IDLE. The user can switch different effects on the same recorded audio without the need to re-record when changing sound effects.
