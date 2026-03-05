# EXP 11: SAMPLING AND RECONSTRUCTION
## OBJECTIVES
1. To investigate the reconstruction of a sampled signal using a tuneable low-pass filter.
2. To observe the process of sampling a continuous signal using different techniques, specifically Natural and Sample-and-Hold.
3. To demonstrate the phenomenon of aliasing and verify the Nyquist-Shannon Sampling Theorem.
## MATERIALS 
1. Emona Telecomms-Trainer 101 (plus power-pack)
2. Dual-channel 20MHz oscilloscope
3. Master Signals, Dual Analog Switch, Speech, Tuneable LPF, VCO
4. BNC-to-banana oscilloscope leads and assorted patch leads
# PROCEDURES

## PART A: SAMPLING A SIMPLE MESSAGE
> 1. Gather the required equipment and ensure the trainer is powered.
> 2. Connect the 2KHz SINE output from the Master Signals module to the IN socket of the Dual Analog Switch.
> 3. Connect the 8KHZ DIGITAL output to the CONTROL input of the switch.
> 4. Set the oscilloscope's Trigger Source to CH1 and the Mode to CH1.
> 5. View the 2KHz SINE output on CH1 and adjust the Timebase to view approximately two cycles.
> 6. Connect the output of the switch to CH2 of the scope and switch the scope to DUAL mode.
> 7. Set the Vertical Attenuation controls to 1V/div.
> 8. Natural Sampling: Observe the waveform where the pulses follow the shape of the message signal.
> 9. Sample-and-Hold: Modify the set-up to use the S/H circuit (Figure 4) and observe the resulting waveform.



## BLOCK DIAGRAM
<img width="612" height="453" alt="Part A Block Diagram" src="https://github.com/user-attachments/assets/4ad896ff-ecf7-444d-9ad6-46e9f2da6a08" />

## PART B: SAMPLING SPEECH
> 10. Disconnect the plugs from the Master Signals 2KHz SINE output.
> 11. Connect the lead to the Speech module’s output as shown in Figure 6.
> 12. Set the oscilloscope Timebase to 2ms/div.
> 13. Talk, sing, or hum while watching the display to see the sampled representation of a complex signal.



## BLOCK DIAGRAM
<img width="598" height="533" alt="Paart B Block Diagram" src="https://github.com/user-attachments/assets/b9b2534e-924d-4539-9007-7b1c6a835099" />

## PART C: RECONSTRUCTING A SAMPLED MESSAGE
> 14. Return the Timebase to 0.1ms/div and reconnect the 2KHz SINE message.
> 15. Set the Tuneable LPF module's Gain to the middle and turn the Cut-off Frequency Adjust fully anti-clockwise.
> 16. <img width="1362" height="948" alt="image" src="https://github.com/user-attachments/assets/c601b7a6-2bad-4ebf-8df1-cd616e8ef1b5" />
<img width="1339" height="943" alt="image" src="https://github.com/user-attachments/assets/32b7defe-8f73-4803-bb90-946791ab2ca4" />
<img width="1343" height="969" alt="image" src="https://github.com/user-attachments/assets/36b190fa-ab6a-4de7-9073-fed1a71cc5e3" />






