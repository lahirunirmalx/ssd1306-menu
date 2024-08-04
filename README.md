# OLED Menu Navigation System

This Arduino project demonstrates an OLED menu navigation system using an Adafruit SSD1306 display and the OneButton library. The system allows you to navigate through a series of menu items using three buttons: OK, UP, and DOWN.

## Hardware Requirements

- Arduino board (e.g., Arduino Uno)
- Adafruit SSD1306 OLED display
- Three push buttons
- Connecting wires
- Breadboard (optional)

## Libraries Used

- [Adafruit GFX Library](https://github.com/adafruit/Adafruit-GFX-Library)
- [Adafruit SSD1306 Library](https://github.com/adafruit/Adafruit_SSD1306)
- [OneButton Library](https://github.com/mathertel/OneButton)

## Pin Configuration

- `PIN_INPUT_OK` connected to digital pin 16
- `PIN_INPUT_UP` connected to digital pin 18
- `PIN_INPUT_DOWN` connected to digital pin 19

## Display Configuration

- Screen width: 128 pixels
- Screen height: 64 pixels

## Menu Items

The menu consists of 11 items:

1. New File
2. Open File
3. Save
4. Save As
5. Undo
6. Redo
7. Sensor
8. Key Lock
9. Settings
10. Network
11. Close

## Features

- Navigate up and down through the menu items
- Select a menu item with the OK button
- Display a closing animation when the "Close" menu item is selected

## Code Explanation

### Global Variables

- `currant_screen`: Keeps track of the current screen (initially 0).
- `selected_item`: Keeps track of the selected menu item (initially 0).

### Image Data

- `refreshImage`: A bitmap image stored in program memory (PROGMEM) for displaying an icon on the screen.

### Menu Items

- `main_menu_items`: A 2D array holding the menu item names.

### Display and Button Initialization

- `Adafruit_SSD1306 display`: Initializes the OLED display.
- `OneButton button_ok`, `button_up`, `button_down`: Initializes the buttons with their respective pins.

### Button Functions

- `goUp()`: Moves the selection up.
- `goDown()`: Moves the selection down.
- `goTop()`: Moves the selection to the top item.
- `goBottom()`: Moves the selection to the bottom item.
- `clickOk()`: Executes the action for the selected item.

### Menu Display Functions

- `printMenu()`: Displays the menu with the currently selected item.
- `printActionMenu()`: Displays the menu items on the screen.
- `printMenuTitle()`: Displays the menu title.
- `trim_string()`: Trims a string to a specified length.

### Main Functions

- `setup()`: Initializes the serial communication, display, and button functions. Displays the initial menu.
- `loop()`: Continuously updates the menu display and checks for button presses.

## Setup and Usage

1. Connect the OLED display to the Arduino using the I2C interface.
2. Connect the push buttons to the Arduino according to the pin configuration.
3. Install the required libraries in the Arduino IDE.
4. Upload the code to the Arduino board.
5. Use the buttons to navigate through the menu and select items.

## License

This project is licensed under the LGPL-2.1 license. See the `LICENSE` file for details.
 

## Acknowledgments

- Adafruit for the display and libraries.
- Mathertel for the OneButton library.
