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
 - [Steering Management](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/edit/main/README.md#steering-mechanism) 
2. [ Motor Selection](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/blob/main/README.md#2-motor-selection)
3. [Chassis design](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/edit/main/README.md#3-chassis-design-%EF%B8%8F)
4. [Component Mounting](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/edit/main/README.md#4-component-mounting-)
5. [Engineering Principles](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/edit/main/README.md#5-engineering-principles)
6. [Assmebly Instruction](https://github.com/Sikandar-005/WRO-2025-Future-Engineers---TEAM-BAITUSSALAM/edit/main/README.md#6-assembly-instructions)

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

Ackerman steering mechanism<img width="809" height="434" alt="image (1)" src="https://github.com/user-attachments/assets/822befb1-dbc8-469c-be05-a470986c1154" />
 The Ackermann steering The Ackermann steering geometry in the center of the mechanism ensures that both front wheels turn at angles that allow them to follow concentric paths during a turn. This is achieved by angling the steering linkages inward toward the rear axle, so when the central steering arm moves, it causes the inner wheel to turn more sharply than the outer one. As a result, the extended lines from both wheels intersect at the rear axle center, minimizing tire slippage and improving cornering efficiency. This setup is especially useful in vehicles or robotic platforms that require precise and smooth turning.


# 2. Motor Selection
Type: Pololu 25D Metal Gearmotor(25mm Brushed DC Gearmotor with Encoder Option)

![DC Gear motor](https://github.com/user-attachments/assets/3a9aa373-d86a-4775-925d-1fac07e292df)
- Motor Type: Brushed DC motor (available in low-, medium-, and high-power versions)

- Voltage Options: 6V and 12V variants

- Gear Ratios: Wide range from 4.4:1 to 499:1, allowing for speed-torque customization

- Encoder Option: Integrated 48 CPR (counts per revolution) quadrature encoder for precise speed and position feedback

- Body Diameter: 25 mm

- Output Shaft: 4 mm diameter, D-shaped, extends ~12.5 mm


Selection Criteria:
- Torque sufficient for acceleration and climbing inclines
- RPM matched to required top speed for the track
- Low power consumption for extended run time
Implementation: Motors are mounted to custom 3D-printed brackets, connected to 5mm G2 pulleys and a 200 mm closed-loop timing belt driving the rear wheels.

Type:  MG996R Digital High-Torque Servo Motor

[MG996R Servo Motor](IMG-20250808-WA0003https://github.com/user-attachments/assets/43486e56-bbe5-492d-b259-4bfc2bd13bfc)

# 3. Chassis Design 🛠️


- Material: 'PLA' chosen for light weight and structural rigidity
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
- 3D Print chassis and motor mounting brackets (/CAD_Files/)
- Mount Motors to brackets and attach pulleys
- Install Belt Drive and adjust tension
- Mount Electronics and battery
- Connect Wiring according to circuit diagram
- Run Calibration to verify motor direction and steering alignment
















