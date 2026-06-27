# Smart-Perishable-Product-Tracker

# 🛒 Smart Perishable Product Tracker with RFID & LCD

An Arduino-based smart checkout system that **tracks product cost and weight** using RFID cards, displays totals on an LCD, and gives real-time feedback via LEDs and buzzer.

Ideal as a proof of concept for **smart supermarkets** or **self-checkout kiosks**.

---

## 📦 **Features**
✅ Scan products using RFID tags  
✅ LCD shows product name, price, weight & running total  
✅ Grand total calculation card  
✅ Audio-visual feedback (green/red LEDs, buzzer)  
✅ Supports multiple items, resets after checkout

---

## 🛠 **Hardware Used**
- Arduino UNO (or compatible)
- MFRC522 RFID Reader
- RFID cards/tags (configured with unique UIDs)
- LCD Display 16x2 (I2C interface, address 0x27)
- Green LED
- Red LED
- Buzzer
- Jumper wires

---

## ⚙️ **How It Works**
- Each product has an RFID card/tag with a unique UID.
- When a card is tapped:
  - LCD displays product name, price, and weight.
  - Adds to running total (`T` for total price, `G` for total weight).
  - Green LED blinks & buzzer beeps for valid item.
- If unknown UID:
  - LCD shows “PRODUCT NOT ADDED”
  - Red LED + buzzer alert.
- When “Grand Total” card is scanned:
  - LCD shows final price & weight.
  - Resets totals to zero.

---

## 🧰 **Libraries Used**
- `SPI.h`
- `MFRC522.h`
- `Wire.h`
- `LiquidCrystal_I2C.h`
