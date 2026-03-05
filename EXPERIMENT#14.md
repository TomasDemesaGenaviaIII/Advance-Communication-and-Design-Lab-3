# EXP 14: BANDWIDTH LIMITING AND RESTORING DIGITAL SIGNAL
## OBJECTIVES
> 1. To observe the effect of bandwidth limiting on a PCM communication system.
> 2. To model a communication channel using a low-pass filter.
> 3. To examine the effect of bandwidth limiting on digital signal shape.
> 4. To investigate the effect of increasing bit-rate.
> 5. To restore a bandwidth-limited digital signal using a comparator and observe its limitations.
## MATERIALS 
> 1. Emona Telecoms-Trainer 101 (plus power-pack)
> 2. Dual-channel 20MHz oscilloscope
> 3. Variable DCV, PCM Encoder, PCM Decoder, Tuneable Low-pass Filter, Sequence Generator, VCO, Utilities (Comparator)
> 4. Three oscilloscope leads, assorted patch leads, stereo headphones
## INTRODUCTION
> Bandwidth limiting in digital communication refers to the restriction of the frequency range that a signal can occupy when transmitted through a communication channel. In practical systems, transmission media such as cables, wireless channels, or filters cannot support unlimited bandwidth, so the digital signal must pass through a bandwidth-limited channel. When this happens, the sharp transitions of a digital signal become smoother and distorted due to the loss of high-frequency components. As a result, the received waveform may no longer look like an ideal square wave, and it may suffer from effects such as attenuation, delay, and intersymbol interference (ISI). These distortions can make it difficult for the receiver to correctly interpret the original digital data.

> To recover the original information, signal restoring techniques are used at the receiver. One common method is the use of regenerative repeaters or decision circuits, which reshape and regenerate the distorted digital signal. These circuits detect the incoming signal levels and reconstruct them into clean digital pulses representing binary 1s and 0s. Additionally, filtering and equalization may be applied to compensate for channel distortion. The restoration process ensures that the digital signal regains its proper amplitude, timing, and shape so that the data can be accurately interpreted by the receiving system. 

# PROCEDURES
## PART A: THE EFFECT OF BANDWIDTH LIMITING ON PCM DECODING 
> 1. Gather a set of the equipment listed above.
> 2. Set up the scope per the instructions in Experiment 1.
> 3. Set the scope's Mode control to the DUAL position.
> 4. Set the scope's Channel 1 and Channel 2 Input Coupling controls to the DC position.
> 5. Set the scope's Channel 1 and Channel 2 Vertical Attenuation controls to the 1V/div position.
> 6. Locate the Variable DCV module and set its VDC control to about the middle of its travel.
> 7. Locate the PCM Encoder module and set its Mode switch to the PCM position.
> 8. Connect the set-up where the PCM Encoder module’s PCM DATA output is connected to the PCM Decoder module’s PCM DATA input.

## BLOCK DIAGRAM
<img width="3500" height="1932" alt="image" src="https://github.com/user-attachments/assets/ea0567df-7494-4cf3-ae25-d9f6c6249fc1" />

<img width="3058" height="2294" alt="image" src="https://github.com/user-attachments/assets/575686d7-af9d-4f31-9709-c5700f91a85f" />

> 9. Vary the Variable DCV module’s VDC control left and right.
> 10. Locate the Tuneable Low-pass Filter module and set its Gain control to about the middle of its travel.
> 11. Turn the Tuneable Low-pass Filter module’s Cut-off Frequency Adjust control fully clockwise.
> 12. Modify the set-up so that the low-pass filter is inserted between the PCM Encoder and PCM Decoder.
> 13. Vary the Variable DCV module’s VDC control left and right while slowly turning the Cut-off Frequency Adjust control anti-clockwise.
> 14. Stop turning once the PCM Decoder module’s output becomes corrupted.

## BLOCK DIAGRAM
<img width="3246" height="1545" alt="image" src="https://github.com/user-attachments/assets/744169bf-3f83-41d0-841c-3a30c04acc9f" />

<img width="1379" height="998" alt="image" src="https://github.com/user-attachments/assets/adefb107-3f4a-41b6-9c0a-9322c271ba7f" />



##PART B: THE EFFECT OF THE BANDWIDTH LIMITING ON A DIGITAL SIGNAL'S SAFE
> 15. Completely dismantle the previous set-up.
> 16. Set the scope's Mode control to the CH1 position.
> 17. Set the scope's Trigger Source control to the EXT position.
> 18. Set the scope's Trigger Source Coupling control to the HF REJ position.
> 19. Set the Tuneable Low-pass Filter module's Gain control to about the middle of its travel.
> 20. Turn the Tuneable Low-pass Filter module's Cut-off Frequency Adjust control fully clockwise.
> 21. Locate the Sequence Generator module and set its dip-switches to 00.
> 22. Connect the set-up where the Sequence Generator output passes through the Tuneable Low-pass Filter.
> 23. Set the scope's Timebase control to the 1ms/div position to view about twenty bits of data.
> 24. Set the scope's Mode control to the DUAL position and compare the signals.
> 25. Turn the Cut-off Frequency Adjust control anti-clockwise to narrow the bandwidth and observe the signal shape.

## BLOCK DIAGRAM
<img width="3500" height="1841" alt="image" src="https://github.com/user-attachments/assets/bc5c432f-13b0-48c6-bc3c-0e235214e36a" />

<img width="3315" height="2552" alt="image" src="https://github.com/user-attachments/assets/6597c2a5-419f-4659-a8d4-bbb306e3c51f" />

## INCREASING BIT-RATE
> 26. Turn the Tuneable Low-pass Filter module’s Cut-off Frequency Adjust control fully clockwise.
> 27. Turn the VCO module’s Frequency Adjust control to about a quarter of its travel.
> 28. Set the VCO module’s Range control to the LO position.
> 29. Modify the set-up so that the Sequence Generator module’s clock is provided by the VCO module’s DIGITAL output.
> 30. If the scope’s display is unstable, adjust the VCO frequency slightly until it settles.
> 31. Continue turning the VCO module’s Frequency Adjust control clockwise to increase the transmission bit-rate while observing the scope display.

## BLOCK DIAGRAM
<img width="3500" height="1691" alt="image" src="https://github.com/user-attachments/assets/fcb8cb91-a523-48d8-97ca-58f62f574b53" />



## PART C: RESTORING DIGITAL SIGNALS
> 32. Set the scope’s Timebase control to the 0.5ms/div position.
> 33. Set the Variable DCV module’s Variable DC control to about the middle of its travel.
> 34. Insert the comparator from the Utilities module after the Tuneable Low-pass Filter.
> 35. Compare the original digital signal and the restored digital signal.
> 36. Slowly turn the Variable DCV module’s DC Voltage control fully clockwise and fully anti-clockwise and observe the effect.
> 37. Return the Variable DCV control to about the middle of its travel.
> 38. Slowly narrow the channel’s bandwidth by turning the Cut-off Frequency Adjust control anti-clockwise and observe the effect.
> 39. Turn the Cut-off Frequency Adjust control clockwise and stop when the comparator’s output matches the original digital signal (ignoring phase shift).
> 40. Compare the restored digital signal with the bandwidth-limited digital signal.


## BLOCK DIAGRAM
<img width="3380" height="1649" alt="image" src="https://github.com/user-attachments/assets/d7b8e104-0c9b-47be-960e-c653baa14fc4" />

<img width="3288" height="2501" alt="image" src="https://github.com/user-attachments/assets/45ae122f-45bd-40f5-9332-308f50d6d08b" />


## DATA ANALYSIS
>How a digital waveform is affected when it passes through a channel with a limited bandwidth is demonstrated in the experiment on restoring and limiting digital signal bandwidth. Digital signals ought to have square waveforms with sharp transitions between high and low states. However, the limited bandwidth of a practical communication channel eliminates some of the high-frequency components that cause these sharp edges when the signal is transmitted. The result is a distorted waveform and smoother and slower transitions between binary levels. Degradation of the signal as a result of this distortion may result in errors in detecting the transmitted data. On the oscilloscope, the digital signal appeared rounder and less distinct during the experiment due to the limited bandwidth. Regeneration or shaping circuits were used in a signal restoration procedure to solve this issue. These circuits help restore the original digital waveform by amplifying the signal, reshaping the pulse edges, and correcting the timing.  The digital signal regains its square-wave form following restoration, making it simpler for the receiver to correctly interpret the binary data. Digital communication systems can't function properly over long distances or in noisy channels without this procedure.


## QUESTIONA AND ANSWERS
> 1.  Why does bandwidth limiting of the channel cause the PCM Decoder module to output incorrect voltages as well as the correct one?
> 2.  If this were a communications system transmitting speech, what would these errors sound like when the message is reconstructed?
> 3.  What two things are happening to cause the digital signal to change shape?
> 4.  What other change to your communication system distorts the digital signal in the same way as increasing its bit-rate?
> 5.  Although the restored digital signal is almost identical to the original digital signal, there is a difference. Can you see what it is?
> 6.  Can this difference be ignored? Why?
> 7.  Why do some DC voltages cause the comparator to output the wrong information?
> 8.  Why does the comparator begin to output the wrong information when this control is turned far enough?

>> ANSWERS

> 1. Because bandwidth limiting attenuates higher-frequency harmonics and introduces phase shifts, distorting the digital waveform so the decoder misinterprets logic levels.
> 2. The reconstructed speech would sound noisy, distorted, or contain audible glitches.
> 3. Attenuation of higher-frequency harmonics and phase shifting of frequency components.
> 4. Reducing the channel bandwidth produces the same distortion effect.
> 5. There is a phase shift between the original and restored signals.
> 6. It may be ignored if logic levels are correct, but excessive phase shift can cause timing errors in digital systems.
> 7. Because the threshold voltage does not match the signal’s switching point, causing incorrect logic detection.
> 8. Because excessive distortion prevents the comparator from correctly detecting signal transitions.


## LEARNING SUMMARY
>I observed the effects of bandwidth restrictions on digital communication systems in this experiment. I found out that for digital signals to keep their square shape, they need enough harmonic content. Attenuation and phase shift cause distortion when bandwidth is reduced or bit rate is increased. I also learned that resquaring digital signals with comparators can fix distorted signals, but this method has some drawbacks. Errors are caused by excessive distortion and inadequate threshold settings. In communication systems, this demonstrates the significance of adequate bandwidth and signal conditioning.










 
