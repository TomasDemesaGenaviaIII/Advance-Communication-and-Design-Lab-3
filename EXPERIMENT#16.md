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

## BLOCK DIAGRAM
<img width="3500" height="2485" alt="image" src="https://github.com/user-attachments/assets/25a64ba3-7b14-4333-9e61-5d400bfab81d" />

<img width="3129" height="2367" alt="image" src="https://github.com/user-attachments/assets/ac895aa1-0721-4469-b36d-93124783ba02" />



## PART B: DEMODULATING AND FSK SIGNAL
> 14. Turn the VCO’s Frequency Adjust control to approximately the 2 o’clock position.
> 15. Turn the Tuneable Low-pass Filter module’s Cut-off Frequency Adjust control fully clockwise.
> 16. Turn the Tuneable Low-pass Filter module’s Gain control fully clockwise.
> 17. Modify the set-up by routing the VCO OUT through the Tuneable Low-pass Filter.

## BLOCK DIAGRAM
<img width="3500" height="1650" alt="image" src="https://github.com/user-attachments/assets/8b663e4f-6e1c-488b-a45a-baba1ce29f41" />

<img width="3551" height="2717" alt="image" src="https://github.com/user-attachments/assets/9590311f-bf09-4c75-a7d3-483b20c20237" />



> 18. Slowly turn the LPF Cut-off Frequency Adjust control counter-clockwise until the higher frequency component of the FSK signal is suppressed.
> 19. Compare the original digital signal with the filter’s output.
> 20. Modify the set-up by adding the Rectifier after the filter to form an envelope detector.
> 21. Connect Scope Channel 2 to the envelope detector output.
> 22. Compare the original digital signal with the recovered signal.

## OUTPUT
<img width="2869" height="2265" alt="image" src="https://github.com/user-attachments/assets/5709e245-e170-4384-a3cb-d659fed36dca" />



## PART C: RESTORING THE RECOVERED DIGITAL SIGNAL USING A COMPARATOR
> 23. Modify the set-up by connecting the envelope detector output to the Comparator IN.
> 24. Observe and note the amplitude of the filtered signal (varies between 0V and a maximum value).
> 25. Set the Variable DCV module’s output to approximately half of the maximum amplitude noted in step 24 and connect it to the Comparator REF input.
> 26. Compare the original digital signal with the recovered digital signal from the Comparator output.

## BLOCK DIAGRAM
<img width="3500" height="1450" alt="image" src="https://github.com/user-attachments/assets/9bb5ee04-ef5f-4c55-bb00-e7b226534a99" />

<img width="2550" height="1913" alt="image" src="https://github.com/user-attachments/assets/2628ad81-f7c9-4b74-a37e-e74318dc35e7" />



## DATA ANALYSIS
>The Frequency Shift Keying (FSK) experiment demonstrates a digital modulation technique where the frequency of the carrier signal changes according to the binary input data while the amplitude remains constant. In binary FSK, two different carrier frequencies are used to represent the digital states: the mark frequency for binary “1” and the space frequency for binary “0.”
>During the experiment, the digital input signal was used to control the carrier frequency of the modulator. When the input bit was 1, the circuit generated a higher frequency signal, and when the input bit was 0, a lower frequency signal was produced. On the oscilloscope, this resulted in a waveform where the frequency alternated depending on the digital data sequence. The modulated FSK signal was then passed through a demodulator circuit, which detected the frequency changes and reconstructed the original digital signal. This process demonstrates how digital information can be transmitted through communication channels by encoding data into frequency variations of a carrier wave.

## QUESTION AND ANSWER
> 1. What’s the name for the VCO output frequency that corresponds with logic-1s in the digital data?
> 2. What’s the name for the VCO output frequency that corresponds with logic-0s in the digital data?
> 3. Based on your observations of the FSK signal, which of the two is the higher frequency?
> 4. Which of the FSK signal’s two sinewaves is the filter picking out?
> 5. What does the filtered FSK signal look like?
> 6.  What can be used to “clean-up” the recovered digital signal?
> 7. How does the comparator turn the slow rising voltages of the recovered digital signal into sharp transitions?

>> ANSWERS

> 1. The Mark frequency.
> 2. The Space frequency.
> 3. The Mark frequency is typically the higher frequency. On the oscilloscope, the waveform corresponding to logic-1 appears with cycles that are closer together, indicating a higher frequency.
> 4. The filter picks out the Space frequency (the lower frequency) by attenuating the higher frequency component.
> 5. It appears as bursts of sinewaves during logic-0 intervals, separated by near-zero voltage during logic-1 intervals where the higher frequency has been filtered out.
> 6.  A comparator circuit (or Schmitt trigger).
> 7.  The comparator compares the input signal to a fixed reference voltage. When the input exceeds the reference, the output switches to its maximum level; when it falls below the reference, the output switches to minimum level. This produces sharp digital transitions

## SUMMARY OF LEARNINGS
>A digital sequence was used to control a Voltage Controlled Oscillator (VCO) in this experiment to generate an FSK signal that caused the carrier frequency to shift between Mark and Space frequencies. The oscilloscope revealed a connection between frequency variation and digital data. By removing one frequency component and employing envelope detection, the FSK signal was demodulated. The comparator successfully restored the sharp edges necessary for digital processing, despite the recovered waveform's gradual transitions. This experiment demonstrated that digital data can be reliably reconstructed at the receiver and transmitted using frequency modulation.
>This experiment provided a clearer understanding of how digital data can be transmitted using frequency variations in a carrier signal. Observing the FSK waveform helped demonstrate how binary information is represented by two distinct frequencies and how these frequencies can be detected and converted back into digital data at the receiver. It also highlighted the advantages of FSK, particularly its resistance to noise and interference compared to other modulation methods such as ASK. Through this activity, the importance of modulation techniques in digital communication systems became more evident, helping develop a deeper understanding of how modern communication systems transmit data efficiently and reliably.
