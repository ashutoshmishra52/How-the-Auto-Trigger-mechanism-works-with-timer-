# How-the-Auto-Trigger-mechanism-works-with-timer-
The ESP32 uses a non-blocking timer (`millis()`) to control the auto trigger. After a fixed time interval, Servo-1 aligns to a set angle and Servo-2 performs the trigger action. The OLED displays timer status and trigger state. After activation, servos reset and the timer restarts automatically.
