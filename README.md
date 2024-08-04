# Audio Processor

A simple audio processor written in C and Assembly, designed to run on an FPGA. This project implements audio recording, processing, and playback capabilities using a range of sound effects.

## Features

- **Audio Recording:** Capture audio input via a microphone.
- **Sound Effects:** Apply various effects to the recorded audio, including:
  - Original
  - Reverse
  - Chipmunk (fast & high-pitch)
  - Monster (slow & low-pitch)
  - Echo
  - Chorus
  - Grow
  - Fade
- **Audio Playback:** Output processed audio through a speaker.

## Control and User Interface

The system utilizes a VGA display and LEDs for the user interface, providing visual feedback on the current state. Control is managed through keys and switches on the DE1-SoC board.

### Operating Instructions

1. **Initial State:**  
   After running the project, the system starts in the **IDLE** state. This is indicated by a neutral display screen and LED1 being lit.

   <p align="center">
     <img src="https://github.com/user-attachments/assets/6d23faa3-067c-4c1c-b189-0d95a392c718" alt="image"/>
   </p>

2. **Recording Audio:**  
   - Press **Button 0** to begin recording. The display will show the **RECORDING** state, and LED2 will turn on.
   - To stop recording, press **Button 0** again. The system will revert to the **IDLE** state.
   - The default recording duration is 12.5 seconds or 100,000 samples, adjustable via the `SAMPLE_MAX` parameter in the code.

3. **Applying Sound Effects:**  
   - Use the first three switches (SW0-SW2) to select a sound effect (0-7 corresponding to each effect).
   - The VGA display provides feedback on the selected effect. If an effect is loading, the display shows "LOADING," and all LEDs turn on.

4. **Playing Audio:**  
   - Press **Button 1** to enter the **PLAYING** state, initiating audio playback.
   - After playback, the system returns to **IDLE**.
   - You can switch effects on the recorded audio without needing to re-record.

## Project Setup

To operate the project on the DE1-SoC board, ensure that the board is properly configured and connected. Follow the above instructions for seamless operation.
