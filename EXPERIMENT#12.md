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



## BLOCK DIAGRAM
<img width="2443" height="2123" alt="image" src="https://github.com/user-attachments/assets/92bb6c2e-1e2b-456a-8093-00beded35c30" />
<img width="2581" height="2258" alt="image" src="https://github.com/user-attachments/assets/1a2f0480-5e5e-4df7-8862-2764cf583bf4" />

## PART B: PCM ENCODING OF VARIABLE DC VOLTAGE
> 14. Set the scope's Mode control to the CH1 position.
> 15. Set the scope's Trigger Source control to the EXT position.
> 16. Set the scope's Trigger Source Coupling control to the HF REJ position.
> 17. Modify the set-up to include the Variable DCV module to change the DC voltage on the PCM Encoder module's input.

<img width="1808" height="1365" alt="image" src="https://github.com/user-attachments/assets/f0754c11-f410-4047-b64f-b4d3f18e67cc" />

> 18. Set the scope's Channel 1 Vertical Attenuation control to the 1V/div position.
> 19. Set the scope's Channel 1 Input Coupling control to the GND position.
> 20. Use the scope's Channel 1 Vertical Position control to align the trace with a horizontal line (zero volt reference).
> 21. Set the scope's Channel 1 and Channel 2 Input Coupling controls to the DC position.
> 22. Set the scope's Mode control to the DUAL position.
> 23. Adjust the Variable DCV module's Variable DC control until the PCM Encoder module outputs the 0V code.
> 24. Measure the Variable DCV module's output voltage (should be close to 0V).
> 25. Turn the Variable DCV module's Variable DC control clockwise.
> 26. Continue turning clockwise until the PCM Encoder module's output is 11111111.
> 27.  Record the input voltage in Table 1.
> 28.  Devise a method (using a Buffer or Adder) to reach the upper and lower limits of the input range if necessary.
> 29.  Adjust the setup for a small negative input voltage.
> 30.  Increase the negative voltage and observe the binary number output.
> 31.  Continue until the output is 00000000.
> 32.  Measure and record this value in Table 1.


## BLOCK DIAGRAM
<img width="2743" height="2398" alt="image" src="https://github.com/user-attachments/assets/e191bfe8-428b-4e30-b9b0-740965c004b1" />

## PART C: QUANTIZATION
> 33. Return to the basic variable DC setup and set the control to the middle of its travel.
> 34. Vary the control left and right slightly to observe that the output code remains unchanged until a quantisation threshold is crossed.



## PART D: PCM ENCODING OF CONTINUOSLY CHANGING VOLTAGES
> 35. Return the scope's Trigger Source control to CH1 and Trigger Source Coupling to AC.
> 36. Set the scope's Vertical Attenuation for both channels to 2V/div.
> 37. Locate the VCO module and set its Range control to the HI position.
> 38. Turn the VCO module's Frequency Adjust control fully anti-clockwise (for approx. 50kHz clock).
> 39. Disassemble the current set-up.
> 40. Connect the setup where the VCO clocks the PCM Encoder and a sinewave is applied to the input.
> 41. Set the scope's Timebase control to the 50µs/div position.
> 42. Watch the PCM Encoder module's PCM DATA output change continuously on the scope.
> 43. Return the scope's Variable Sweep control to the locked position.



<img width="1639" height="1231" alt="image" src="https://github.com/user-attachments/assets/a1f03eb5-0dcc-41f9-be58-c0d7e6e02d32" />

## QUESTIONA AND ANSWER
> 1. Indicate on your drawing the start and end of the frame. 
> 2. Indicate on your drawing the start and end of each bit. 
> 3. Indicate on your drawing which bit is bit-0 and which is bit-7.
> 4. What is the binary number that the PCM Encoder module is outputting at 0V?
> 5. Why does the code change even though the input voltage is steady?
> 6. Why does the PCM Encoder module output this code for 0V DC and not 00000000?
> 7. What happens to the Variable DCV module's output?
> 8. In what way does the binary number change?
> 9. Explain why you were unable to obtain 11111111.
> 10. Devise a method of obtaining a variable DC voltage that can reach the limits.
> 11. What happens to the binary number as the size of the negative input voltage increases?
> 12. What is the maximum allowable amplitude (peak-to-peak) for an AC signal?
> 13. What's the name for the difference between a sampled voltage and its closest quantisation level?
> 14.  Calculate the difference between the quantisation levels
> 15.  To reduce quantisation error it's better to have:
> 16.  To reduce quantisation error it's better to have:


>     ANSWERS


## DATA ANALYSIS AND RESULTS
| PCM ENCODER(OUTPUT) | PCM ENCOUDER (INPUT VOLTAGE)|
|------------------|--------------------|
| 11111111(+ PEAK) | + 2.5 V            | 
| 10000000 (MP)    | 0.00 V             | 
| 00000000 (- PEAK) | -2.5 V             | 
 
# LEARNING SUMMARY
