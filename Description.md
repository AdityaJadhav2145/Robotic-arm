# Robotic-arm
"5-DOF Robotic Arm | Arduino UNO + MG995 Servos | SolidWorks CAD &amp; FEA | 3D Printed (PUR)"

 Key Features
 5-DOF Articulated Design - Maximum workspace flexibility for pick-and-place, welding, and assembly tasks

 Cost-Effective - Built with affordable components and 3D printing technology

 3D Printed Structure - PUR links with acrylic components for lightweight yet rigid construction

 CAD Validated - Full SolidWorks assembly with mass properties verification

 FEA Verified - Structural analysis confirming safety factors well within limits

 Arduino Controlled - Easy to program and extend with Arduino ecosystem

 Precision Motion - Servo-driven joints with PWM control

## 👥 Core Team

- **Aditya Jadhav** – *Electronics Design & Integration, System Assembly, Hardware Validation*  
  Responsible for circuit design, component selection (Arduino UNO, PCA9685, MG995 servos), soldering/wiring, and physical assembly of the entire robotic structure. Ensured seamless integration between the electronics stack and mechanical links.

Metric	Result
Payload Capacity	~48 g at full horizontal reach
Governing Constraint	J1 Shoulder & J2 Elbow torque limits
FEA Safety Factor	Min FOS = 260
Maximum Stress	0.176 MPa (Well below yield)
Deformation	Sub-micron range

Degrees of Freedom
Joint 1 - Base Yaw (Servo 1)
Joint 2 - Shoulder Pitch (Servo 2)
Joint 3 - Elbow Pitch (Servo 3)
Joint 4 - Wrist Pitch (Servo 4)
Joint 5 - Wrist Roll (Servo 5)
Joint 6 - Gripper (Servo 6)

Circuit Diagram-

                   ┌─────────────────────────────────────┐
                   │           ARDUINO UNO               │
                   │          ATmega328P                 │
                   │                                     │
     ┌─────────────┤  D3    D5    D6    D9    D10   D11 │
     │             │                                     │
     │             │  SDA (A4)                           │
     │             │  SCL (A5)                           │
     │             │                                     │
     │             │  5V / GND                           │
     │             └──────────────┬──────────────────────┘
     │                            │
     │   ┌────────────────────┐   │
     │   │   PCA9685          │   │
     │   │   16-ch I2C        │   │
     │   │   Servo Driver     │◄──┘
     │   └────────┬───────────┘
     │            │
     │   ┌────────┴────────────┐
     │   │  6V / 5A DC Power   │
     │   │  Supply             │
     │   └────────┬────────────┘
     │            │
     │   ┌────────┴──────────────────────────┐
     │   │  6 × MG995 Servo Motors           │
     │   │  (Base, Shoulder, Elbow,          │
     │   │   Wrist Pitch, Wrist Roll, Gripper)│
     │   └───────────────────────────────────┘
     │
     └── USB / Serial (PC / Arduino IDE)




     🌟 Applications
     
🏭 Industrial Automation
Pick-and-place operations
Repetitive material handling
Conveyor sorting systems

🔬 Research & Education
Teaching kinematics and robotics
Robotics programming courses
FEA validation demonstrations

🏥 Medical Assistance
Rehabilitative therapy support
Surgical assistance (concept)
Pharmaceutical handling

🌐 Remote Operations
Hazardous environment tele-operation
Nuclear facility handling
Deep-sea exploration support

🤖 Collaborative Robotics
Human-robot collaboration studies
Light assembly tasks
Service counter operations

🔧 Rapid Prototyping
Gripper design testing
Sensor integration platform
Control algorithm development
