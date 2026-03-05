# EXP 20: UNDERSAMPLING IN SDR
## OBJECTIVES
> 1. To generate a bandwidth-limited DSBSC signal.
> 2. To understand the concept of undersampling (band-pass sampling).
> 3. To observe how aliasing can be used for direct down-conversion.
> 4. To recover a baseband message using a Sample-and-Hold and Low-pass Filter.
> 5. To investigate the importance of synchronization in SDR systems.
> 6. To understand how harmonics of the sampling clock can act as a local oscillator.
## MATERIALS
> 1. Emona Telecoms-Trainer 101 (plus power-pack)
> 2. Dual-channel 20MHz oscilloscope
> 3. Master Signals, Multiplier, Sample-and-Hold, Tuneable Low-pass Filter, VCO
> 4. 	Two oscilloscope leads and assorted patch leads
## INTRODUCTION
>Undersampling, also known as bandpass sampling, is a technique used in Software Defined Radio (SDR) to directly sample high-frequency signals at a rate lower than the Nyquist rate of the carrier frequency, while still avoiding aliasing of the signal of interest. Instead of using traditional high-speed analog-to-digital converters (ADCs) to sample the full carrier, undersampling exploits the fact that the signal occupies a narrow bandwidth relative to its center frequency. By carefully selecting the sampling frequency, the high-frequency signal is “folded” down to a lower intermediate frequency or baseband in the digital domain without loss of information, allowing SDRs to process RF signals efficiently with lower-speed ADCs. This technique is particularly useful for reducing hardware complexity and cost in SDR systems while enabling the reception of multiple high-frequency bands. However, accurate undersampling requires precise filtering and knowledge of the signal’s bandwidth and location to prevent overlap with unwanted spectral components. Undersampling is widely applied in modern SDR implementations for communications, radar, and signal intelligence systems, where flexibility and cost-effective high-frequency signal processing are essential.
# PROCEDURES
## PART A: SETTING UP BANDWIDTH LIMITED SIGNAL
> 1. Gather the required equipment.
> 2. Set up the oscilloscope
> 3. Trigger Source → CH1 (or INT)
> 4. Mode → CH1
> 5. Connect the setup
> 6. 2kHz Sine (Message) → Multiplier Y input
> 7. 100kHz Cosine (Carrier) → Multiplier X input
> 8. Adjust the scope’s Timebase to view two cycles of the 2kHz sine wave.
> 9. Set scope Mode to DUAL.
> 10. Set
> 11. Channel 1 Attenuation → 1V/div
> 12. Channel 2 Attenuation → 2V/div
> 13. Observe the DSBSC signal output from the Multiplier.

## BLOCK DIAGRAM
<img width="3500" height="3108" alt="image" src="https://github.com/user-attachments/assets/f0e6bf77-75f4-4457-b24f-2584d90a51ff" />

<img width="3018" height="2309" alt="image" src="https://github.com/user-attachments/assets/65456fe0-8d86-4051-80b2-f9d34efc33d0" />



## PART B: DIRECT DOWM CONVERRION USING UNDERSAMPLING
> 14. Return Scope Channel B scale to 0.5V/div.
> 15. Modify the setup by adding the Sample-and-Hold (S/H) module.
> 16. Trigger the S/H using an 8kHz clock from Master Signals.
> 17. Compare the undersampled DSBSC signal with the original message.
> 18. Modify the setup by connecting the S/H output to the Tuneable Low-pass Filter (LPF).
> 19. Observe the LPF output and compare it with the original 2kHz sine wave.

## OUPTU AND BLOCK DIAGRAM
<img width="3500" height="2479" alt="image" src="https://github.com/user-attachments/assets/50e18d1b-bfd4-416e-b158-784645bcb3d9" />

<img width="3346" height="2504" alt="image" src="https://github.com/user-attachments/assets/d1519b0f-48c2-4334-884a-d2f2334e9e3f" />

<img width="3518" height="2677" alt="image" src="https://github.com/user-attachments/assets/7b2a3858-8ee1-4c71-a310-564d8c3beddc" />



## PART C: SYNCHRONIZATION
> 20. Locate the VCO module and set its Range to LO.
> 21. Set the Frequency Adjust control to mid-position.
> 22. Connect Scope CH1 to the VCO Digital Output.
> 23. Adjust the VCO frequency to 8.333kHz (Period ≈ 120µs).
> 24. Return Scope CH1 to the 2kHz sine output.
> 25. Adjust the timebase to view 2–3 cycles of both original and recovered signals.
> 26. Disconnect the 8kHz clock from Master Signals.
> 27. Use the VCO Digital Output as the new S/H clock source.
> 28. Observe the effect on the recovered message.
> 29. Attempt to correct frequency error by adjusting the VCO Frequency control.

## OUTPUT
<img width="2608" height="1999" alt="image" src="https://github.com/user-attachments/assets/28ae4f7f-95d9-48ae-beef-c11055c5b71d" />

## DATA ANALYSIS
>In the undersampling experiment, a high-frequency carrier signal modulated by a low-frequency message was sampled at a rate lower than its Nyquist frequency, demonstrating the principle of bandpass sampling. The oscilloscope showed that, despite the lower sampling rate, the signal was correctly folded down into the baseband, preserving the original message waveform. The spectrum of the undersampled signal confirmed that aliasing occurred in a controlled manner, allowing the high-frequency information to be captured without distortion. Recovery of the original message after low-pass filtering indicated that the undersampling technique can effectively replace conventional mixing, enabling SDR systems to process high-frequency signals with lower-speed ADCs. Minor deviations in amplitude or phase observed were attributed to timing jitter and slight mismatches between the sampling clock and carrier frequency, highlighting the importance of precise synchronization in practical SDR implementations. Overall, the experiment successfully validated that undersampling can be used to simplify hardware requirements while maintaining accurate signal reconstruction.

## QUESTION AND ANSWERS
> 1. For the given inputs to the Multiplier module, what are the frequencies of the two sinewaves that make up the DSBSC signal?
> 2. What is the bandwidth of the DSBSC signal?
> 3. What is the significance of the signal at the Baseband LPF output?
> 4. Given the sampling frequency is 8.333kHz, which harmonic in the sampling signal demodulates the DSBSC signal?
> 5. Why doesn’t adjusting the VCO solve the instability problem and allow stable recovery?

>> ANSWERS
> 1.  f1 = fc - fm = 100 kHz - 2 kHz = 98 kHz
      f2 = fc + fm = 100 kHz + 2 kHz = 102 kHz
> 2. BW = 102 kHz - 98 kHz = 4 kHz
> 3. It is the recovered message signal. The LPF removes high-frequency aliases generated during sampling, leaving only the baseband component, which matches the original 2kHz sine wave.
> 4. 12 × 8.333 kHz ≈ 100 kHz
> 5. Because the VCO is not phase-locked to the transmitter carrier. Even a small frequency mismatch causes a beat frequency between the carrier and the sampling harmonic, producing amplitude variations (“rolling”) in the recovered signal. Without synchronization (e.g., a Phase-Locked Loop), the two oscillators cannot remain in phase

## SUMMARY OF LEARNINGS
>An 8kHz sampling clock was used to undersample a 100kHz DSBSC signal in this experiment. Without the use of a conventional mixer, the signal was effectively down-converted to baseband by selecting a sampling frequency whose harmonic coincided with the carrier frequency. The original 2kHz message signal was successfully recovered by the Low-pass Filter. This demonstrated that SDR systems can purposefully exploit aliasing, which is typically regarded as undesirable, for direct conversion. However, the experiment also brought to light how crucial synchronization is. In the absence of a phase-locked or shared clock, even minute variations in frequency result in signal instability. This lab clearly demonstrates that modern SDR systems are more dependent on clever sampling strategies and mathematical signal processing than on intricate analog hardware.



