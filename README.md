# Venturi_X_Omnidirectional_Wind_Turbine
This project focuses on the development, simulation, and validation of a  highly  optimized Diffuser Augmented Wind Turbine (DAWT). The design introduces specific fluid dynamic  modifications to accelerate ambient air, effectively lowering the minimum wind speed required for  operation. 

Here is the engineering justification for why a 1.5-foot rotor is the ultimate sweet spot, especially when it comes to matching the turbine to off-the-shelf generators and powertrain components.
1. Overcoming Generator "Cogging Torque"
Every Permanent Magnet Synchronous Generator (PMSG) or DC motor has "cogging torque." This is the initial magnetic resistance you feel when you try to spin the shaft by hand.
•	A tiny 1-foot rotor has very little mechanical leverage (a short moment arm). In Peradeniya’s low 2 m/s winds, a 1-foot blade will likely stall because it cannot generate enough raw twisting force to break the generator's magnetic resistance.
•	A 1.5-foot rotor significantly increases the moment arm. It generates enough starting torque to punch through the cogging resistance of standard small generators (like NEMA 23/34 stepper motors wired as generators, e-bike hub motors, or small marine alternators), allowing the system to actually start spinning in low winds.
2. The RPM and Gearbox Matching
To generate useful electricity, your generator needs to spin fast (often 1000 to 3000 RPM).
•	A 2-foot blade rotates relatively slowly, meaning you would need a massive, heavy gear ratio (like 1:20) to get the generator up to speed. High gear ratios introduce terrible mechanical friction, which kills efficiency.
•	A 1.5-foot blade naturally spins at a much higher baseline RPM. This means you only need a small, lightweight, standard gear ratio (like 1:5 or 1:10) to reach your target generator speed. Standard planetary gearboxes in these ratios are cheap and easy to source.
3. Ease of Blade Manufacturing (3D Printing)
You mentioned earlier that you are transitioning to custom blade profiles (SG6043 to S809) with serrated trailing edges.
•	If you plan to 3D print these blades, an 18-inch (450 mm) diameter means each individual blade is roughly 8 to 9 inches long.
•	This length fits perfectly diagonally on the build plate of standard, low-cost desktop 3D printers (like a Creality Ender 3). If you went up to 2 feet, the blades would be too large to print in one piece, forcing you to slice them and glue them together, which introduces severe structural weak points under high centrifugal loads.
4. Optimal Overall Rig Size
Maintaining your 9:1 area ratio, sizing the throat to 1.5 feet keeps the rest of your tower incredibly manageable for a university workshop build:
•	Throat Diameter: 1.5 feet (0.45 m)
•	Intake Diameter: 4.5 feet (1.37 m)
•	Total Estimated Height: ~6.5 to 7 feet. This creates a rig that is small enough to fit inside a standard pickup truck or laboratory door, yet large enough to prove the fluid dynamics definitively to your panel.


You should use exactly 3 blades for your rotor.
This matches the exact specifications of the Sunforce 600 turbine used in the original research paper's field demonstration. However, beyond just copying the paper, there is a very strict aerodynamic and mechanical reason why a 3-blade configuration is the absolute best choice for your specific 1.5-foot scaled-down setup. 
Here is the engineering breakdown of why 3 blades is the magic number for your Venturi throat:
1. The Perfect Balance of "Solidity" and Airflow
In turbine design, "solidity" refers to the percentage of the swept area that is blocked by solid blade material.
•	If you use more blades (e.g., 5 or 6): The rotor becomes too solid. While this gives you massive starting torque, it acts like a wall inside your narrow Venturi pipe. It creates severe aerodynamic blockage, choking the high-speed air stream and completely destroying the velocity jump you need.
•	If you use fewer blades (e.g., 2): The rotor spins incredibly fast, but it lacks the physical surface area to generate enough raw rotational force (torque) at low wind speeds. It would struggle to break the "cogging torque" (magnetic resistance) of your generator during Peradeniya's 2 m/s lulls.
•	The 3-Blade Sweet Spot: Three blades provide just enough surface area to guarantee a strong, reliable start-up torque without choking the aerodynamic flow through the Venturi throat.
2. Gyroscopic Stability and Vibration
A 1.5-foot rotor spinning at high RPMs inside a rigid pipe acts like a massive gyroscope.
•	A 2-blade rotor creates unequal weight distribution during rotation, leading to severe harmonic vibrations. In an open-air turbine, this causes tower wobble; inside your tight Venturi pipe, this vibration will cause your blade tips (which only have a 5 mm clearance) to scrape against the inner walls and shatter.
•	A 3-blade rotor provides perfect $120^\circ$ radial symmetry. The center of mass remains perfectly stable, resulting in smooth, vibration-free rotation even under heavy wind shear.
3. Wake Interference
We previously discussed how your serrated trailing edges will break up the wake vortices. If you pack 4 or 5 blades into a 1.5-foot circle, the blades are too close together. The turbulent wake from one blade will smash directly into the leading edge of the next blade, causing it to stall. Spacing exactly 3 blades at $120^\circ$ gives the air just enough time to smooth out before the next blade passes through.
Here are the exact physical dimensions you need to manufacture your 1.5-foot throat section.
1. The Tip Clearance: 5 mm (0.2 inches)
You should aim for a tip clearance of exactly 5 mm (about 0.2 inches) between the edge of the blade and the inner wall of the pipe.
•	Why not smaller? (The Mechanical Limit): If you make the gap any smaller than 5 mm, you risk disaster. When the turbine spins at high RPMs, the blades will flex slightly forward under wind load, and the bearings will have a microscopic amount of play. A clearance tighter than 5 mm means the blades could easily scrape the inside of the throat, shattering your 3D-printed rotors.
•	Why not larger? (The Aerodynamic Limit): If you make the gap larger than 5 mm, you suffer from Tip Bleed. High-pressure air always seeks the path of least resistance. If the gap is too wide, the concentrated wind stream will bypass your blades entirely, slipping through the crack along the wall instead of doing the mechanical work of pushing your rotor.
2. The Inner Diameter (ID) of the Throat: 18.4 inches (467.2 mm)
Since clearance applies to both the left and right sides of the spinning rotor, you must add double the clearance value to your turbine diameter to find the true Inner Diameter (ID) of the pipe.
•	Turbine Diameter: 1.5 ft (18.0 inches / 457.2 mm)
•	Total Clearance (Both Sides): 0.4 inches (10.0 mm)
•	Final Throat Inner Diameter: 18.4 inches (467.2 mm or 1.53 ft)
Manufacturing Tolerance Warning
When Sachethana models this in SolidWorks, ensure the 18.4-inch dimension is the Inner Diameter (ID), not the Outer Diameter (OD). If you are buying a pre-made pipe (like PVC or acrylic), the wall thickness will dictate the Outer Diameter. If you buy an 18-inch OD pipe, the inside will be too small, and your blades won't fit.

The physical length of your straight horizontal throat section needs to be between 650 mm and 750 mm.
Here is the exact mechanical and aerodynamic breakdown of why it needs to be this long:
1. Housing the Internal Powertrain
Since you are mounting the mechanical components directly in the center of the pipe, the throat must act as a protective sleeve for the entire assembly. The combined length of your rotor hub, 1:5 planetary gearbox, 250W generator, and the aerodynamic tapering tail cone will measure approximately 600 mm. The pipe must be slightly longer than the pod itself to fully contain it before the expanding diffuser begins.
2. Flow Stabilization (The L/D Ratio)
In fluid dynamics, the Length-to-Diameter (L/D) ratio dictates how well the air stabilizes inside a pipe.
•	Your throat's Inner Diameter (ID) is 467.2 mm.
•	A throat length of roughly 700 mm gives you an L/D ratio of 1.5.
This 1.5 ratio is the absolute sweet spot for a Venturi system. It provides enough straight distance for the high-speed air to smoothly recombine behind your generator's tail cone, but it is short enough that you don't lose massive amounts of kinetic energy to the friction of the pipe walls.
Component	Dimension (mm)	Engineering Note
Turbine Rotor Diameter	457.2 mm	The exact span of the 3-blade custom SG6043 to S809 rotor.
Blade Tip Clearance	5.0 mm	The microscopic gap between the blade tip and the 467.2 mm pipe wall.
Aerodynamic Pod Length (Total)	~ 600.0 mm	The total length of the bullet-shaped casing housing your powertrain.
Rotor-to-Gearbox Spacing	85.0 mm	Shaft clearance behind the blades.
Gearbox Housing Length	140.0 mm	Standard footprint for a 1:5 planetary gear set.
Generator Housing Length	140.0 mm	Standard footprint for a 250W PMSG/alternator.
Tail Cone Taper Length	235.0 mm	The tapering back-end of the pod to prevent wake turbulence and drag.

Here is the exact spatial map of your 700 mm Venturi throat, starting from the absolute front edge ($0\text{ mm}$) where the straight pipe begins, all the way to the back edge ($700\text{ mm}$) where the expanding helical diffuser starts.
Think of this as the centerline blueprint for your aerodynamic pod.
The 700 mm Component Map (Front to Back)
[ 0 mm ] — START OF STRAIGHT THROAT (The curved elbow ends here)
•	The Front Buffer Zone ($50\text{ mm}$ length): This empty space allows the incoming air to recover from the 90-degree turn and straighten into a perfectly uniform, flat velocity profile.
[ 50 mm ]— TURBINE BLADES
•	The Rotor Plane ($0\text{ mm}$ thickness at centerline): This is the exact vertical slice where your 3-blade (1.5 ft diameter) rotor spins. It captures the stabilized air right at its maximum velocity.
[ 50 mm to 135 mm ]— SHAFT CLEARANCE
•	The Low-Speed Shaft ($85\text{ mm}$ length): This is the exposed spinning shaft connecting the back of your rotor hub to the front face of the gearbox. This physical gap is required so the flexing blades do not strike the stationary metal housing of the gearbox.
[ 135 mm to 275 mm ]— THE GEARBOX STAGE
•	1:5 Planetary Gearbox ($140\text{ mm}$ length): This is the front half of your enclosed aerodynamic pod. It takes the high-torque, low-RPM rotation from the blades and multiplies the speed for the generator.
[ 275 mm to 415 mm ]— THE GENERATOR STAGE
•	250W Permanent Magnet Generator ($140\text{ mm}$ length): This is the back half of your enclosed pod's main body. It receives the high-speed shaft rotation and converts it into your target electrical power.
[ 415 mm to 650 mm ]— THE AERODYNAMIC TAIL CONE
•	The Wake Eliminator ($235\text{ mm}$ length): The casing immediately begins to taper smoothly down to a point. This prevents the high-speed air from collapsing violently behind the flat back of the generator, eliminating aerodynamic drag.
[ 650 mm ]— END OF THE AERODYNAMIC POD
•	The Rear Buffer Zone ($50\text{ mm}$ length): The air comes off the tip of the tail cone and uses this empty space to smoothly recombine into a solid column of air before it gets pushed out of the straight pipe.
[ 700 mm ] — END OF STRAIGHT THROAT (The expanding helical diffuser begins here)



Materials:

Choosing the right materials is critical for this prototype. Because you are building this for testing in Sirimalwatta, the materials must balance aerodynamic smoothness, structural strength, weather resistance (tropical heat and humidity), and university-budget manufacturing.
Here is the master material breakdown for each specific component of your scaled-down DAWT, optimized for local workshop fabrication.
1. The Turbine Blades & Aerodynamic Pod
•	Recommended Material: 3D-Printed PETG (Polyethylene Terephthalate Glycol) or ABS.
•	Why: You are using highly complex custom shapes (SG6043 transitioning to S809 with serrated trailing edges). Hand-carving or fiberglassing these tiny serrations accurately is nearly impossible. 3D printing is the only way to get millimeter-perfect airfoils.
•	Warning: DO NOT USE PLA. While PLA is cheap and easy to print, its glass transition temperature is very low (around 60°C). Inside a metal throat under the Sri Lankan sun, PLA blades will soften, warp, and hit the inner walls. PETG or ABS will easily withstand the heat and the centrifugal forces.
2. The Horizontal Venturi Throat Pipe
•	Recommended Material: Rolled Galvanized Iron (GI) Sheet Metal (Gauge 18 or 20).
•	Why: The throat needs to have an exact Inner Diameter (ID) of 467.2 mm. Finding a standard PVC pipe in that exact specialty size is very difficult and expensive. A local metal workshop can easily take a flat, perfectly smooth GI sheet and run it through a slip roller to weld/rivet a perfect 467.2 mm pipe.
•	Aerodynamic Benefit: GI sheet metal has very low surface friction, which prevents boundary-layer drag inside the high-speed throat.
3. The Omnidirectional Intake (Coanda Lips & Funnel)
•	Recommended Material: Fiberglass Reinforced Plastic (FRP) over a carved foam core.
•	Why: The Coanda effect relies on beautiful, smooth, compound 3D curves. You cannot easily bend sheet metal into 3D convex bowl shapes in a basic workshop.
•	How to build it: 1. Carve the large 1.38m curved funnel shape out of cheap high-density polystyrene (styrofoam). 2. Wrap it in fiberglass cloth and brush it with epoxy resin. 3. Once it hardens, sand it smooth and paint it. This gives you an incredibly strong, ultra-lightweight, perfectly aerodynamic intake.
4. The 6 Rectangular Guide Vanes (Partition Walls)
•	Recommended Material: Polycarbonate sheets or Thin Aluminum Sheet.
•	Why: These are flat vertical walls that guide the wind into the funnel. Polycarbonate (Lexan) or thin aluminum is lightweight, completely weatherproof, and can easily be bolted directly into your fiberglass intake.
5. The Helical Diffuser (Exhaust Cone)
•	Recommended Material for the Cone: Rolled GI Sheet Metal. (Same as the throat, just rolled at a 6° expanding angle).
•	Recommended Material for the Helical Ridges: Flexible rubber tubing or 3D-printed strips.
•	Why: Instead of trying to manufacture a complex metal helix, you can build a smooth metal cone, and then industrial-glue heavy rubber tubing or printed plastic strips in a spiral pattern down the inner wall to create the vortex-generating ridges.
6. The Main Support Structure (The Tower)
•	Recommended Material: Mild Steel Square Tubing (e.g., 1.5-inch or 2-inch Box Iron).
•	Why: The 1.38m intake will act like a giant sail when a gust of wind hits it. You need a highly rigid, heavy base to prevent the rig from vibrating or tipping over. Mild steel is cheap, easy to arc-weld into a lattice tower, and provides the necessary counter-weight at the bottom. Just ensure you apply a good coat of anti-rust primer and enamel paint.
Summary Checklist for Purchasing:
1.	PETG Filament: For blades and the generator housing.
2.	GI Sheet Metal (18/20 Gauge): For the throat and diffuser cone.
3.	Fiberglass Kit (Cloth + Epoxy Resin): For the curved Coanda intake.
4.	Mild Steel Box Iron: For the frame and mounting brackets.



