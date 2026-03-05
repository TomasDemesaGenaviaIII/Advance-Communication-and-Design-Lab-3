# EXP 12: PCM ENCODING
## OBJECTIVES
> 1. To observe the conversion of an analog message signal into a serial stream of 0s and 1s.
> 2. To investigate the process of sampling, quantisation, and encoding using the Emona Telecoms-Trainer 101.
> 3. To identify the relationship between input analog voltages and their corresponding 8-bit binary numbers.
> 4. To examine the effect of quantisation error and the role of the Frame Synchronisation (FS) signal.
## MATERIALS
> 1. Emona Telecomms-Trainer 101 (plus power-pack)
> 2. Dual-channel 20MHz oscilloscope
> 3. Master Signals, PCM Encoder, Variable DCV, VCO
> 4. Three scope leads and assorted patch leads
# PROCEDURES
## PART A: AN INTRODUCTION TO PCM ENCODING USING A STATIC DC VOLTAGE
> 1. Gather a set of the equipment listed above.
> 2. Set up the scope per the instructions in Experiment 1. Ensure that the Trigger Source is set to CH1 and Mode is set to CH1.
> 3. Locate the PCM Encoder module and set its Mode switch to the PCM position.
> 4. Connect the set-up where the PCM Encoder module is clocked by the Master Signals module’s 8kHz DIGITAL output and its analog input is connected to 0V DC.

<img width="3131" height="2440" alt="image" src="https://github.com/user-attachments/assets/82bcd05f-e181-4b8b-a602-0950fc61c274" />


> 5. Adjust the scope's Timebase control to view three pulses of the PCM Encoder module's FS output.
> 6. Set the scope's Slope control to the position to start the sweep when the FS signal goes from high to low.
> 7. Adjust the scope’s Horizontal Position control so that the start of the trace aligns with the left-most vertical line on the screen.
> 8. Set the scope's Timebase control to the 0.1ms/div position.
> 9. Adjust the scope's Variable Sweep control until the FS signal matches the required reference.

<img width="2868" height="2151" alt="image" src="https://github.com/user-attachments/assets/7a2bb5f3-6bb9-463b-90ef-6848501562cd" />


> 11. Set the scope's Mode control to the DUAL position to view the PCM Encoder module’s CLK input as well as its FS output.
> 12. Draw the two waveforms to scale, leaving enough room for a third digital signal.
> 13. Connect the scope's Channel 2 input to the PCM Encoder module's output.

<img width="1524" height="1148" alt="image" src="https://github.com/user-attachments/assets/04b79553-cab1-4175-a94e-b28b392e836a" />
> 15. Draw the resulting waveform (10 bits of data) to scale on the graph paper.



## BLOCK DIAGRAM
<img width="2443" height="2123" alt="image" src="https://github.com/user-attachments/assets/92bb6c2e-1e2b-456a-8093-00beded35c30" />
<img width="2581" height="2258" alt="image" src="https://github.com/user-attachments/assets/1a2f0480-5e5e-4df7-8862-2764cf583bf4" />




 
