# Venturi_X_Omnidirectional_Wind_Turbine

## Project Overview

This project focuses on the design, simulation, and validation of a highly optimized Diffuser Augmented Wind Turbine (DAWT) intended for operation in low-wind-speed environments. The system incorporates Venturi-based flow acceleration and diffuser augmentation to increase wind velocity through the turbine, thereby reducing the minimum wind speed required for power generation and improving overall energy extraction efficiency.

The turbine utilizes a 1.5-foot (457.2 mm) rotor, selected as the optimal balance between aerodynamic performance, generator compatibility, manufacturability, and structural practicality. This rotor size generates sufficient starting torque to overcome the cogging torque of commonly available permanent magnet generators while maintaining rotational speeds that can be efficiently matched using practical gearbox ratios.

A three-blade rotor configuration has been adopted due to its superior balance between airflow, torque generation, and rotational stability. The configuration minimizes aerodynamic blockage within the Venturi throat while maintaining reliable startup performance under low wind conditions. The 120° blade spacing also reduces vibration and wake interference, ensuring smoother operation and improved durability.

The turbine is housed within a Venturi throat section featuring an internal diameter of 467.2 mm, providing a blade tip clearance of 5 mm. This clearance minimizes aerodynamic losses while preventing blade-wall contact during operation. The straight throat section is approximately 700 mm long, providing sufficient space for the complete powertrain assembly and promoting stable airflow through the turbine.

The internal powertrain consists of a rotor hub, low-speed shaft, planetary gearbox, permanent magnet generator, and aerodynamic tail cone. The gearbox increases rotational speed before power generation, while the tail cone minimizes wake turbulence and aerodynamic drag. Together, these components form an integrated aerodynamic pod positioned within the throat section.

The omnidirectional intake system is designed to capture wind from multiple directions and direct it efficiently toward the Venturi throat. Curved Coanda-effect surfaces and guide vanes help align and accelerate incoming airflow. Downstream of the throat, a helical diffuser promotes pressure recovery and enhances the overall efficiency of the system.

Material selection has been optimized for tropical environmental conditions, structural reliability, and cost-effective manufacturing. Turbine blades and aerodynamic pod components are intended to be manufactured using PETG or ABS through additive manufacturing. The throat and diffuser structures utilize rolled galvanized iron sheet metal, while the intake assembly is constructed from fiberglass reinforced plastic (FRP). Polycarbonate or aluminum sheets are used for guide vanes, and the supporting tower structure is fabricated from mild steel square tubing.

The completed prototype is designed as a compact, transportable, and experimentally practical wind energy platform suitable for university-level research and performance validation. The project aims to demonstrate the effectiveness of Venturi-assisted wind acceleration and diffuser augmentation in improving wind turbine performance under low wind speed conditions.

Engineering Defense: Why the 46 cm DAWT Cannot Produce 250W
1. The Kinetic Energy Deficit at Local Wind Speeds
The fundamental limit of any wind system is the raw kinetic energy available in the air. At the established local average wind speed of 1.46 m/s, the air simply does not carry enough physical mass to generate heavy wattage through a small opening.

Ambient Wind: 1.46 m/s

DAWT Amplified Throat Wind: 3.65 m/s (using a highly optimistic 2.5x multiplier)

Throat Area (46 cm diameter): 0.166 square meters

Total Available Kinetic Power: 0.5 × 1.16 kg/m³ × 0.166 m² × (3.65)³ = 4.69 Watts

Conclusion: Even if the turbine, gearbox, and generator were 100% perfectly efficient (which is physically impossible), the absolute maximum energy entering the system is 4.69W. It is a strict violation of the Law of Conservation of Energy to extract 250W from a 4.69W source.

2. The 21 m/s Velocity Paradox & Aerodynamic Choking
To mathematically force 250W of electrical output from a 46 cm pipe (factoring in 25% total system efficiency), the wind speed inside the throat must reach 21.75 m/s.

To accelerate the ambient 1.46 m/s wind to 21.75 m/s, the system requires an Area Ratio of nearly 15:1.

The Physical Reality: Constructing an intake funnel large enough to achieve a 15:1 ratio creates a massive flat surface area facing the wind. Instead of smoothly flowing into the throat, the air pressure will instantly build up inside the funnel, creating a high-pressure "wall." The incoming wind will simply bounce off this wall and bypass the turbine completely—a condition known as aerodynamic choking.

3. The RPM vs. Torque Mismatch
Small-scale 250W generators require high speeds (usually 2000+ RPM) to produce voltage, necessitating a 1:5 gearbox.

The blades will easily spin the gearbox up to 2000 RPM when freewheeling.

However, the moment a 250W electrical load is applied, the internal electromagnetic resistance (cogging torque) of the generator engages.

Because the 3.65 m/s wind only provides about 4.7W of physical pushing force, it will instantly be overpowered by the 250W of magnetic resistance. The blades will completely stall and lock in place.

4. The Sizing Reality Check for a 250W DAWT
To successfully build a DAWT that outputs 250W in Katugastota's 1.46 m/s ambient wind, we must calculate the required throat size using the realistic 3.65 m/s internal flow and a 25% system efficiency.

Required Kinetic Energy: 1000 Watts

Calculation: 1000 W = 0.5 × 1.16 kg/m³ × Area × (3.65 m/s)³

Required Area: 35.4 square meters

Required Throat Diameter: 6.7 meters (22 feet)

Conclusion: To hit the 250W target in this specific geographic location, the central metal pipe alone would need to be nearly 7 meters wide, with an intake funnel over 20 meters wide. This exceeds the structural and financial scope of a university undergraduate prototype.

