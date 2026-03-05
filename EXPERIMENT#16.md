# EXP 16: FREQUENCY SHIFT KEYING (FSK)
## OBJECTIVES
> 1. To generate a Frequency Shift Keying (FSK) signal using a VCO.
> 2. To observe the relationship between a digital signal and its FSK-modulated carrier.
> 3. To demodulate an FSK signal using a tuneable low-pass filter and envelope detector.
> 4. To restore a recovered digital signal using a comparator.
> 5. To understand the concepts of Mark and Space frequencies.
## MATERIALS
> 1. Emona Telecoms-Trainer 101 (plus power-pack)
> 2. Dual-channel 20MHz oscilloscope
> 3. Master Signals, Sequence Generator, VCO, Tuneable Low-pass Filter, Rectifier, Comparator (Utilities), Variable DCV
> 4. Three oscilloscope leads and assorted patch leads
## INTRODUCTION
>Frequency Shift Keying (FSK) is a digital modulation technique in which the frequency of a carrier signal is varied according to the digital input data, while the amplitude and phase remain constant. In FSK, binary information is transmitted by switching the carrier frequency between two or more discrete values. Typically, a binary “1” is represented by a higher frequency called the mark frequency, while a binary “0” is represented by a lower frequency called the space frequency. This method allows digital signals to be transmitted through communication channels by converting them into frequency variations of an analog carrier signal.
>FSK is widely used in digital communication systems because it is more resistant to noise compared to Amplitude Shift Keying (ASK). Since information is carried in the frequency rather than amplitude, small amplitude variations caused by noise do not significantly affect the detection of the signal. For this reason, FSK is commonly used in applications such as radio communication, data transmission over telephone lines, wireless modems, telemetry systems, and RFID technologies.

# PROCEDURES
## PART A: GENERATING AN FSK SIGNAL
> 1. Gather a set of the equipment listed above.
> 2. Set up the scope per the instructions in Experiment 1.
> 3. Set the scope's Trigger Source control to the EXT position.
> 4. Set the scope's Trigger Source Coupling control to the HF REJ position.
> 5. Set the scope's Channel 1 and Channel 2 Input Coupling controls to the DC position.
> 6. Set the VCO Gain control to about half of its travel.
> 7. Set the VCO Frequency Adjust control to about the 9 o’clock position.
> 8. Set the VCO module's Range control to the LO position.
> 9. Set the Sequence Generator dip-switches to 00 (both up).
> 10. Connect the set-up so that:

        • The Sequence Generator SYNC output connects to the Scope EXT trigger.
        • The Sequence Generator OUT connects to the VCO IN.
        • The VCO OUT connects to Scope Channel 2.
> 12. Set the scope’s Timebase control to 0.5ms/div.
> 13. Set the scope’s Mode control to the DUAL position to view both the digital signal and the FSK signal.
> 14. Compare the signals and observe how the carrier frequency shifts according to the digital data.

