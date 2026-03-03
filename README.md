<h1 align='center'>Computing Mizing Elbow</h1>
<h4 align='center'>Volumetric Geometry/Domain Preparation &nbsp | &nbsp Pressure based & Steady &nbsp | &nbsp Turbulence (k-omega SST) &nbsp | &nbsp Data Post-Processing</h4></h1>

<p align="right">Minor Project - Mixing Elbow,</br> Flowthermolab </br>18/08/2025</p>
<h2 align='left'>Project Overview</h2>
<p align = "left">This project presents a steady-state CFD analysis of a Mixing Elbow to investigate:</br>
<ul><li>Flow mixing behavior</li>
      <li>Velocity distribution</li>
      <li>Temperature profile</li>
      <li>Outlet uniformity</li></ul>
</p>

<h2 align "left">Problem Statement</h2>
<p align='left'>Perform a Pressure-Based, Steady-State CFD Simulation to analyze mixing inside a pipe elbow with two inlets:</br>
<table align = "center">
      <tr><th>Inlet</th><th>Velocity</th><th>Temperature</th></tr>
      <tr><td>Big Inlet</td><td>20 m/s</td><td>60<sup>o</sup>C</td></tr>
      <tr><td>Small Inlet</td><td>30 m/s</td><td>100<sup>o</sup>C</td></tr>
      <tr><td>Outlet</td><td>Pressure Outlet</td><td> - </td></tr>
</table>
Objective: </br>
<ul><li>Study velocity field behavior</li>
      <li>Analyze temperature mixing</li>
      <li>Evaluate outlet flow uniformity</li>
      <li>Suggest flow control improvements</li></ul>
</p>

<h2 align = "left">Software Used</h2>
<p align='justify'>
      1. &nbsp Ansys Space-Claim ------- Geometry Cleanup and refinement </br> 
      2. &nbsp Ansys Fluent Mesher ----- Mesh / Grid Generation </br>
      3. &nbsp Ansys Fluent ------------- Computation </br>
      4. &nbsp Ansys Post Processor ---- Post Processing </br>
      5. &nbsp MATLAB ------------------ Data Analysis & Scientific Plots</p>
 
<h2 align = "left">Methodology</h2>
<h3 align = "left">1. Geometry Cleanup and refinement</h3>
<p align = "justify">
      <ul><li>Cleaned provided geometry for computation</li>
            <li>Internal flow domain extracted for simulation.</li></ul></p>
<p align = "center"><img width="250" height="626" alt="image" src="https://github.com/user-attachments/assets/259042b6-0fac-45e4-880c-db3c2dfe5958" /><br/> <b>Domain prepared (Mixing Elbow)</b></p>

<h3 align = "left">2. Mesh Details</h3>
<p align = "justify">
      <ul><li>Surface mesh max size: 7 mm</li>
            <li>Curvature normal angle: 12<sup>o</sup></li>
            <li>2 cells per gap</li>
            <li>First layer height: 0.00022168 mm</li>
            <li>Y+ ≈ 1</li>
            <li>12 boundary layers (growth rate: 1.01)</li>
            <li>Poly-Hexcore volumetric meshFocused on mesh refinement at: Valve throat, Valve seat, and Valve lift region.</li></ul>
      Mesh Statistics:
      <ul><li>Nodes: 142,154</li>
            <li>Elements: 52,776</li></ul>
</p>
<p align = "center"><p align='center'><img width="250" height="673" alt="image" src="https://github.com/user-attachments/assets/f4de9db3-dbfe-4765-9a56-37d1cb2e0d80" /><br/>
      <b>Meshed Domain (Number of Elements: 52776)</b></p>


<h3 align = "left">3. Solver Settings</h3>
<table align="center">
<tr><th>Parameter</th><th>Setting</th></tr>
<tr><td>Solver Type</td><td>Pressure-Based</td></tr>
<tr><td>Time</td><td>Steady</td></tr>
<tr><td>Turbulence Model</td><td>k-ω SST</td></tr>
<tr><td>Material</td><td>Water (Liquid)</td></tr>
<tr><td>Inlet Velocities</td><td>20 m/s & 30 m/s</td></tr>
<tr><td>Inlet Temperatures</td><td>60°C & 100°C</td></tr>
<tr><td>Outlet</td><td>Pressure Outlet</td></tr>
<tr><td>Discretization</td><td>Second Order Scheme</td></tr>
<tr><td>Residuals & Monitors</td><td><ul><li>Area-weighted average temperature at outlet</li>
      <li>Area-weighted average velocity at outlet</li>
      <li>Mass flow rate balance</li></ul></td></tr>
<tr><td>Initialization</td><td>Hybrid</td></tr>
<tr><td>Iterations</td><td>~2000 (Converged ~250)</td></tr>
</table>

<h3 align = "left">4. Results</h3>

<h4 align = "left">1. Velocity Contours</h4>
<ul align='left'><li>For Velocity Contours: 
      <ul><li>Figure below shows how the flow velcoity changes at it transists from 2 inlets to outlet.</li>
            <li>Red color shows max velocity points/regions & blue color shows the least, lengends can be seen on left center of all images</li></ul>
</li></ul>
<p align = "center"><img width="400" height="848" alt="image" src="https://github.com/user-attachments/assets/1ffd80de-c812-4885-9265-c5b4165c58b0" /><img width="400" height="848" alt="image" src="https://github.com/user-attachments/assets/8f4ea8ed-de38-4e05-9e85-fdea0ac56250" /><br/>
      <b>Velocity Streamlines, Vectors & Contours (Flow Doamin XY plane)</b></p>

<h4 align = "left">Temperature Contours</h4>
<ul align='left'><li>For Temperature Contours: 
      <ul><li>Figure below shows that velocity contours and velocity vectors highlighting the flow direction and velocity changes.</li>
            <li>Figure 4 shows Temperature at inlet 1 is 60<sup>o</sup>C and at inlet 2 is 100<sup>o</sup>C, as the flow progress the mixing of temperature can be observed.</li>
            <li>Red color shows max temperature points/regions & blue color shows the least, lengends can be seen on left center of all images</li></ul>
</li></ul>
<p align = "center"><img width="400" height="848" alt="image" src="https://github.com/user-attachments/assets/66d9ab3d-02b7-4703-bad9-54b4679e5f21" /><img width="400" height="503" alt="image" src="https://github.com/user-attachments/assets/e11ba915-22b0-4ed2-b6fb-c0833523b7cb" /><br/>
      <b>Temperature Contours at outlet</b></p>

<h4 align = "left">Velocity and Temperature Profiles</h4>
<ul align='left'><li>For Velocity & Temperature Profiles: 
      <ul><li>Line Coordinates at which the profile data points are extracted: (101.6, 203.2, 9.331), (203.2, 203.2, 1.5553). This line is at the outlet plane.</li>
            <li>Temperature at 102.1 mm is 333.15 K and at 203.2 mm is 341.31 K. Maximum Temperature at 188.9 mm is 354.18 K</li>
            <li>Maximum Velocity at 188.4 mm is 25.877 m/s</li></ul>
</li></ul>
<p align="center"><p align='center'><img width="400" height="479" alt="image" src="https://github.com/user-attachments/assets/a7debf1f-03c6-4fd9-96ab-b6a65092285d" /><img width="400" height="478" alt="image" src="https://github.com/user-attachments/assets/f8bfec47-1303-4877-b8ea-ccb8d6055902" /><br/>
      <b>Temperature & Velocity Profile at Outlet</b></p>


<h2 align='left'>Discussion & Future Scope</h2>

<p>There are two inlet same liquid i.e. water at different velocity (Inlet1 = 20m/s and Inlet2 = 30m/s) and temperature (Inlet1 = 60 degree Celsius and Inlet2 = 100 degree Celsius) are injected in the pipe and undergoes mixing and at Outlet generating:
<ul><li>Mass Flow Average temperature = 336.507 K</li>
<li>Max. Temperature at Mid-Section Line = 354.18 K</li></ul>

Mixing Elbow Problem was solved, and results were analyzed. Below is conclusion of findings:
<ul><li>Maximum temperature recorded is 354.18 K and is not uniform over the entire Outlet of Pipe.</li>
<li>From the Velocity and Temperature Contour it can be concluded that the flow is not mixed properly.</li></ul>

Temperature and Velocity recorded at outlet: 
<ul><li>Area Average of Temperature at outlet = 336.111 K</li>
<li>Area Average of Velocity at outlet = 21.8739 m/s</li>
<li>Mass Flow Average of Temperature on outlet = 336.507 K</li>
<li>Mass Flow Average of Velocity on outlet = 22.1749 m/s</li></ul>
</p>

<p>FLOW CONTROL STRATEGIES:
<table align='center'>
      <tbody>
            <tr><th>METHOD</th><th>MIXING EFFICIENCY INCREASES</th><th>PRESSURE DROP PENALTY</th></tr>
            <tr><th>HELICAL STATIC MIXER</th><th>+50–70%</th><th>+15–20%</th></tr>
            <tr><th>PULSATING FLOW</th><th>+30–50%</th><th>+5%</th></tr>
            <tr><th>ACOUSTIC EXCITATION</th><th>+20–40%</th><th>Negligible</th></tr>
      </tbody>
</table></p><br/>

<p>QUANTITATIVE COMPARISON METHODS:
<table align='center'>
      <tbody>
            <tr><th>METHOD</th><th>MECHANISM</th><th>PROS</th><th>CONS</th></tr>
            <tr><th>CO-FLOW INJECTION</th><th>Secondary fluid injection</th><th>Simple implementation</th><th>Requires extra plumbing</th></tr>
            <tr><th>ELECTROHYDRODYNAMICS</th><th>Electric field-induced vortices</th><th>No moving parts</th><th>High voltage needed</th></tr>
            <tr><th>MAGETIC STIRRING</th><th>Ferrofluid + rotating magnets</th><th>Precise control</th><th>Limited to conductive fluids</th></tr>
      </tbody>
</table></p><br/>
<p>
Final Recommendation:<br/>
Reduce Smaller inlet Velocity (More CFD Simulations to identify the right velocity) and use Helical Static mixer
</p>

<h2>Recommended Repository Structure</h2>
<pre>
CFD-Study-Globe-Valve/
│
├── README.md
├── Geometry image
├── Mesh images
├── Fluent_Case_Files
├── Results & Data
</pre>

<p><b>Author:</b></br> 
      Ansh Vishal, </br>Aerospace Engineer</br>
      <a href="anshvishal215@gmail.com">anshvishal215@gmail.com</a></br>
      <a href="https://www.linkedin.com/in/ansh-vishal/">LinkedIn</a></p>



