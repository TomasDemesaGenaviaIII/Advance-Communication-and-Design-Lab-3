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
> 16. Connect the output of the Sample-and-Hold circuit to the IN of the Tuneable LPF.
> 17. Slowly turn the Cut-off Frequency control clockwise until the 2KHz sine wave is reconstructed on the oscilloscope.



<img width="1362" height="948" alt="image" src="https://github.com/user-attachments/assets/c601b7a6-2bad-4ebf-8df1-cd616e8ef1b5" />
<img width="1339" height="943" alt="image" src="https://github.com/user-attachments/assets/32b7defe-8f73-4803-bb90-946791ab2ca4" />
<img width="1343" height="969" alt="image" src="https://github.com/user-attachments/assets/36b190fa-ab6a-4de7-9073-fed1a71cc5e3" />

## BLOCK DIAGRAM
<img width="677" height="490" alt="Part C Block Diagram" src="https://github.com/user-attachments/assets/07caa501-1019-4a0f-9b90-7726e9c9f003" />


## PART D: INVESTIGATING ALIASING
> 18. Locate the VCO module, set Frequency Adjust fully clockwise, and set Range to LO.
> 19. Replace the fixed 8KHz control signal with the VCO variable frequency output.
> 20. Monitor the reconstructed signal on CH2 while slowly decreasing the VCO frequency.
> 21. Observe the distortion (aliasing) that occurs as the sampling rate drops below the Nyquist rate.


## BLOCK DIAGRAM
<img width="674" height="500" alt="Part D Block Diagram" src="https://github.com/user-attachments/assets/2a999c99-1f78-48a3-9485-7543851e4342" />

# RESULTS ANALYSIS AND REFLECTION

## PART A: SAMPLING 
<img width="628" height="476" alt="Part A Output" src="https://github.com/user-attachments/assets/36c57786-98f9-42b0-b933-587bb49c355a" />

<img width="622" height="470" alt="Part B Output" src="https://github.com/user-attachments/assets/0e32160e-e606-441b-9740-75d168f71077" />

<img width="621" height="456" alt="Part D Output" src="https://github.com/user-attachments/assets/50dbb844-be7b-41fa-b6da-81f875899344" />

The three waveforms depicted in the images illustrate different aspects of signal analysis, each offering insights into the behavior of the signal under various conditions. The first waveform, labeled "Part A: Sampling," shows a relatively clean sinusoidal wave, indicative of a well-sampled signal that accurately captures the original waveform without significant distortion. The measured parameters, such as the peak-to-peak voltage (Vpp) and frequency, suggest a stable and consistent signal, which is essential for precise digital representation. Moving to "Part B: Speech," the waveform appears more complex and less uniform, reflecting the natural variability inherent in speech signals. This complexity is characterized by fluctuations in amplitude and frequency, which are typical of human speech patterns and require more sophisticated processing to analyze effectively. The final waveform, "Part D: Aliasing," demonstrates the effects of inadequate sampling rates, where the waveform appears distorted and introduces artifacts that do not correspond to the original signal. This aliasing effect results from undersampling, causing the high-frequency components to fold back into lower frequencies, thereby corrupting the integrity of the signal. Overall, these waveforms highlight the importance of proper sampling techniques and the challenges posed by real-world signals like speech. They underscore how critical it is to select appropriate sampling rates and filtering methods to preserve signal fidelity and avoid distortions such as aliasing.




