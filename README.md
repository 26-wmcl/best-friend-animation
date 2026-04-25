# best-friend-animation
A minimalist OLED animation project inspired by Best Friend by Rex Orange County. Built for small microcontrollers, this project turns a simple OLED display into a looping pixel-art animation system.

## 🧰 Hardware Requirements
- ESP8266 or ESP32
- 0.96" SSD1306 OLED Display (I2C)
- Jumper wires
- Breadboard

## 🔌 Wiring (I2C)
### ESP8266 (V3)
| OLED Pin | ESP8266 Pin | Description |
|----------|-----------  |-------------|
| GND      | GND         | Ground |
| VCC      | 3V3         | Power Supply (3.3V) |
| SCL      | D2          | I2C Data |
| SDA      | D1          | I2C Clock |

### ESP32
| OLED Pin | ESP32 Pin | Description |
|----------|-----------|-------------|
| GND      | GND       | Ground |
| VCC      | 3V3       | Power Supply (3.3V) |
| SCL      | GPIO 22   | I2C Clock |
| SDA      | GPIO 21   | I2C Data |

## 💡 How It Works
- Bitmap frames are stored in flash memory (PROGMEM)
- Frames are rendered sequentially using the Adafruit SSD1306 library
- Delays control animation speed and vibe timing
- Motion is simulated using sprite shifts + loop logic

