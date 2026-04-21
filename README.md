//# LCD_Screen
//This is a code on how to use an LCD screen

#include <Wire.h>
#include <LiquidCrystal_I2C.h>

// Set the LCD address to 0x27 for a 16 chars and 2 line display
// If 0x27 doesn't work, try 0x3F
LiquidCrystal_I2C lcd(0x27, 16, 2);

void setup() {
  // Initialize the LCD connected to GPIO 21 (SDA) and 22 (SCL)
  lcd.init();

  // Turn on the backlight
  lcd.backlight();

  // Print a message to the LCD
  lcd.setCursor(0, 0);         // Move cursor to character 0, line 0
  lcd.print("Hello, this is!");

  lcd.setCursor(0, 1);         // Move cursor to character 0, line 1
  lcd.print("Easy and Simple");
}

void loop() {
  // You don't need to do anything in the loop for a static message
}
