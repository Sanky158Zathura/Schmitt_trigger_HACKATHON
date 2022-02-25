# Schmitt Trigger in 28nm CMOS
Technology
Sanket M Mantrashetti
RV College of Engineering(Bangalore)



Abstract-The Scope of the work is to design 2 Schmitt trigger using 28nm CMOS technology with relatively lower power consumption and low area. The proposed Schmitt triggers works for low voltage and has an intended use over high-speed applications. It is designed using 3 PMOS and 3 NMOS. 
Keywords-PMOS NMOS CMOS highspeed  
1.INTRODUCTION
Schmitt triggers made of CMOS have a wide application in both analog and digital technology. They are widely used to shape the signals. They convert irregular shaped signals to triangular or square pulse. Schmitt trigger are found useful to remove noise from signals and mechanical contact bounce in switches.
Lately aggressive scaling of CMOS to nanometer have found application in various fields. Schmitt trigger works on the principle of comparator, when the input is greater  or lower than a chosen threshold the output switches.                   Schmitt trigger designed using OP-Amp and feedback resistors have high power losses and greater area consumption over the chip. While the CMOS technology benefits over both the drawbacks of conventional method.
Schmitt trigger provides two switching thresholds one for positive-going and other for negative-going input signal,               but the comparator gives only one switching threshold. This feature of Schmitt trigger is called hysteresis. Various Schmitt triggers are compared for noise margin and noise stable from the hysteresis curve.
2.Circuit Details
1.Circuit 1 - Consider Vout = 0 and Vin <=Vdd at this state P3 is on and there is path to ground for Node A. When Vin changes from Vdd to 0 and Vout changes from 0 to Vdd, the output is compromised because current has a alternative path to ground through P3 till Vout raises such that P3 goes to off condition. So there is a slight variation in waveform from the ideal waveform when plotted for high frequency input voltage. Considering the other case When Vout = Vdd and Vin >= Vdd at this stage N3 is on and there is path to Vdd for  node B. . When Vout changes from Vdd to 0 and Vin changes from 0 to Vdd, the output is compromised because current has a alternative path to Vdd through N3 till Vout decreases such that N3 goes to off condition.
2. Circuit 2 - Assuming Vin is low and Vout is low, So N1,N3 are in cutoff region and similarly P1,P3 are in saturation region. For Vin to change from low to high, N1 turns on slowly, the voltage at node B decrease, and vout increase slowly. Since the voltage Vp can be changed, so this acts as threshold voltage for positive form of the output and similarly Vn acts as threshold voltage for negative part of the output. Circuit 2 dominates Circuit 1  for having 2 threshold voltages.

