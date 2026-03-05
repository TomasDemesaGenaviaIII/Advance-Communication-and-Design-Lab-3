#EXP 18: QUADRATURE PHASE SHIFT KEYING (QPSK)
## OBKECTIVES
> 1. To generate a Quadrature Phase Shift Keying (QPSK) signal.
> 2. To observe how a serial data stream is split into even and odd bit streams.
> 3. To modulate two orthogonal carriers (I and Q channels) using BPSK.
> 4. To demodulate QPSK using phase discrimination and a product detector
> 5. To understand the bandwidth advantage of QPSK over BPSK.
> 6. To combine two BPSK signals to form a QPSK signal.
## MATERIALS
> 1. Emona Telecoms-Trainer 101 (plus power-pack)
> 2. Dual-channel 20MHz oscilloscope
> 3. Master Signals, Sequence Generator, Divider, Serial-to-Parallel Converter, Multiplier (Product Modulator), Adder, Tuneable Low-pass Filter, Phase Shifter, Comparator (Utilities), Variable DCV
> 4. 	Three oscilloscope leads and assorted patch leads
## INTRODUCTION
>Quadrature Phase Shift Keying (QPSK) is a widely used digital modulation technique in modern communication systems, including satellite, cellular, and Wi-Fi networks. It is a form of phase modulation where the phase of a carrier signal is shifted to represent digital data. Unlike Binary Phase Shift Keying (BPSK), which encodes only one bit per symbol, QPSK encodes two bits per symbol by using four distinct phase states: 0°, 90°, 180°, and 270°, with each phase corresponding to a unique two-bit combination. This allows QPSK to transmit data at twice the rate of BPSK without increasing the required bandwidth. Mathematically, a QPSK signal can be represented using in-phase (I) and quadrature (Q) components, making it efficient for implementation in digital communication systems. QPSK offers advantages such as higher data rates, bandwidth efficiency, and good noise immunity, although it requires more complex demodulation and carrier recovery to avoid phase ambiguity. Its reliability and efficiency make it suitable for applications in digital television broadcasting, cellular networks like GSM and LTE, satellite communications, and Wi-Fi systems.

# PROCEDURES
## PART A: GENERATING A QPSK
> 1. Gather a set of the equipment listed above.
> 2. Set up the scope per the instructions in Experiment 1.
> 3. Set the scope's Trigger Source control to the EXT position.
> 4. Set the scope's Trigger Source Coupling control to the HF REJ position.
> 5. Set the scope's Channel 1 and Channel 2 Input Coupling controls to the DC position.
> 6. Set the scope's Timebase control to the 0.5ms/div position.
> 7. Locate the Divider module and set it to divide by 2 (left switch UP, right switch DOWN).
> 8. Connect the set-up as shown in the lab manual (Serial-to-Parallel configuration).

## OUTPUT
<img width="3500" height="2577" alt="image" src="https://github.com/user-attachments/assets/da8c6952-5f5f-4113-a7d2-7b2c73e3e204" />



## BLOCK DIAGRAM
<img width="2942" height="2227" alt="image" src="https://github.com/user-attachments/assets/f8486ef7-ebcc-4e3d-8e96-5014a1341151" />

<img width="3299" height="2542" alt="image" src="https://github.com/user-attachments/assets/cb1603bb-5fb3-4d7f-8d6b-419277ab86e3" />



> 9. Set the scope’s Mode control to the DUAL position to view the even and odd bit streams.
> 10. Compare the signals (Even bits on Ch1, Odd bits on Ch2).
> 11. Modify the set-up by connecting the Multiplier modules for I and Q modulation.

## BLOCK DIAGRAM
<img width="3500" height="2577" alt="image" src="https://github.com/user-attachments/assets/135bae8e-79cf-47a9-8f3e-41ad1026a4b6" />

<img width="3299" height="2542" alt="image" src="https://github.com/user-attachments/assets/077581c8-de2c-4cab-83c2-15a0f4a5ce56" />



> 12. Compare the even bits with the Multiplier output (PSK_I).
> 13. Set the scope’s Timebase to 0.2ms/div.
> 14. Activate the scope’s Sweep Magnifier.
> 15. Use the Horizontal Position control to observe a transition in the data sequence.
> 16. Examine how the carrier changes at the transition.
> 17. Deactivate the Sweep Magnifier.
> 18. Move the scope connections to observe the Q-channel output (PSK_Q).

## BLOCK DIAGRAM
<img width="3494" height="3500" alt="image" src="https://github.com/user-attachments/assets/460e6097-4922-48ef-b5d9-6c557dff5b80" />

<img width="3194" height="2399" alt="image" src="https://github.com/user-attachments/assets/5fddbed1-105b-4b54-a851-c972b34945d0" />



> 19. Activate the Sweep Magnifier and observe a transition.
> 20. Examine how the quadrature carrier changes.
> 21. Deactivate the Sweep Magnifier and return the timebase to 0.5ms/div.
> 22. Modify the set-up by adding the Adder module.

## BLOCK DIAGRAM
<img width="3500" height="3155" alt="image" src="https://github.com/user-attachments/assets/34061aac-e71c-413b-8751-7034538ae487" />

<img width="3431" height="2579" alt="image" src="https://github.com/user-attachments/assets/76d90445-a1f8-49ad-88ea-c54a7a21527b" />



> 23. Turn the Adder’s g control fully anti-clockwise.
> 24. Adjust the g control to obtain a 4V p-p output.
> 25. Disconnect the patch lead to the Adder’s B input.
> 26. Adjust the G control to obtain a 4V p-p output.
> 27. Reconnect the patch lead to the Adder’s B input.
> 28. Set the scope timebase to 0.2ms/div.
> 29. Activate the Sweep Magnifier.
> 30. Examine the complete QPSK signal from beginning to end.

## PART B: PHASE DISCRIMINATION (DEMODULATION
> 31. Deactivate the Sweep Magnifier and return the timebase to 1ms/div.
> 32. Locate the Tuneable Low-pass Filter and turn its Cut-off Frequency Adjust control fully clockwise.
> 33. Set the LPF Gain control to the middle of its travel.
> 34. Locate the Phase Shifter and set its Phase Change control to 0°.
> 35. Modify the set-up by adding the product detector configuration.
> 36. Compare the even data bits with the LPF output.

## BLOCK DIAGRAM
<img width="3500" height="2761" alt="image" src="https://github.com/user-attachments/assets/afbfdbca-e5a5-4674-9cd5-b53d72e7dabe" />



> 37. Vary the Phase Adjust control until a bipolar signal is observed.
> 38. Set the Phase Shifter to 180° and repeat the observation.
> 39. Modify the set-up by adding the Comparator module.
> 40. Set the Phase Shifter to 0°.

## BLOCK DIAGRAM
<img width="3500" height="1891" alt="image" src="https://github.com/user-attachments/assets/6fa178a5-a792-451d-8ac5-e4be7699899c" />



> 41. Compare the even data bits with the recovered data.
> 42. Adjust the Phase Adjust control until the even bits are recovered.
> 43. Move Scope Ch1 to observe the odd bits.
> 44. Compare the odd bits with the recovered data.
> 45. Set the Phase Shifter to 180°.
> 46. Adjust the Phase Adjust control until the odd bits are recovered.
> 47. 



# DATA ANALYSIS
>In the QPSK experiment, the serial input data stream was first split into even and odd bits, which were then used to modulate two orthogonal carriers, the in-phase (I) and quadrature (Q) components, using BPSK modulation. Observation of the QPSK waveform on the oscilloscope revealed that the combined signal exhibited four distinct phase states, corresponding to the four possible bit pairs (00, 01, 10, 11). This confirms that the system successfully encodes two bits per symbol, effectively doubling the data rate compared to standard BPSK for the same bandwidth. The amplitude of the signal remained relatively constant, demonstrating the phase modulation nature of QPSK, where information is conveyed through phase shifts rather than amplitude changes. During demodulation, the I and Q signals were recovered using a product detector and low-pass filtering, and the output matched the original bit stream with minimal error, indicating accurate transmission and proper alignment of carrier phase. Any slight deviations in waveform observed were attributed to phase jitter or minor synchronization errors, which are typical in practical setups. Overall, the experiment validated the bandwidth efficiency and reliability of QPSK, demonstrating its advantage in digital communication systems where high data rates are required without increasing the channel bandwidth.


## QUESTIONS AND ANSWERS
> 1. What is the relationship between the bit rate of the two digital signals and the Sequence Generator output?
> 2. What feature of the Multiplier output suggests that it is a BPSK signal?
> 3. What type of signal is present on the Multiplier output?
> 4. What type of signal is present on the Adder output?
> 5. Why is there only one sinewave when the QPSK signal is made up of two BPSK signals?
> 6. What causes the 3- and 4-level signals out of the LPF during phase adjustments?
> 7. hat is the phase relationship required to recover the even bits?
> 8. What is the phase relationship required to recover the odd bits?
> 9. hy is this demodulator only half of a full QPSK receiver?

>> ANSWERS

> 1. The presence of 180° phase reversals in the carrier whenever the digital data changes logic level.
> 2. A BPSK (Binary Phase Shift Keying) signal.
> 3. Because adding two sinewaves of the same frequency results in a single sin
> 4. ewave whose amplitude and phase are determined by the vector sum of the two components.
> 5. A QPSK (Quadrature Phase Shift Keying) signal.
> 6. This occurs when the local carrier is not properly aligned, causing partial detection of both I and Q channels simultaneously (cross-talk).
> 7. The local carrier must be in-phase (0° or 180°) with the I-channel carrier.
> 8.  The local carrier must be shifted by 90° relative to the I-channel carrier to align with the Q-channel carrier.
> 9.  A full QPSK receiver requires two parallel product detectors to simultaneously recover both I and Q channels, whereas this setup recovers only one channel at a time.


##SUMMARY OF LEARNINGS
>By modulating two parallel digital data streams onto orthogonal carriers and splitting a serial digital data stream, this experiment produced a QPSK signal. By combining the two BPSK signals into a single QPSK waveform, improved bandwidth efficiency was demonstrated. Using a product detector and a Low-pass filter, phase discrimination was used to demonstrate. In order to accurately recover either the even bit stream or the odd bit stream, carrier phase alignment was essential. The significance of synchronization in digital communication systems was also brought to light by this experiment, which demonstrated the fundamentals of quadrature modulation.

