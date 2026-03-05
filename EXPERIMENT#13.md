# EXP 13: PCM DECODING
## OBJECTIVES
> 1. To observe the process of converting a PCM data stream back into a Pulse Amplitude Modulation (PAM) signal.
> 2. To understand the critical role of clock and frame synchronization in digital decoding.
> 3. To reconstruct the original message and speech signals using a tuneable low-pass filter.

## INTRODUCTION
> Pulse Code Modulation (PCM) Decoding is the process of converting a digital PCM signal back into its original analog form. In a communication system, PCM decoding occurs at the receiver side after the signal has been transmitted over a channel. The encoded digital data consists of binary values that represent the sampled amplitudes of the original analog signal. During the decoding process, these binary codes are first interpreted and converted back into their corresponding quantized amplitude levels.

## MATERIALS
> 1. Emona Telecomms-Trainer 101 (plus power-pack)
> 2. Dual-channel 20MHz oscilloscope
> 3. PCM Encoder, PCM Decoder, Tuneable LPF, Buffer, VCO, Speech, Variable DCV
> 4. BNC-to-banana oscilloscope leads and assorted patch leads

# PROCEDURES
## PART A: SETTING UP THE PCM ENCODER
> 1. Gather a set of the equipment listed.
> 2. Set up the scope per Experiment 1. Ensure Trigger Source is CH1 and Mode is CH1.
> 3. Locate the PCM Encoder module and set its Mode switch to the PCM position.
> 4. Connect the set-up shown in Figure 1. (Note: Insert black plugs into GND).

## BLOCK DIAGRAM
<img width="3413" height="2482" alt="image" src="https://github.com/user-attachments/assets/a49f5891-31e4-49a5-9189-bbcbe070f121" />

<img width="1454" height="1092" alt="image" src="https://github.com/user-attachments/assets/8cef33e1-ab0d-419d-ab23-7e0aa13f5953" />



> 5. Set the scope's Slope control to the "-" position.
> 6. Adjust the scope's Timebase control to view one pulse of the PCM Encoder module's FS output (Tip: 10us/Div)
> 7. Set the Variable DCV module's Variable DC control to about the middle of its travel.
> 8. Set the scope's Mode control to the DUAL position to view the PCM Encoder module's PCM DATA output as well as its FS output.
> 9. Vary the Variable DCV module's Variable DC control left and right.
> 10. Confirm the number on PCM DATA output goes down and up.
> 11. Disconnect the plug to the Variable DCV module's VDC output.
> 12. Locate the VCO module and turn its Frequency Adjust control fully anti-clockwise.
> 13. Set the VCO module's Range control to the LO position.

## BLOCK DIAGRAM
<img width="3394" height="2665" alt="image" src="https://github.com/user-attachments/assets/ed7daf5a-a936-4598-bad4-a1eb794e2cc6" />

<img width="1604" height="1207" alt="image" src="https://github.com/user-attachments/assets/dbc50bc2-c1e5-47e2-a4ac-3c2505ea3a70" />



## PART B: DECODING THE PCM DATA
> 14. Return the scope's Slope control to the "+" position.
> 15. Set the scope's Mode control to CH1 position.
> 16. Modify the set-up as shown in Figure 5.

## BLOCK DIAGRAM
<img width="2793" height="1661" alt="image" src="https://github.com/user-attachments/assets/cb3f74d2-a5d9-4ebb-86a4-41ece0ad383a" />

<img width="3162" height="2525" alt="image" src="https://github.com/user-attachments/assets/5da3101e-6096-4873-9056-0db3ca3fe027" />

> 17. Adjust the scope's Timebase control to view two or so cycles of the message.
> 18. Set the scope's Mode control to the DUAL position to view the PCM Decoder module's output as well as the message signal.
> 19. Add the Buffer module to the set-up as shown in Figure 7 leaving scope connections as they are.
> 20. Turn the Buffer module's Gain control fully anti-clockwise.
> 21. Without wearing headphones, plug them into the Buffer module's headphone socket.
> 22. Put the headphones on.
> 23. Turn the Buffer module's Gain control clockwise until you can comfortably hear the PCM Decoder module's output.
> 24. Disconnect the Buffer module's lead where it plugs to the PCM Decoder module's output.
> 25. Modify the set-up as shown in Figure 8 below, again leaving the scope's connections as they are.
> 26. Compare the sound of the two signals. You should notice that they're similar but clearly different.

## PART C: ENCODING AND DECODING SPEECH
> 27. Completely remove the Buffer module from the set-up.
> 28. Disconnect the plugs to the VCO module's SINE output.
> 29. Modify the set-up as shown in Figure 9.
> 30. Talk, sing or hum while watching the scope's display.

## PART D: RECOVERING THE MESSAGE
> 31. Locate the Tuneable Low-pass Filter module and set its Gain control to about the middle.
> 32. Turn the Tuneable Low-pass Filter module's Cut-off Frequency Adjust control fully anti-clockwise.
> 33. Disconnect the plugs to the Speech module's output.
> 34. Modify the set-up as shown in Figure 10.
> 35. lowly turn the **Cut-off Frequency** control clockwise and stop the moment the message signal has been reconstructed (ignoring phase shift)
> 36. Add the **Buffer** module as shown in Figure 12.
> 37. Turn the Buffer module's **Gain** control fully anti-clockwise.
> 38. Put the headphones on.
> 39. urn the Buffer module's **Gain** control clockwise until you can hear the filter output.
> 40. Disconnect the Buffer lead from the PCM Decoder and connect it to the **VCO** output.
> 41. Compare the sound of the two signals; they should be very similar.

## BLOCK DIAGRAM

<img width="3500" height="1806" alt="image" src="https://github.com/user-attachments/assets/64a3aa5d-980d-4922-9278-1ef8843ea285" />

<img width="3125" height="2392" alt="image" src="https://github.com/user-attachments/assets/6d2b5e1d-8988-4241-9383-e54865fe779e" />



## QUESTION AND ANSWERS
> 1. What does the PCM Decoder's "stepped" output tell you about the type of signal that it is?
> 2. What must be done to the PCM Decoder module's output to reconstruct the message properly?
> 3. Even though the two signals look and sound the same, why isn't the reconstructed message a perfect copy of the original message?

>> ANSWERS

> 1. It indicates the signal is a Pulse Amplitude Modulation (PAM) signal. The "steps" show that the decoder is holding a specific voltage level for the duration of one frame before jumping to the next sampled value.
> 2. It must be passed through a Low-pass Filter. This filter removes the high-frequency transitions (the steps) and recovers the original smooth analog waveform.
> 3. This is due to Quantization Error. Because an 8-bit system only has 256 discrete levels to represent an infinite range of analog voltages, there is a small rounding difference (quantization noise) between the original signal and its digital representation.



## DATA ANELYSIS AND REFLECTION
>The experiment demonstrated that a "staircase" PAM waveform is the raw output of a PCM decoder. The sampling intervals are represented by the high-frequency "steps." The receiver maintained perfect alignment by "stealing" the transmitter's Clock and Frame Sync functions. The Tuneable LPF's final reconstruction step was crucial for smoothing the signal back into its analog form.
> The return to analog reality from digital data was clearly demonstrated in this lab. The most important takeaway was that bit and frame synchronization are absolutely necessary; without them, the data is just noise. In addition, it demonstrated how our reconstructed signal suffers from resolution limitations imposed by bit depth (8 bits), highlighting the significance of quantization theory in digital communications.
