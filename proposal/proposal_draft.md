## Project
"Draw a Perfect Circle" Game demo on the DE1-SOC Board.


### Goal
- Hard enough, but not too difficult. 
- Looks coool and attractive.
- Equal workload division.

### Input: 
PS/2 mouse; board button for clear/restart.

### Output: 
VGA drawing area, circularity score, status indicators.

### Logic:

- User holds the left mouse button → draws a circle → releases → FPGA evaluates the drawing.

- Inspired by browser-based [“draw a perfect circle”](https://matrix67.itch.io/pi-day-challenge) games. 

- Main processing happens on the FPGA: input handling, drawing, point storage, geometric calculations, scoring.

It is possible to finish this whole project with Verilog code and the given VGA and PS/2 Adapter modules.


Estimate π from the drawn curve. This part shold be done only after the core system is stable.

### User interaction

- Ready: blank drawing area + visible cursor.

- Press Reset button: begin a new attempt; record the starting point.

- Drag: draw a continuous trace and store sampled coordinates with the mouse.

- Release: finish capture; check validity; calculate score.

- Result: keep the drawing visible; display score or invalid-input status.

- Restart button: clear the canvas and reset all attempt data.

- Initial interface: simple graphics and numeric output. Detailed text, colors, and animations are secondary.


### Workload
- Get input from PS/2 Mouse (Left button and movement)
- Real-time Calculate the mouse cursor movement to get the final score. Do a lot of Math Coding work. Maybe square roots and derivatives. 
    - Goal: Reveal the original (maybe JavaScript? idk) game code with Verilog.
- VGA display output. Display the real-time mouse movement.
- Score output:  Seg7 display.
- Other : 
    - Combine these parts together. 
    - On-board button to Start/Reset. 
- Optional: 
    - Audio: A beep when ready for the user to start drawing, and a beep-beep when the user finishes drawing.
    - Cool UI design


