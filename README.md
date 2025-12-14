## ⏱️ Auto Trigger Mechanism (Timer-Based)

This project implements an automatic trigger mechanism using an ESP32, two servo motors, and an OLED display.  
The system works on a timer-based logic and operates fully automatically without manual input.

---

## 🔧 Components Used

- ESP32 (Main Controller)
- 2 Servo Motors  
  - Servo 1: Horizontal movement  
  - Servo 2: Trigger / firing action  
- OLED Display (System status & timer)
- Non-blocking Timer (`millis()` based)

---

## ⚙️ Working Principle

### System Initialization
- On power ON, the ESP32:
  - Moves both servos to their default positions
  - Displays **System Ready** and timer status on the OLED
- No button or manual trigger is required

---

### Timer-Based Auto Trigger Logic
- The system uses the `millis()` function instead of `delay()`
- This ensures:
  - Smooth servo motion
  - Accurate timing
  - Non-blocking execution

**Trigger Condition:**


When this condition is met, the auto trigger activates.

---

### Servo Motor Action
- Servo 1 rotates to a predefined alignment angle
- Servo 2 performs the trigger action:
  - Moves forward (Trigger ON)
  - Holds briefly
  - Returns to default position (Trigger OFF)

This simulates a mechanical trigger mechanism.

---

### OLED Display Feedback
The OLED shows:
- Remaining time before the next trigger
- Trigger states:
  - READY
  - TRIGGERED
  - RESETTING
- Optional trigger cycle count

---

### Automatic Reset & Loop
- After triggering:
  - Servos reset to default position
  - Timer restarts automatically
- The process repeats continuously

---

## 🔁 Auto Trigger Flow

Start → Timer Running → Time Completed → Servo Trigger
→ Reset Position → Timer Restart → Repeat

---

## ✅ Key Features
- Fully automatic operation
- Timer-based logic using `millis()`
- Smooth and reliable servo control
- Real-time OLED feedback
- Easy to modify trigger interval

---

## 🧠 Applications
- Educational auto-trigger demos
- Robotics automation
- Servo-based mechanical systems
- IoT timed action projects

