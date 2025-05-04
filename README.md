# 🤖 Gesture Controlled Car using IoT

A hand gesture-controlled robotic car using Arduino, MPU6050, and nRF24L01 for wireless communication.


## 🔧 Features
- Hand gesture recognition using MPU6050
- Wireless control using nRF24L01
- Real-time car movement based on gestures
- Simple, low-cost design using Arduino

## 📦 Components Used

### 🧤 Transmitter Side (Hand Controller)
- Arduino Nano
- nRF24L01 Module
- MPU6050 Gyroscope + Accelerometer
- Push Button (Tx Enable)
- LED Indicator
- 1 × 18650 Li-ion Battery

### 🚗 Receiver Side (Car)
- Arduino Uno
- nRF24L01 Module
- L298N Motor Driver Module
- 2 × BO Motors (Left & Right)
- 2 × 18650 Li-ion Batteries (in series)

---

## ⚙️ Circuit Connections

### 🔹 Transmitter (Tx) Connections

**Arduino Nano:**

| Pin | Connected To        |
|-----|---------------------|
| D9  | nRF24L01 CE         |
| D10 | nRF24L01 CSN        |
| D11 | nRF24L01 MOSI       |
| D12 | nRF24L01 MISO       |
| D13 | nRF24L01 SCK        |
| A4  | MPU6050 SDA         |
| A5  | MPU6050 SCL         |
| D8  | Tx Enable Switch    |
| D7  | LED Indicator       |
| 3.3V| nRF24L01 & MPU6050 VCC |
| GND | All GNDs            |

**Power:**
- 1 × 18650 Battery (3.7V) connected to VCC_1 (through a 3.3V regulator if needed)

---

### 🔹 Receiver (Rx) Connections

**Arduino Uno:**

| Pin | Connected To              |
|-----|---------------------------|
| D9  | nRF24L01 CE               |
| D10 | nRF24L01 CSN              |
| D11 | nRF24L01 MOSI             |
| D12 | nRF24L01 MISO             |
| D13 | nRF24L01 SCK              |
| D3  | L298N IN3 (Motor Left A)  |
| D4  | L298N IN4 (Motor Left B)  |
| D5  | L298N IN1 (Motor Right A) |
| D6  | L298N IN2 (Motor Right B) |
| 3.3V| nRF24L01 VCC              |
| GND | All GNDs                  |

**Motor Driver Output:**
- OUT1 & OUT2 → Left Motor (Red/Black)
- OUT3 & OUT4 → Right Motor (Red/Black)

**Power:**
- 2 × 18650 Batteries (~7.4V) connected to VCC_2 (motor power supply)
- Separate 3.7V supply to Arduino Uno via VCC_1


## Contributions are welcome! Please fork the repository and submit a pull request.