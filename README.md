# Schmitt Trigger in 28nm CMOS
Technology
Sanket M Mantrashetti
RV College of Engineering(Bangalore)



**Abstract**-The Scope of the work is to design 2 Schmitt trigger using 28nm CMOS technology with relatively lower power consumption and low area. The proposed Schmitt triggers works for low voltage and has an intended use over high-speed applications. It is designed using 3 PMOS and 3 NMOS. 
Keywords-PMOS NMOS CMOS highspeed  


1.**INTRODUCTION**
Schmitt triggers made of CMOS have a wide application in both analog and digital technology. They are widely used to shape the signals. They convert irregular shaped signals to triangular or square pulse. Schmitt trigger are found useful to remove noise from signals and mechanical contact bounce in switches.
Lately aggressive scaling of CMOS to nanometer have found application in various fields. Schmitt trigger works on the principle of comparator, when the input is greater  or lower than a chosen threshold the output switches. Schmitt trigger designed using OP-Amp and feedback resistors have high power losses and greater area consumption over the chip. While the CMOS technology benefits over both the drawbacks of conventional method.
Schmitt trigger provides two switching thresholds one for positive-going and other for negative-going input signal,but the comparator gives only one switching threshold. This feature of Schmitt trigger is called hysteresis. Various Schmitt triggers are compared for noise margin and noise stable from the hysteresis curve.



**2.Circuit Details**

**1.Circuit 1** - Consider Vout = 0 and Vin <=Vdd at this state P3 is on and there is path to ground for Node A. When Vin changes from Vdd to 0 and Vout changes from 0 to Vdd, the output is compromised because current has a alternative path to ground through P3 till Vout raises such that P3 goes to off condition. So there is a slight variation in waveform from the ideal waveform when plotted for high frequency input voltage. Considering the other case When Vout = Vdd and Vin >= Vdd at this stage N3 is on and there is path to Vdd for  node B. . When Vout changes from Vdd to 0 and Vin changes from 0 to Vdd, the output is compromised because current has a alternative path to Vdd through N3 till Vout decreases such that N3 goes to off condition.

**2. Circuit 2** - Assuming Vin is low and Vout is low, So N1,N3 are in cutoff region and similarly P1,P3 are in saturation region. For Vin to change from low to high, N1 turns on slowly, the voltage at node B decrease, and vout increase slowly. Since the voltage Vp can be changed, so this acts as threshold voltage for positive form of the output and similarly Vn acts as threshold voltage for negative part of the output. Circuit 2 dominates Circuit 1  for having 2 threshold voltages.




**3.Circuit Design**

![image](https://user-images.githubusercontent.com/92454845/155769173-680e5be2-c827-4c7d-a269-8f511c969061.png)
CIRCUIT 1

![image](https://user-images.githubusercontent.com/92454845/155769262-8e83e089-864f-4c4b-a132-2b9a4282bc67.png)
CIRCUIT 2



**Transistor Dimensions**

Length = 28nm	Circuit 1	Circuit 2

	            Width(nm)	Width(nm)
              
P1	              560    	560

P2	              560	560

P3	              728    	280

N1	              280	280

N2	              280	280

N3	              630   	140


Length = 30nm	Circuit 1	Circuit 2

	            Width(nm)	Width(nm)
              
P1	              600    	600

P2	              600	600

P3	              780    	300

N1	              300	300

N2	              300	300

N3	              675   	150




**Simulation tool used**

SYNOPSYS

Synopsys is at the forefront of Smart Everything with the world's most advanced technologies for chip design, verification, IP integration, and software security and quality testing
Synopsys is an American electronic design automation company that focuses on silicon design and verification, silicon intellectual property and software security and quality. Products include logic synthesis, behavioral synthesis, place and route, static timing analysis, formal verification, hardware description language (SystemC, SystemVerilog/Verilog, VHDL) simulators, and transistor-level circuit simulation. 

![Screenshot 2022-02-25 001914](https://user-images.githubusercontent.com/92454845/155771264-cb82df72-b39c-4892-998a-1343de02d668.png)

Synopsys custom compiler

![info](https://user-images.githubusercontent.com/92454845/155771330-08392773-c4d5-495a-a1c0-ae9eb4b4c628.png)

libraries available in Synopsys

![Screenshot 2022-02-25 001938](https://user-images.githubusercontent.com/92454845/155771370-0e78a1e4-d590-4c23-8d25-3e7ec2edf369.png)

![Screenshot 2022-02-25 001959](https://user-images.githubusercontent.com/92454845/155771377-a7770493-6f79-48ae-b95b-d7622476471e.png)




**Simulation Implementation**

Design of Circuit 1

![1 design](https://user-images.githubusercontent.com/92454845/155769910-368e153e-fbca-457a-9af7-6e37b3a2a605.png)
This is design of Schmitt trigger 1 It consists of 6 Mosfets with tags for Vin Vout Vdd and GND. The 
Ciruit acts as skeleton for the Symbol.

Symbol for Circuit 1

![1 symbol](https://user-images.githubusercontent.com/92454845/155769870-dc20209f-e112-4bce-a567-3f68ef2fd517.png)


Circuit 1 implementation

![1 implementation](https://user-images.githubusercontent.com/92454845/155769929-eeb46c86-eab1-4df7-a642-6f9a9d883106.png)



Design for Circuit 2

![2 design](https://user-images.githubusercontent.com/92454845/155770059-e1d293f2-2c6f-4e57-b0cb-4e35c981d25a.png)
This Circuit is design of Schmitt trigger 2 Constructed using 6 mosfets with appropriative tags for input, output, ground and threshold voltages.

symbol for Circuit 2

![2 symbol](https://user-images.githubusercontent.com/92454845/155770116-728e1ba1-a77b-4afc-a12c-ef14105efdda.png)

Circuit 2 implementation

![2 implementation](https://user-images.githubusercontent.com/92454845/155770169-1d981c5c-d026-4f39-8139-4d4c19d69b77.png)




**Output Waveforms**

Waveform of Circuit 1

![1 output](https://user-images.githubusercontent.com/92454845/155770450-6013afdc-a990-448b-b4af-f840fa503646.png)

![output1](https://user-images.githubusercontent.com/92454845/155770527-00fabaf0-82fd-4ed8-b7dd-7d165e142978.png)

These waveforms corresponds to Circuit 1. The input provided is 2V peak to peak, frequency 50Hz and DC offset voltage of 0.5V. The output waveform obtained matches the pulse wave with amplitude 1V.It is plotted for transient analysis.


Waveform of Circuit 2

![2 op](https://user-images.githubusercontent.com/92454845/155770556-f7dacfdd-464a-48c6-bdca-51ec630948ca.png)

The waveform corresponds to The waveforms of circuit 2. . The input provided is 2V peak to peak, frequency 50Hz and DC offset voltage of 0.5V. Output of which is a pulse wave of aplitude 1V. Plotted for transient analysis.

hysteresis Curve

![1 hysteresis](https://user-images.githubusercontent.com/92454845/155770601-0b4ba9c5-51cb-4b1d-b7f9-43b1fd1be5c7.png)

This is plot of hysteresis Curve. Plotted using DC analysis by varying Vin linearly and plotting Vout. This plot corresponds to Vsat Vh and hysteresis loss during it's operation.


'#'**Acknowledgements**
1)Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.
2)Synopsys Inc
3)IIT Hyderabad
4)Analog IC Design Hackathon
5)Sameer Durgoji, NIT Karnataka
6)Chinmay Panda, IIT Hyderabad


**References**

1. http://web.mit.edu/Magic/Public/papers/00260219.pdf
2. R. Sapawi, R. L. S. Chee, S. K. Sahari and N. Julai, "Performance of CMOS Schmitt Trigger," 2008 International Conference on Computer and Communication Engineering, 2008, pp. 1317-1320, doi: 10.1109/ICCCE.2008.4580818.
3. W. Ibrahim, V. Beiu, M. Tache and F. Kharbash, "On Schmitt trigger and other inverters," 2013 IEEE 20th International Conference on Electronics, Circuits, and Systems (ICECS), 2013, pp. 29-32, doi: 10.1109/ICECS.2013.6815337.
4. https://ieeexplore.ieee.org/document/87026
