# **Jet Turbine Engine CAD \& Structural Analysis**



This is a personal project in which I designed a multi-stage axial turbofan engine in SolidWorks and put through a structural analysis in ANSYS Mechanical.



#### ***What This Is***



I modeled a single-spool turbofan motor, fan, four-row compressor, four-row turbine, all on one shaft, then ran a static structural FEA to see how it holds up under the loads it'd actually see while running: spinning at 12000 RPM, aerodynamic pressure on the blades, torque through the shaft, thrust, and gravity. The goal was to check the stress, deformation, and safety factor against Inconel 718, the material real turbine rotors are made from.



#### ***How the FEA was set up***



###### Material of the rotor: **Inconel 718**



* Density = 8190 kg/m^3
* Young's Modulus = 200 GPa
* Poisson's ratio = 0.29
* Tensile Yield Strength = 1100 MPa
* Tensile Ultimate Strength = 1375 MPa



###### Loads Applied:



* Rotational Velocity = 12000 RPM (1256 rad/s)
* Variable pressure on every blade row (compressor \& turbine)
* 600 Nm of torque on the shaft
* 5000 N of axial thrust on the rear bearing ends
* Standard Earth Gravity



###### How it's held in place: 



The rotor is constrained at the shaft's bearing location   











#### ***Results***



|*Result*|*Value* |*Location*|
|-|-|-|
|Max Deformation|1.11 mm|Fan blade tips|
|Max stress (von-Mises)|368.3 MPa|Casing ring (rear, near turbine)|
|Max elastic strain|0.00188 m/m|Casing ring (rear, near turbine)|
|Min safety factor|2.99|Casing ring (rear, near turbine)|





A safety factor of around 3.0 against Inconel 718's yield strength, which is well past the 1.5 that's usually treated as the floor in aerospace design.    







