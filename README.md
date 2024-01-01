# FEA Portofolio by Rui Vieira
Welcome to my FEA Portfolio, showcasing diverse projects and analyses in linear and nonlinear static analysis, fatigue cycles, and buckling across metallic structures. Detailed analyses will later be accessible through the project titles.

#### Stack
- CAD & Design : NX, Inventor
- Solvers : Nastran, CalculiX
- Pre-/Post-Processing : NX, PrePoMax, ParaView

### [Watch components analysis](https://github.com/vierui/FEA-Portfolio/tree/main/2D-nonLin-watch-wheel-spring/README.dm "2D plane-stress watch components")
The crown wheel transmits the winding motion to the mainspring. The click-spring), is a ratchet mechanism that prevents the mainspring from unwinding, thus retaining the energy stored during winding

#### Objective
Determine the maximum torque required for tooth passage in the crown wheel and the maximum stress in the click spring, providing insights into mechanical efficiency and material stress limits.

#### Hyphotesis 
- 2D Plane Stress (XY)
- Nonlinear (NASTRAN - SOL402)

#### Main Results
<p align="center">
<img
  src="https://github.com/vierui/FEA-Portfolio/blob/main/2D-nonLin-watch-wheel-spring/torque-tooth-passage.png"
 width="810">
</p>

<p align="center">
Figure 1-1 : Crown wheel torque measure 
</p>

<p align="center">
<img
  src="https://github.com/vierui/FEA-Portfolio/blob/main/2D-nonLin-watch-wheel-spring/stress-critical-area-design-efficiency.png"
 width="800">
</p>

<p align="center">
Figure 1-2 : Highest stress profile and definition of a critical area (VonMises Nodal)
</p>

#### Dicussion
- Identification of constraints exceeding the elastic limit, leading to high risk of plastic deformations.
- Identification of maximum torque and stress points calling out for design improvement.
- It is suggested to replace the standard steel with spring steel for better fatigue resistance.
- Extremely high contact pressure (over 4000 MPa), indicating a need for surface treatment to improve friction.
- Possibility to increase torque while maintaining constant stress by increasing the friction coefficient.

### [2D Axisymmetric analysis of a copper extrusion process](https://github.com/vierui/FEA-Portfolio/tree/main/stat-housing-flange/README.dm "2D axisymmetric extrusion process")
Examination of the extrusion process in copper wire, focusing on stress profiles and plastic deformations. It combines simulation with empirical validation, offering insights into the complexities of material behavior under stress.

#### Objective
- Analyze stress profiles in extruded copper wire section.
- Study plastic deformations and stress in the matrix (die) and extruded copper wire.
- Determine the thrust force of the hydraulic cylinder.
- Examine the extrusion process.

#### Hyphotesis 
- Structural axisymmetric modeling (2D) with SOL 402 (Non-linear).
- Assumptions include large strains and material nonlinearity.

#### Main Resuts
- The yield limit of the matrix material exceeded, indicating critical areas.
- Critical zones located upstream of diameter restriction.
- Copper exhibits stick-slip effect; piston experiences non-linear movement.
- Simulation results align with hand calculations, confirming the accuracy of the simulation.

<p align="center">
<img
  src="https://github.com/vierui/FEA-Portfolio/blob/main/nonlinear-copper-extrusion/resctrition-profile-plasticity-stress.png"
 width="810">
</p>

<p align="center">
Figure 2-1 : Extrusion section stress-profile (left) and copper's plastic strain (right)
</p>

<p align="center">
<img
  src="https://github.com/vierui/FEA-Portfolio/blob/main/nonlinear-copper-extrusion/press-matrix-stress.png"
 width="450">
</p>

<p align="center">
Figure 2-2 : Matrix high stress highlight (VonMises Nodal)
</p>

**Discussion**
- Matrix material properties need modification to avoid work hardening; preheating copper could reduce stress.
- Non-axial displacement of the piston observed, contributing to significant upstream stresses.
- The simulation demonstrates plastic growth in material, supporting the hypothesis.

### [Aerospace panel buckling analysis](https://github.com/vierui/FEA-Portfolio/tree/main/stat-housing-flange/README.dm "Buckling aeropspace panel")

#### Objective
Investigate the buckling behavior of an F/A-18 structural-wing panel, exploring both linear and nonlinear analysis methods for a comprehensive understanding of the panel's structural integrity.

#### Hyphotesis 
- Linear approach (NASTRAN - SOL101)
- Nonlinear approach (NASTRAN - SOL402)
- Multiple mesh models
- 3D Shell

#### Main Results
<p align="center">
<img
  src="https://github.com/vierui/FEA-Portfolio/blob/main/buckling-shell-aerospace-panel/panel-nodal-avrg-vonmises.png"
 width="800">
</p>

<p align="center">
Figure 3-1 : linear stress (left) vs nonlinear stress (right) (VonMises Nodal)
</p>

<p align="center">
<img
  src="https://github.com/vierui/FEA-Portfolio/blob/main/buckling-shell-aerospace-panel/panel-nodal-displ.png"
 width="800">
</p>

<p align="center">
Figure 3-2 : out of plane displacement : linear (left) vs non linear (right)
</p>

<div align="center">
  
|  Comparison                                   | Linear   | Nonlinear |
|-----------------------------------------------|----------|-----------|
| Number of elements around the hole            | 30       | 30        |
| Number of nodes                               | 5633     | 5633      |
| Max Von Mises stress on the inner edge of the hole | 533 MPa | 429 MPa   |
| Max principal stress on the inner edge of the hole | 508 MPa | 427 MPa   |
| Maximum out-of-plane displacement             | 1.17 mm  | 6.44 mm   |
</div>

<p align="center">
Table 3-1 : Linear vs. nonlinear main results summary .
</p>

#### Discussion
- The study underscores the limitations of linear solutions in certain scenarios, advocating for the necessity of nonlinear analysis in similar contexts.
- The stress exerted on the piece exceeds the elastic limit of standard steel and may even surpass the tensile strength of lower-grade steels.
- Suggests potential material improvements and structural modifications for enhanced performance.

### [Linear actuator's Housing and flange analysis](https://github.com/vierui/FEA-Portfolio/tree/main/stat-housing-flange/README.dm "Static housing and flange")
Static analysis of a ACL2 120 linear actuator gear's housing and its flange focusing on fatigue load cases and material behavior under stress."

#### Objective
- Perform finite element structural analysis on the screw drive of an ACL2 120 linear actuator.
- Determine stress and fatigue effects on the screw drive under varied loads.

#### Hyphotesis 
- Linear static analysis with emphasis on fatigue load cases.
- Assumptions include material properties based on FKM criteria and the application of maximum load conditions.

#### Main Results


<div align="center">

|                       | FEA Model  | Analytical Value | Decision |
|-----------------------|------------|------------------|----------|
| Max Deformations [mm] | 0.016      | 0.006            | Accepted |
| Max Stresses [MPa]    | 15.18      | 8.36             | Accepted |
| Max Support Force [N] in x | 1872  | 1872             | Accepted |

</div>
<p align="center">
Table 4-1 : Results values summary
</p>

<p align="center">
<img
  src="https://github.com/vierui/FEA-Portfolio/blob/main/stat-housing-flange/flange-react-forces.png"
 width="400">
</p>

<p align="center">
Figure 4-1 : Housing & flange reaction forces
</p>

- Analysis showed low deformation and stress values, indicating endurance within limits.
- Discrepancies between numerical and analytical results were observed but not significant.
- 
#### Discussion
- Need for more accurate force application modeling for realistic load distribution.
- Screw drive's design validated for endurance under given conditions.

### [Linear actuator's worm gear analysis](https://github.com/vierui/FEA-Portfolio/tree/main/stat-housing-flange/README.dm "Static worm gear")
Structural integrity analysis of a worm gear from a ACL2 120 linear actuator to evaluate its performance under fatigue stress conditions.

#### Objective
- Analyze and evaluate the structural performance of a worm gear in an ACL2 120 linear actuator under fatigue stress.
- Identify potential structural weaknesses and assess gear longevity and reliability.

#### Hypothesis
- CTETRA(10)
- Bearings has initial boundary conditions 
- Hypothesizes that the gear can withstand specified loads without significant deformation or failure, using linear static analysis and fatigue load cases.

#### Main Results
An Haigh diagram is used  to assess the fatigue life of materials under varying stress conditions. It graphically represents the relationship between stress amplitude and mean stress, helping to determine safe stress levels to avoid material failure.
<p align="center">
<img
  src="https://github.com/vierui/FEA-Portfolio/blob/main/stat-worm-gear/worm-gear-haigh-diagram.png"
 width="400">
</p>

<p align="center">
Figure 5-1 : Haigh diagram for the CrMn
</p>

<p align="center">
<img
  src="https://github.com/vierui/FEA-Portfolio/blob/main/stat-worm-gear/worm-gear-stress-nodal.png"
 width="400">
</p>

<p align="center">
Figure 5-2 : Worm gear stress 
</p>

- Analysis revealed minimal deformation and stress, suggesting good structural integrity.
- High safety factor
- Some discrepancies between numerical and analytical results were within acceptable limits.

#### Discussion
- Affirms the structural robustness of the worm gear.
- Recommends refining force application model for accurate load distribution and enhancing gear design.

