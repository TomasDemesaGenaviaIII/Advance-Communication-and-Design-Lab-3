# EXP 19: DIRECT SEQUENCE SPREAD SPECTRUM MODULATION AND DEMODULATION
## OBJECTIVES
> 1. To generate a Direct Sequence Spread Spectrum (DSSS) signal.
> 2. To understand how a Pseudo-Noise (PN) sequence spreads a message signal.
> 3. To observe the similarity between DSSS and DSBSC modulation.
> 4. To recover a DSSS signal using a synchronized product detector.
> 5. To investigate the effect of incorrect PN synchronization.
> 6. To examine the interference rejection capability of DSSS.
## MATERIALS
> 1. Emona Telecoms-Trainer 101 (plus power-pack)
> 2. Dual-channel 20MHz oscilloscope
> 3. Master Signals, Sequence Generator, Multiplier (Product Modulator), Adder, Tuneable Low-pass Filter, Speech Module, VCO
> 4. Two oscilloscope leads and assorted patch leads
## INTRODUCTION
>Direct Sequence Spread Spectrum (DSSS) is a digital modulation technique used to enhance the reliability and security of wireless communication. In DSSS, the original data signal is multiplied by a high-rate pseudo-random noise (PN) sequence, also called a spreading code, which increases the signal’s bandwidth far beyond that of the original data. This process spreads the signal energy over a wide frequency range, making it less susceptible to interference, jamming, and eavesdropping. At the receiver, the signal is demodulated by correlating it with the same PN sequence, which effectively despreads the signal back to its original bandwidth while reducing the effects of noise and interference. DSSS is widely used in systems such as GPS, CDMA cellular networks, and secure military communications, where robustness, privacy, and resistance to multipath fading are critical. Understanding DSSS modulation and demodulation helps engineers design communication systems that can operate reliably in noisy and contested frequency environments.
# PROCEDURES
## PART A: GENERATINF A DSSS SIGNAL USING A SIMPLE MESSAGE
> 1. Gather the required equipment.
> 2. Set up the oscilloscope:
> 3. Trigger Source → CH1
> 4. Mode → CH1
> 5. Set the scope’s Trigger Source Coupling to HF REJ.
> 6. Set the Sequence Generator dip-switches to 00.
> 7. Connect the setup:
> 8. kHz Sine from Master Signals → Multiplier Input A
> 9. 100kHz Clock to Sequence Generator
> 10. PN output → Multiplier Input B
> 11. Adjust the scope’s Timebase to view two cycles of the 2kHz sine wave.
> 12. Set the scope to DUAL mode to observe both the message and DSSS signal.
> 13. Adjust vertical sensitivity for clear display.
> 14. Observe and sketch both waveforms.
> 15. Compare the message waveform with the DSSS signal envelope.

## BLOCK DIAGRAM
<img width="3369" height="3499" alt="image" src="https://github.com/user-attachments/assets/817292c1-9a64-4c08-a944-60e5c6efd51b" />

<img width="3056" height="2333" alt="image" src="https://github.com/user-attachments/assets/d322b433-dacd-474f-953b-16fb70abe9f0" />



## PART B: GENERATING A DSSS SIGNAL USING SPEACH
> 16. Disconnect the 2kHz sine wave input.
> 17. Connect the Speech Module output to the Multiplier input.
> 18. Set the scope’s Timebase to 2ms/div.
> 19. Speak or sing into the Speech module microphone.
> 20. Observe the spread-spectrum waveform.

## OUTPUT
<img width="3489" height="2700" alt="image" src="https://github.com/user-attachments/assets/bd50cff4-efa8-4f98-a816-309df8627130" />



## PART C: RECOVERING THE MESSAGE  USING A PRODUCT DETECTOR
> 21. Connect the DSSS output to a second Multiplier (Product Detector).
> 22. “Steal” the same PN sequence from the transmitter and connect it to the second Multiplie
> 23. Connect the Multiplier output to the Tuneable Low-pass Filter.

## BLOCK DIAGRAM
<img width="3500" height="2107" alt="image" src="https://github.com/user-attachments/assets/09b959b1-2425-4d00-9d95-f026c2835d95" />

<img width="3500" height="2149" alt="image" src="https://github.com/user-attachments/assets/5c8ed5c9-23ff-447b-a1ce-64aa648b75b3" />



> 24. Adjust the LPF cut-off frequency and gain.
> 25. Observe the recovered signal on the oscilloscope.
> 26. Replace the receiver PN sequence with a different sequence.
> 27. Observe the LPF output again.

## OUTPUT
<img width="3042" height="2309" alt="image" src="https://github.com/user-attachments/assets/f403a64f-cf72-4189-baa9-11e4c93accf5" />



## PART D: DSSS AND DELIBERATE INTERFERENCE 
> 28. Add a VCO output to the DSSS signal using an Adder module.
> 29. Adjust the VCO frequency to act as a narrowband jammer.
> 30. Increase the jammer amplitude.
> 31. Observe the combined signal.
> 32. Pass the composite signal through the product detector and LPF.
> 33. Observe the recovered message.
> 34. Vary the jammer frequency and amplitude.
> 35. Examine the effect on the recovered signal.

## BLOCK DIAGRAM
<img width="3500" height="1799" alt="image" src="https://github.com/user-attachments/assets/c38b8080-49f5-406c-83a1-7ee696bc7926" />

<img width="3398" height="2564" alt="image" src="https://github.com/user-attachments/assets/972ba2d2-63ec-4254-892d-88cea4c8ade7" />

<img width="3242" height="2432" alt="image" src="https://github.com/user-attachments/assets/fd0bdd81-ffbd-462f-98b5-dff0ea840bfa" />



## DATA ANALYSIS
>In the DSSS experiment, the original binary data stream was first combined with a high-rate pseudo-random noise (PN) sequence, resulting in a spread signal with many chips per data bit. Observation of the transmitted waveform on the oscilloscope showed that the signal occupied a significantly wider bandwidth than the original data, confirming the spreading effect. During demodulation, the received signal was multiplied by the same PN sequence used in transmission, which successfully despread the signal and recovered the original data bits with minimal errors. The correlation between the transmitted and received signals demonstrated the robustness of DSSS against noise and interference, as random disturbances appeared less significant after despreading. Minor deviations in the recovered data were attributed to timing mismatches or imperfect synchronization between the transmitter and receiver PN sequences. Overall, the experiment validated that DSSS can enhance signal security, interference resistance, and reliable data recovery, making it an effective technique for modern digital communication systems.

## QUESTIONS ANG ANSWERS
> 1. What feature of the Multiplier output suggests that it is basically a DSBSC signal?
> 2. Why is the DSSS signal large on the oscilloscope when it is supposed to be small and noise-like?
> 3. Why isn’t there any output from the DSSS modulator when you are not speaking?
> 4. What does the signal out of the Low-pass Filter look like when the correct PN sequence is used?
> 5. Why does using the wrong PN sequence produce noise at the output?
> 6. Why doesn’t the jamming signal prevent recovery of the message?

>> ANSWERS

> 1. The output shows phase reversals corresponding to the PN sequence transitions. The signal’s envelope follows the message waveform, which is characteristic of DSBSC modulation.
> 2. In the lab, the signal is observed directly in the time domain before transmission losses. In real communication systems, the signal power is spread across a wide bandwidth, reducing its power spectral density and making it appear noise-like.
> 3. The Multiplier performs mathematical multiplication:
> 4. It resembles the original message (2kHz sine or speech), possibly with slight attenuation or filtering effects.
> 5. DSSS relies on correlation. Using a mismatched PN sequence does not despread the signal; instead, it spreads it further. The Low-pass Filter then sees only random high-frequency components, resulting in noise.
> 6. When multiplied by the correct PN sequence, the DSSS signal is despread back to its narrow bandwidth. The jammer, however, is spread across a wide bandwidth by this multiplication. The Low-pass Filter passes the narrowband message while rejecting the spread jammer, demonstrating processing gain.


## SUMMARY OF LEARNINGS
>By multiplying a message signal with a high-frequency pseudo-noise sequence, this experiment produced a DSSS signal. The process of spreading the signal's energy across a large bandwidth gave it the appearance of noise and made it difficult to detect. A synchronized product detector with an identical PN sequence was required for message recovery. The original message was successfully reconstructed if synchronization was correct. The output appeared to be noise when it was incorrect. Additionally, the experiment demonstrated that DSSS is highly resistant to interference. The despreading process effectively suppressed the jammer while recovering the message, even with a high-amplitude jamming signal present. In today's wireless communication systems, spread-spectrum techniques provide security, rejection of interference, and robustness. This lab demonstrated this clearly.
