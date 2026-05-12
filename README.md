🚗 Line Following Robot using Arduino
This project implements a Line Following Robot using Arduino and IR sensors. The robot detects a black line on a white surface and moves accordingly by controlling two DC motors with PWM signals.

📌 Features
Uses two IR sensors (Left & Right) for line detection
Controls TT gear motors using PWM
Adjusted PWM frequency for smooth low-speed motor control

Supports:
Forward movement
Left turn
Right turn
Stop condition

🛠️ Components Used
Arduino Uno
2 × IR Sensors
L298N / Motor Driver Module
2 × DC TT Gear Motors
Robot chassis
Power supply (Battery)
Jumper wires

🔌 Pin Configuration
IR Sensors
Sensor	Arduino Pin
Right IR Sensor	11
Left IR Sensor	12

Motor Driver
Motor	Enable Pin	IN1	IN2
Right Motor	6	7	8
Left Motor	5	9	10

⚙️ Working Principle
Both sensors LOW → Robot moves forwar
Right sensor HIGH → Robot turns right
Left sensor HIGH → Robot turns left
Both sensors HIGH → Robot stops

🧠 PWM Frequency Adjustment
TT gear motors don’t rotate properly at low PWM values.
To fix this, the PWM frequency on pins D5 and D6 is increased to 7812.5 Hz using Timer0 configuration:


📄 Code
The project is written in C (Arduino Programming) and includes:
Motor direction control
Speed control using analogWrite()
Sensor-based decision making

▶️ How to Upload & Run
Connect the hardware as per the pin configuration

Open Arduino IDE

Select:
Board: Arduino Uno
Port: Correct COM Port

Upload the code
Place the robot on a black line and power it ON
