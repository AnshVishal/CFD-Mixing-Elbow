<h1 align='center'>CFD STUDY OF MIXING ELBOW</h1>
<p align="center"><i>Disclaimer: This project is a part of an Assignment submitted at Flowthermolab.</i></p>
<h2 align='center'>OVERVIEW</h2>
      <p align='left'><b>1. Problem Statement</b></p>
<ul>
  <li>Pressure Based Solver, Steady state CFD Simulation</li> 
  <li>Study the flow phenomenon (mixing), velocity and temperature profile</li> 
  <li>Study must be conducted over Inlet-big at 20m/s and 60<sup>o</sup>C and Inlet-Small at 30m/s and 100<sup>o</sup>C</li>
</ul>
<p align="justify"><b>Note: </b> <i>It is to highlight that this study has been performed to understand the internal fluid flow dynamics (mixing) through the Mixign Elbow geometry and the studied parameters such as Velocity Profile and Temperature changes so as to understand what are the design changes from perspective of a CFD Engineer (Refer to Discussion Section for more details.)</i><br/>Also, this case has been run for the geometry provided by FlowthermoLab while designed a mixing elbow geometry.</p>
<p align='justify'><b>2. Software Used: </b><br/> Ansys Space-Claim  &nbsp | &nbsp Ansys Fluent Mesher &nbsp | &nbsp Ansys Fluent &nbsp | &nbsp Ansys Post Processor &nbsp | &nbsp MATLAB (for Scientific Plots)</p>
<p align='justify'><b>3. Skills Demonstrated: </b><br/>Volumetric Geometry/Domain Preparation &nbsp | &nbsp Pressure based & Steady &nbsp | &nbsp Turbulence (k-omega SST) &nbsp | &nbsp Data Post-Processing</p>


              
<h2 align='center'>METHODOLOGY</h2>
<p align='justify'>Methodology for the following process comprised of geometry refinement, Domain Preparation in Spaceclaim, meshing the geoemtry for different valve openings, defning the solver details, Solution Details like generating run time residuals and animations, understanding the convergence of results through plots, study results and plot them in MATLAB/python, concluding the project with findings and future scope.</p> 


<table align="center">
<tbody> 
  <tr> <th valign='top'><h3 align='left'>1. Geometry & Domain</h3><p align='left'>Geometry was cleaned for computation study, and extract the domain of study. Ensured proper domain extraction and noted the dimensions required for the processing part.</p></th>
      <th><p align='center'><img width="250" height="626" alt="image" src="https://github.com/user-attachments/assets/259042b6-0fac-45e4-880c-db3c2dfe5958" /><br/>Figure 1: Domain prepared (Mixing Elbow)</p></th>
  </tr>
<tr> <th valign='top'><h3 align='left'>2. Meshing</h3><p align='left'>The geometry was meshed in Ansys Fluent Mesher. Imported at a tolerance of 0.01mm with Surface mesh of max size 7mm at 12<sup>o</sup> curvature normal angle and 2 cells per gap to capture the effects at the corners properly. Caculated the first boundary layer height at y<sup>+</sup>=1. used Uniform Boundary layer offset method with 12 layers growth rate of 1.01 and 0.00022168mm first layer height. Generating Poly hexcore volumetric mesh for 142154 nodes and 52776 elements.</p></th>
      <th><p align='center'><img width="250" height="673" alt="image" src="https://github.com/user-attachments/assets/f4de9db3-dbfe-4765-9a56-37d1cb2e0d80" /><br/>Figure 2: Meshed Domain (Number of Elements: 52776)</p></th>
  </tr> 
<tr> <th valign='top'><h3 align='left'>3. Solver Details</h3>
      <ul align='left'><li>Study was performed for pressure based solver at steady time for k-omega SST Viscous Model using Coupled based Solver through second order Scheme for pressure, moemntum and other turbulence parameteres.</li>
            <li>Water was used as Study Fluid, keeping inlet velcoity at 20m/s & 30 m/s for two inlet respectively and temperature at both inlet at 60<sup>o</sup> and 100<sup>o</sup>C and pressure based outlet. None was the convergence criteria, while monitored the flow convergence through area weighted average for temperature and velcoity at outlet and Mass flow rate at inlet and outlet.</li> 
            <li>Used Hybrid Initialization and ran ~2000 iterations while the convergence was observed around 250 iterations.</li></ul></th>
      <th> - </th>
  </tr> 
<tr> <th valign='top'><h3 align='left'>4.1. Velocity Results: Flow Domain</h3>
      <ul align='left'><li>Figure 3 shows how the flow velcoity changes at it transists from 2 inlets to outlet.</li>
            <li>Red color shows max velocity points/regions & blue color shows the least, lengends can be seen on left center of all images</li>
      </ul></th>      
      <th> <p align='center'><img width="250" height="848" alt="image" src="https://github.com/user-attachments/assets/1ffd80de-c812-4885-9265-c5b4165c58b0" /><img width="250" height="848" alt="image" src="https://github.com/user-attachments/assets/8f4ea8ed-de38-4e05-9e85-fdea0ac56250" /><br/>Figure 3: Velocity Streamlines, Vectors & Contours (Flow Doamin XY plane)</p>
</th></tr> 
<tr> <th valign='top'><h3 align='left'>4.2. Temperature Results: Flow Domain</h3>
      <ul align='left'><li>Figure 4 shows that velocity contours and velocity vectors highlighting the flow direction and velocity changes.</li>
      <li>Figure 4 shows Temperature at inlet 1 is 60<sup>o</sup>C and at inlet 2 is 100<sup>o</sup>C, as the flow progress the mixing of temperature can be observed.</li>
      <li>Red color shows max temperature points/regions & blue color shows the least, lengends can be seen on left center of all images</li></ul></th>      
      <th><p align='center'><img width="250" height="848" alt="image" src="https://github.com/user-attachments/assets/66d9ab3d-02b7-4703-bad9-54b4679e5f21" /><img width="250" height="503" alt="image" src="https://github.com/user-attachments/assets/e11ba915-22b0-4ed2-b6fb-c0833523b7cb" /><br/>Figure 4: Temperature Contours at outlet</p>
</th></tr> 
<tr> <th valign='top'><h3 align='left'>4.3. Velocity and Temperature Profile at Outlet</h3>
      <ul align='left'><li>Line Coordinates at which the profile data points are extracted: (101.6, 203.2, 9.331), (203.2, 203.2, 1.5553). This line is at the outlet plane.</li>
      <li>Temperature at 102.1 mm is 333.15 K and at 203.2 mm is 341.31 K. Maximum Temperature at 188.9 mm is 354.18 K</li>
      <li>Maximum Velocity at 188.4 mm is 25.877 m/s</li></ul></th>      
      <th><p align='center'><img width="250" height="479" alt="image" src="https://github.com/user-attachments/assets/a7debf1f-03c6-4fd9-96ab-b6a65092285d" /><img width="250" height="478" alt="image" src="https://github.com/user-attachments/assets/f8bfec47-1303-4877-b8ea-ccb8d6055902" /><br/>Figure 5: Temperature & Velocity Profile at Outlet</p>
</th></tr> 

</tbody>
</table>

<h2 align='center'>DISCUSSION & FUTURE SCOPE</h2>

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
    

