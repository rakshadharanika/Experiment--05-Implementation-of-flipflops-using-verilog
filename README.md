# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: V RAKSHA DHARANIKA
RegisterNumber: 23013260 





### D FLIPFLOP:




![Exp5 dfp code](https://github.com/rakshadharanika/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149348380/3007c92b-443d-4c6c-9f36-295781a4aea1)





### T FLIPFLOP:





![Exp5 tfp code](https://github.com/rakshadharanika/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149348380/48921cc0-5687-4569-90fc-5f1fc64fef75)






### JK FLIPFLOP:






![Exp5 jkfp code](https://github.com/rakshadharanika/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149348380/6076bedf-4988-46d1-8527-3255f17109c9)







### SR FLIPFLOP:








![Exp5 srfp code](https://github.com/rakshadharanika/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149348380/86d6f9b4-c914-4b2c-9c74-ea2e37bbb10c)









### RTL LOGIC FOR FLIPFLOPS 




### D FLIPFLOP:






![Exp5 dfp RTL diagram](https://github.com/rakshadharanika/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149348380/807131a9-a289-48af-a916-7c4467b19f5a)







### T FLIPFLOP:





![Exp5 tfp RTL diagram](https://github.com/rakshadharanika/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149348380/99eaaa4a-7b3e-4285-8c60-f86d1d66d3c2)









### JK FLIPFLOP:











![Exp5 jkfp RTL diagram](https://github.com/rakshadharanika/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149348380/35e5c661-c2e4-487a-a00b-e7312734cd4d)










### SR FLIPFLOP:











![Exp5 srfp RTL diagram](https://github.com/rakshadharanika/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149348380/325b8b32-fb75-427f-ae70-f589172c500f)












### TIMING DIGRAMS FOR FLIP FLOPS :







### D FLIPFLOP:







![d wave](https://github.com/rakshadharanika/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149348380/118ee810-9517-4487-ad42-8c595ea357bf)








### T FLIPFLOP:








![t wave](https://github.com/rakshadharanika/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149348380/3d903a98-e95b-4ef5-a500-8fbd73f07b0e)








### JK FLIPFLOP:









![jk wave](https://github.com/rakshadharanika/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149348380/984e9a27-984b-4646-92bb-4295c741eb12)






### SR FLIPFLOP:





![sr wave](https://github.com/rakshadharanika/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149348380/e1882f1d-615b-4fe0-97dd-d4bfe3d27d3d)







### RESULTS 
