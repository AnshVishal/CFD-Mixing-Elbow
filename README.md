<h1 align='center'>CFD STUDY OF MIXING ELBOW</h1>
<p align="center"><i>Disclaimer: This project is a part of an Assignment submitted at Flowthermolab.</i></p>
<h2 align='center'>OVERVIEW</h2>
      <p align='left'><b>1. Problem Statement</b></p>
<ul>
  <li>Pressure Based Solver, Steady state CFD Simulation</li> 
  <li>Study the flow phenomenon (mixing), velocity and temperature profile</li> 
  <li>Study must be conducted over Inlet-big at 20m/s and 60<sup>o</sup>C and Inlet-Small at 30m/s and 100<sup>o</sup>C</li>
</ul>
<p align="left"><b>Note: </b> <i>It is to highlight that this study has been performed to understand the internal fluid flow dynamics (mixing) through the Mixign Elbow geometry and the studied parameters such as Velocity Profile and Temperature changes so as to understand what are the design changes from perspective of a CFD Engineer (Refer to Discussion Section for more details.)</i><br/>Also, this case has been run for the geometry provided by FlowthermoLab while designed a mixing elbow geometry.</p>
<p align='justify'><b>2. Software Used: </b><br/> Ansys Space-Claim  &nbsp | &nbsp Ansys Fluent Mesher &nbsp | &nbsp Ansys Fluent &nbsp | &nbsp Ansys Post Processor &nbsp | &nbsp MATLAB (for Scientific Plots)</p>
<p align='justify'><b>3. Skills Demonstrated: </b><br/>Volumetric Geometry/Domain Preparation &nbsp | &nbsp Pressure based & Steady &nbsp | &nbsp Turbulence (k-omega SST) &nbsp | &nbsp Data Post-Processing</p>





        
<h2 align='center'>METHODOLOGY</h2>
<p>Methodology for the following process comprised of geometry refinement, Domain Preparation in Spaceclaim, meshing the geoemtry for different valve openings, defning the solver details, Solution Details like generating run time residuals and animations, understanding the convergence of results through plots, study results and plot them in MATLAB/python, concluding the project with findings and future scope.</p> 


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
<p>In this study CFD Simulations for the Globe Valve over the valve for different valve openings (1mm, 3mm, 5mm, 11mm, 21mm) for different Pressure inlet conditions (4 bar, 5 bar, 8 bar) keeping pressure outlet at 3 bar constant (for all cases). Pressure and Velocity were studied through contours understanding the pressure changes and flow rates at different location. Plot for discharge coefficient and mass flow rate.<br/> 
  &nbsp&nbsp It can be observed from the results main pressure drop occured at the valve throat due to diminished area at less valve lift values. The inherent flow coefficient was obtained through CFD keeping the pressure difference constant for full range (1 ~ 21mm) of opening and obtained the discharge Coefficient and mass flow rate.<br/> 
  &nbsp&nbsp Three most common flow characteristics of a valve which are called quick (fast) opening type, linear type and equal percentage type.
  <ul>
    <li><b><i>Quick opening type</i></b> produces a large increase in flow rate for initial increase in valve ope is usually used for safety or cooling system where the instant large flow is required. </li>
    <li><b><i>Linear type</i></b> has a linear relationship between the flow rate and the valve opening that is commonly used in liquid level conrol applications.</li>
    <li><b><i>Equal percentage type</i></b> provides a small increase in flow rate with the initial valve openings and a significant rise with the greater openings and is widely found in pressure control and heat transfer process. </li>
  </ul>
  &nbsp&nbsp The pressure drop was studied from the contours, the pressure at two planes that comprised of proper representation of valve opening the flow circulation and pressure changes. As it is evident from the graph represented above quick opening flow charateristic and the graph resembles the common characteristic trend for discharge rate and mass flow rate.<br/> <br/>
  &nbsp&nbsp <b><i>Findings Summarized:</i></b> 
  <ul>
    <li>The data generated concluded that there were significant changes in pressure around globe valve specially in small (1mm, 3mm) valve opening, maximum force on the valve 2143.762 N was recorded at pressure difference 5bar and with valve lift the it reduced upto 90.49 N.</li>
    <li>The discharge rate coefficient reduced with more valve lift decreased while the mass flow rate increased, maximum discharge coefficient 0.6012 was recorded at pressure difference 5bar Pa with minimum mass flow rate 1.54 kg.s<sup>-1</sup>recorded at pressure difference 1bar </li>
  </ul>
  &nbsp&nbsp <b><i>Future Scope:</i></b> 
  <ul>
    <li>Perform study to capture cavitation effects</li>
    <li>Perform Preliminary Study and investigate the optimization methods</li>
    <li>Optimize the design of control valve and reduce the force exerted on valve make globe valve more efficient and reduce loud noise generated from globe valve </li>
  </ul>
</p>

    

