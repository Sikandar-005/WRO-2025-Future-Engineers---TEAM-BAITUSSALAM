# TEAM BAITUSSALAM
# Jamia Baitussalam

<img width="197" height="256" alt="download" src="https://github.com/user-attachments/assets/0e03e373-d699-4b1d-b68f-fd0811d3ac7c" />

This repository presents our self-made robotic system, designed acoording to the WRO 2025 (Future Engineers) theme challenge. We use a combination of different mechanics, smart sensors, different algorithms, and autonomous decision-making to solve a real-world problem through a functional, scalable prototype.

# Content Table

# [TEAM INTRODUCTION](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/edit/main/README.md#team-introduction)
1. [WHO ARE WE?](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM?tab=readme-ov-file#who-are-we)
2. [WHERE DO WE COME FROM?](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/blob/main/README.md#-where-do-we-come-fromthe-participants)
3. [Our Journey](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM?tab=readme-ov-file#-our-journey-)

# [Mobility Management](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM#mobility-management-)
1. [Vehicle Movement Management](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/blob/main/README.md#1-vehicle-movement-management)
 - [Steering Mechanism](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/edit/main/README.md#steering-mechanism) 
2. [ Motor Selection](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/blob/main/README.md#2-motor-selection)
3. [Chassis design](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/edit/main/README.md#3-chassis-design-%EF%B8%8F)
4. [Component Mounting](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/edit/main/README.md#4-component-mounting-)
5. [Engineering Principles](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/edit/main/README.md#5-engineering-principles)
6. [Assmebly Instruction](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/edit/main/README.md#6-assembly-instructions)

# [Power and Sense Management ]()

# TEAM INTRODUCTION

# Who are we?

We are a passionate and creative team of young innovators representing our school/country in the WRO 2025 Future Engineers category. Driven by curiosity and a shared vision for a better future, we bring together skills in robotics, programming, engineering design, and teamwork to solve real-world challenges.

Our team thrives on collaboration, critical thinking, and hands-on problem-solving. Each of us contributes unique strengths—whether it's coding intelligent algorithms, designing 3D printable components, optimizing hardware integration, or fine-tuning sensors. Together, we are building more than just a robot—we are building solutions that matter.

With a strong belief in learning by doing, we’ve embraced cutting-edge technologies such as ROS2, IMUs, line sensors, and custom-designed 3D parts to meet the demands of the competition.

We are not just participants—we are future engineers preparing to shape the world.
# 🌍 Where do we come from(The participants)?

We are a team of aspiring engineers from different cities across Pakistan, brought together by a common passion for robotics and innovation. What unites us is Jamia Baitussalam — an institute where modern science and classical education go hand in hand.

At Jamia Baitussalam, we’re not just students — we’re innovators. The institution fosters a unique blend of Islamic education, modern sciences, and cutting-edge technology. With access to state-of-the-art robotics labs, 3D printing, programming, and AI resources, we are encouraged to explore, invent, and lead.

Our journey in WRO 2025 is a reflection of what Baitussalam stands for: bridging the gap between tradition and technology, and empowering youth to become ethical, forward-thinking engineers of tomorrow.

# 🚀 Our Journey 🌟

We are three teammates — Taha Umer, Zulqarnain, and Sikandar — bound together by friendship, teamwork, and a shared passion for technology. We study at Jamia Baitussalam Talagang, an Islamic institute that nurtures both academic excellence and strong moral values.

Our journey began with a simple idea: to step into the world of robotics and engineering through the WRO 2025 Future Engineers challenge. With limited resources but unlimited determination, we started from simple programmes — learning new tools, exploring new technologies, and understanding the real-world applications of robotics.

Along the way, we faced challenges that tested our patience and problem-solving skills — from mechanical design issues to fine-tuning code for better performance. Each challenge became a stepping stone, making our team stronger and our project better.

This repository is the record of our progress — the designs, the code, the experiments, and the lessons learned. For us, this is more than a competition; it’s a journey of growth, learning, and teamwork. And we’re just getting started.

# Mobility Management 🛞
# 1. Vehicle Movement Management
The robot’s movements are controlled through a rear-wheel drive system powered by Pololu 25D Metal Gearmotor(25mm Brushed DC Gearmotor with Encoder Option) and a front steering mechanism servo-based Ackermann.
Motor speed and steering angle are managed using PWM signals from the Raspberry Pi, with feedback from the QTR sensor array and IMU for precise control.
# Steering Mechanism

# Ackerman steering mechanism<img width="809" height="434" alt="image (1)" src="https://github.com/user-attachments/assets/822befb1-dbc8-469c-be05-a470986c1154" />
The Ackermann steering geometry in the center of the mechanism ensures that both front wheels turn at angles that allow them to follow concentric paths during a turn. This is achieved by angling the steering linkages inward toward the rear axle, so when the central steering arm moves, it causes the inner wheel to turn more sharply than the outer one. As a result, the extended lines from both wheels intersect at the rear axle center, minimizing tire slippage and improving cornering efficiency. This setup is especially useful in vehicles or robotic platforms that require precise and smooth turning.


# 2. Motor Selection
| Motor | Specifications |
|-------|----------------|
| ![DC Gear motor](https://github.com/user-attachments/assets/288496ce-5f6e-454b-8fb5-fd1dce2e9569) | • Type: Pololu 25D Metal Gearmotor(25mm Brushed DC Gearmotor with Encoder Option) • Voltage: 12 V <br> • No-load Speed: ~300 RPM• Stall Torque: ~11 kg·cm <br> • Stall Current: ~5 A <br>• Encoder: 48-CPR quadrature, ~1632 counts/rev after gearbox|
These motors provide the necessary torque for overcoming ramps and obstacles, while the encoders enable accurate distance measurement and closed-loop speed control. 


  





Selection Criteria:
- Torque sufficient for acceleration and climbing inclines
- RPM matched to required top speed for the track
- Low power consumption for extended run time
Implementation: Motors are mounted to custom 3D-printed brackets, connected to 5mm G2 pulleys and a 200 mm closed-loop timing belt driving the rear wheels.


Type:  MG996R Digital High-Torque Servo Motor
![MG996R Servo Motor](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/blob/main/Models/3D%20designs/Components/MG996R%20Servo%20Motor.jpg)
- Strong enough to lift and steer — with up to 11 kg·cm torque, it can handle steering mechanisms or manipulator arms in a competition robot.
- Durable metal gears mean fewer breakdowns during long testing sessions or unexpected impacts in the WRO field.
- Fast and responsive movement (about 0.17s per 60° at 6V) helps in precision steering and quick obstacle maneuvers.
- Standard PWM control makes it easy to integrate with Arduino, Raspberry Pi, or even ROS-based systems in your WRO build.
- Affordable and widely available, so replacing one during competition prep is quick and budget-friendly.
- Compact design allows mounting in tight spaces inside a robot chassis without sacrificing strength.
- Reliable under voltage fluctuations — useful when your WRO robot runs on batteries that may drop slightly under load.
- Proven in robotics competitions — it’s a common choice among WRO and other robotics teams, so resources and examples are easy to find.
# 3. Chassis Design 🛠️


- Material:  'PETG' is a tough, impact-resistant filament known for its durability, flexibility, and resistance to moisture and chemicals.
- Layout: Low center of gravity for stability, optimized wheelbase for maneuverability
- Mounting Points: Designed for easy integration of motors, electronics, and sensors without modifying the structure
  
# 4. Component Mounting 🧲
- Motors: Secured with vibration-resistant fasteners to prevent alignment shift
- Electronics: Raspberry Pi and motor driver mounted on a vibration-damped plate
- Battery: Center-mounted for balanced weight distribution
- Sensors: QTR array at the front, IMU at the center for accurate readings

# 5. Engineering Principles
Torque:
- 𝑇 = 𝐹 × 𝑟 – Calculated to ensure enough drive force under load
Speed:
- v = (Wheel Circumference × RPM) / 60 – Ensures speed matches track requirements
Power:
- 𝑃 = 𝑇 × 𝜔 P = T × ω – Verified to match motor and battery capabilities
Gear Ratio: Pulley ratio selected to balance torque and top speed

# 6. Assembly Instructions
- 3D Print chassis and motor mounting brackets ([Models/3D designs](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/tree/main/Models/3D%20designs))
- Mount Motors to brackets and attach pulleys
- Install Belt Drive and adjust tension
- Mount Electronics and battery
- Connect Wiring according to circuit diagram
- Run Calibration to verify motor direction and steering alignment

# Power and Sense Management 
This section explains the robot’s power system and sensor suite, explaining component selection, integration, and layout, supported by a wiring diagram and complete bill of materials.
# 1. Power Source

# 2. Sensors
| Sensor Name | Purpose | Reason for selection | Placement on Robot | 
|----------|----------|----------|----------|
| Camera Module Raspberry pi | the Raspberry Pi Camera Module acts as the robot’s “eyes,” enabling it to detect lanes, obstacles, and signs, as well as recognize objects using AI models. It supports autonomous navigation and decision-making by providing real-time visual data and can also record runs for later analysis. Overall, it makes the robot smarter, more adaptive, and better prepared for handling complex competition courses | Row 1 C3 |
| Row 2 C1 | Row 2 C2 | Row 2 C3 |


















