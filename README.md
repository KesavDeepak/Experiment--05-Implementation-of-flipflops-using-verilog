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
#### Step 1: 
Prepare 470 Ohm Resistors. For this step you need 2 470 ohm resistors....

#### Step 2: 
Mount the 10K Resistors.

#### Step 3: 
Mount the First Transistor.

#### Step 4: 
Mount the Second Transistor....

#### Step 5: 
Mount the LED Lights.

#### Step 6: 
Mount the Capacitors...

#### Step 7: 
Mount the Power Supply.....

#### Step 8: 
Ready.


### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
### Developed by: KESAV DEEPAK SRIDHARAN
### RegisterNumber: 23002011
*/
## T FLIP FLOP
![793309ed-40b2-427c-861c-3fe7f347e371](https://github.com/KesavDeepak/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139336019/3d397b78-4063-4fd5-bd54-0d47176f37a5)

## D FLIP FLOP
![f758954c-6065-48f9-bff0-b5ebbc63bbd4](https://github.com/KesavDeepak/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139336019/1a6c484a-af3e-418f-87fe-8f601c255717)

## JK FLIP FLOP
![02a93915-f2bb-4daf-943b-1624ba0a994d](https://github.com/KesavDeepak/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139336019/1609beb7-1b78-4812-aa45-bd002e7f1a70)

## SR FLIP FLOP
![36100716-4e40-457d-b884-cb0967b0d013](https://github.com/KesavDeepak/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139336019/94d6cf10-751a-44e9-9058-5b142f9d3f95)






### RTL LOGIC FOR FLIPFLOPS 
## SR FLIP FLOP
![d5ed1847-d850-4cc1-a537-adb1864502fa](https://github.com/KesavDeepak/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139336019/470c2653-69e7-4928-88b5-6a0daca9314a)

## JK FLIP FLOP
![9cc936fd-ff27-424d-bfd8-a7a08c77ae0e](https://github.com/KesavDeepak/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139336019/4978ddee-2dee-46c1-aa8d-883332d8f74a)

## D FLIP FLOP
![cd656416-e2dd-4b28-bea8-e303c5d88952](https://github.com/KesavDeepak/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139336019/571abd5f-452d-44ab-8b8b-f27d29f62abd)

## T FLIP FLOP
![299861c0-49a4-46e5-9efd-89c184dcaeb5](https://github.com/KesavDeepak/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139336019/6f6f2597-5bb9-4666-9eba-9c4905171f77)






### OUTPUT:

### TIMING DIGRAMS FOR FLIP FLOPS 
## SR FLIP FLOPS
![d96cba7b-a857-41e1-bf37-8ecb5d9d8f4c](https://github.com/KesavDeepak/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139336019/95e6d0cc-ac98-46d2-b97a-62cde29d003b)

## JK FLIP FLOP
![1b5bbe89-68e4-467e-a329-69a8854be8a5](https://github.com/KesavDeepak/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139336019/89b68bfc-cd17-4d85-b08d-6a370d768b22)

## D FLIP FLOP
![f23d85a0-fe69-459a-9e5f-bf35a8e2594f](https://github.com/KesavDeepak/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139336019/4bece53e-b0bf-41ce-9b3b-73ca0eb726b7)

## T FLIP FLOP
![283bbbca-c55d-4ec4-be90-134115c38c62](https://github.com/KesavDeepak/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139336019/709e55ab-50f1-4028-abcc-1c8ac90ac532)








### RESULTS 
Implementation of flip flops using verilog successfully completed.
