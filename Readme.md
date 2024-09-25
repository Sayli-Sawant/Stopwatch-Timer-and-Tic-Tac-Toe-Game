# Stopwatch Timer and Tic-Tac-Toe Game

## Goal
This project demonstrates the development of two distinct applications on the Tiva C Series Launchpad:
1. **Stopwatch Timer**: A stopwatch capable of displaying time (seconds and milliseconds) on a seven-segment display, controlled via onboard switches (SW1 and SW2) or UART commands.
2. **Tic-Tac-Toe Game**: A Tic-Tac-Toe game playable using a 4x4 keypad, with game updates displayed on the UART console.

### Stopwatch Timer Features:
- **Display**: Four seven-segment displays (three for seconds, one for milliseconds).
- **Control**: Controlled by:
  - **SW1**: Start/Stop
  - **SW2**: Pause/Resume
  - UART commands: `timer start`, `timer stop`, `timer pause`, `timer resume`
- **Indications**: 
  - Ready state: Continuous Green LED, LCD displays "Timer Ready."
  - Running state: Blinking Green LED, LCD displays "Timer Running."
  - Paused state: Blinking Blue LED, LCD displays "Timer Paused."

### Tic-Tac-Toe Game Features:
- **Input**: Played using a 4x4 keypad (first 3 rows/columns).
- **Players**: Alternates between two players ('X' and 'O').
- **Output**: Game updates, move validation, and result (win/draw) printed on the UART console.

## Requirements
- **Hardware**:
  - Tiva C Series Launchpad (TM4C123GH6PM)
  - EDUARM Board with the following interfaces
    - Seven-segment LED display
    - 4x4 Keypad
    - LCD display
    - Green and Blue LEDs
    - SW1 and SW2 switches
  - UART interface for communication
- **Software**:
  - TivaWare library
  - Code Composer Studio (CCS) or other compatible IDE

## Working

### Stopwatch Timer:
1. **Control via Switches**:  
   - Press **SW1** to start/stop the timer.
   - Press **SW2** to pause/resume the timer.
   - Time is displayed on the seven-segment LED and state information is shown on the LCD and indicated by LEDs.
   
2. **Control via UART**:  
   - Use commands: `timer start`, `timer stop`, `timer pause`, and `timer resume` to control the timer through UART.

3. **LED Indicators**:  
   - **Green LED**: Continuous when the timer is ready, blinking when running.
   - **Blue LED**: Blinking when the timer is paused.

### Tic-Tac-Toe Game:
1. **Player Moves**:  
   - Players make their moves using the 4x4 keypad. Each valid move is updated in the game matrix.
   
2. **Game Status**:  
   - After each move, the status is updated on the UART console, including win/draw or invalid moves.

3. **Winning Condition**:  
   - The program checks for a winning line or a draw condition after each move.
   
