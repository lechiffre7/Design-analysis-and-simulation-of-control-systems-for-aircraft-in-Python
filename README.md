# Design-analysis-and-simulation-of-control-systems-for-aircraft-in-Python
Develop a modeling and simulation framework using Python to analyze and verify the design of aircraft flight control systems (FCS) using system algebra formal methods. The goal is to demonstrate the capability of system algebra to assess system properties like availability, redundancy, coupling and fault tolerance.
For this case we are using longitudinal aicraft contrpol.




  **State variabes**:
  
1. $\delta u$: Change in forward velocity
2. $\delta \theta$: Change in pitch angle
3. $\delta q $: Change angle in pitch rate
4. $\delta \alpha $: Change in angle of attack

   **Control Inputs:**
   
   $\delta_{elevator}$: Elevator deflection
   
 **System Equation:** 
 
 1.**Equation for $\delta u$**:
 
 $\dot{\delta} u = \frac{1}{m_1}\left(D\left(\alpha_0, \delta_{\alpha}, \delta_{q}, \delta_{u}\right)\right) - m.g.\sin\left(\alpha_{0} + \delta_{\alpha}\right) + T_{thrust}\left(\delta_{elevator}\right)$
 
 2. **Equation for $\delta \theta$**:

 $\dot{\delta}\theta = \delta q$

3. **Equation for $\delta q$**

   $\dot{\delta} q = \frac{1}{I_{yy}}\left(-L\left(\alpha_{0}, delta_{\alpha}, \delta_{q}, \delta_{u}\right).c_{mean} - M\left(\alpha_{0}, \delta_{\alpha}, \delta_{q}, \delta_{u}\right).c_{mean}.\delta \theta + Q_{elevator}\left(\delta_{elevator}\right)\right)$

4. **Equation for $\delta\alpha$**:

   $\dot{\alpha} = \delta q$

   Where:

   1. $\alpha_0$: Angle of attack at trim,
   2. $c_{mean}$ : Mean aeordynamic chord,
   3. $\left(D\left(\alpha_0, \delta_{\alpha}, \delta_{q}, \delta_{u}\right)\right)$: Aeorodynamic drag,
   4. $\left(L\left(\alpha_0, \delta_{\alpha}, \delta_{q}, \delta_{u}\right)\right)$: Aerodynamic lift,
   5. $\left(M\left(\alpha_0, \delta_{\alpha}, \delta_{q}, \delta_{u}\right)\right)$: Aerodynamic pitching moment,
   6. $Q_{elevator}\left(\delta_{elevator}\right)$: Elevator effectiveness term.
   7. $T_{thrust}\left(\delta_{elevator}\right)$: Thrust force.
   
