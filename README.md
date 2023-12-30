# Exp-6-Synchornous-counters - up counter and down counter 
### AIM: To implement 3 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## UP COUNTER 
The counter is a digital sequential circuit and here it is a 3 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

 
 

3-bit “Up” Counter

![Screenshot 2023-12-30 140044](https://github.com/Gowtham-jk/Exp-7-Synchornous-counters-/assets/149857834/77b51171-dbdd-47ac-af18-c35a270d0e71)



## DOWN COUNTER 

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.

![Screenshot 2023-12-30 140114](https://github.com/Gowtham-jk/Exp-7-Synchornous-counters-/assets/149857834/b73c65c4-e40f-4def-9790-c337d532a4c7)


3-bit Count Down Counter
### Procedure
1.Create a new project in Quartus II software. 2.Name the project as uc for upcounter and dc for downcounter. 3.Create a new Verilog HDL file in the project file. 4.Name the module as dc and uc for downcounter and upcounter. 5.Within the module declare input and output variables. 6.Complete the program. 7.End the module.

### PROGRAM 

Program for flipflops  and verify its truth table in quartus using Verilog programming.

Developed by: Gowtham V

RegisterNumber: 23006362 

### RTL LOGIC UP COUNTER AND DOWN COUNTER  

### UP COUNTER

![Screenshot 2023-12-30 134513](https://github.com/Gowtham-jk/Exp-7-Synchornous-counters-/assets/149857834/0b9b1047-33eb-4baf-acd9-042648d62239)

###  DOWN COUNTER  

![Screenshot 2023-12-30 134520](https://github.com/Gowtham-jk/Exp-7-Synchornous-counters-/assets/149857834/34247ab3-d609-456a-9edc-969a88611bd8)


### TIMING DIGRAMS FOR COUNTER  

### UP COUNTER

![Screenshot 2023-12-30 134529](https://github.com/Gowtham-jk/Exp-7-Synchornous-counters-/assets/149857834/fb328a3d-6643-4975-a4ed-a347b1095b20)

###  DOWN COUNTER  
![Screenshot 2023-12-30 134535](https://github.com/Gowtham-jk/Exp-7-Synchornous-counters-/assets/149857834/7a84ddc3-1735-418a-a983-a08175cb408e)


### TRUTH TABLE 
### UP COUNTER
![Screenshot 2023-12-30 134541](https://github.com/Gowtham-jk/Exp-7-Synchornous-counters-/assets/149857834/7e614ff1-793f-4e5c-a208-9def415b491f)


###  DOWN COUNTER  

![Screenshot 2023-12-30 134547](https://github.com/Gowtham-jk/Exp-7-Synchornous-counters-/assets/149857834/5017b902-2591-43e7-8993-7853deaa2fa1)




### RESULTS 
Thus, the flipflops are implemented using verilog.
