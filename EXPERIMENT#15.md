# EXP 15: AMPLITUDE SHIFT KEYING (ASK)
## OBJECTIVES
> 1. To generate an Amplitude Shift Keying (ASK) signal.
> 2. To observe the relationship between a digital signal and its ASK-modulated carrier.
> 3. To demodulate an ASK signal using an envelope detector.
> 4. To restore a recovered digital signal using a comparator.
> 5. To understand the principles of On-Off Keying (OOK).

## MATERIALS
> 1. 	Emona Telecoms-Trainer 101 (plus power-pack)
> 2. 	Dual-channel 20MHz oscilloscope
> 3. 	Master Signals, Sequence Generator, Dual Analog Switch, VCO, Rectifier, Tuneable Low-pass Filter, Comparator (Utilities), Variable DCV
> 4. 	Three oscilloscope leads and assorted patch leads

## INTRODUCTION
>Amplitude Shift Keying (ASK) is a digital modulation technique in which the amplitude of a carrier signal is varied in accordance with the digital data being transmitted, while the frequency and phase remain constant. In ASK, binary data (0s and 1s) are represented by different amplitude levels of a sinusoidal carrier wave. Typically, a binary “1” is transmitted using a carrier signal with a specific amplitude, while a binary “0” is represented by either a lower amplitude or the absence of the carrier signal. Because of this simple method of encoding data, ASK is considered one of the most basic forms of digital modulation used in communication systems.
>In an ASK system, the digital input signal is combined with a carrier wave using a modulator. When the input bit is 1, the carrier is transmitted at its full amplitude, and when the input bit is 0, the amplitude is reduced or completely removed. At the receiver, a demodulator or envelope detector is used to recover the original digital data from the modulated signal. The demodulator detects the variations in amplitude and converts them back into binary form. However, ASK is sensitive to noise and interference because noise can also affect the amplitude of the signal, which may lead to errors in data detection.

# PROCEDURES
## PART A: GENERATING AN ASK SIGNAL
> 1. Gather a set of the equipment listed above.
> 2. Set up the scope per the instructions in Experiment 1.
> 3. Set the scope's Trigger Source control to the EXT position.
> 4. Set the scope's Trigger Source Coupling control to the HF REJ position.
> 5. Set the scope's Channel 1 and Channel 2 Input Coupling controls to the DC position.
> 6. Set the scope's Timebase control to the 1ms/div position.
> 7. Connect the set-up where the Master Signals module’s 2kHz Digital output clocks the Sequence Generator and the 2kHz Sine output is connected to the Dual Analog Switch module.

## BLOCK DIAGRAM
<img width="3500" height="2398" alt="image" src="https://github.com/user-attachments/assets/17677d02-8da7-4e2b-8eed-4a551abb5ac6" />

<img width="3385" height="2573" alt="image" src="https://github.com/user-attachments/assets/01cf6f6c-3498-4290-86d0-0730651b97fb" />


> 8. Set the scope's Mode control to the DUAL position to view the Sequence Generator output and the ASK signal from the Dual Analog Switch module.
> 9. Compare the signals.
> 10. Locate the VCO module and set its Frequency Adjust control to about the middle of its travel.
> 11. Set the VCO module's Range control to the HI position.
> 12. Modify the set-up by replacing the 2kHz sine carrier with the VCO’s high-frequency carrier (approximately 100kHz).
> 13. Compare the signals.
> 14. Use the scope's Channel 1 Vertical Position control to overlay the digital signal with the ASK signal’s envelopes and compare them.

## BLOCK DIAGRAM
<img width="3500" height="1883" alt="image" src="https://github.com/user-attachments/assets/1bbf2839-4f61-4cce-a607-d0289db5351a" />

<img width="2495" height="1914" alt="image" src="https://github.com/user-attachments/assets/eb557683-94d8-432b-aff5-41d55c803245" />



## PART B: DEMODULATING AN ASK SIGNAL USING THE ENVELOPE DETECTOR
> 15. Locate the Tuneable Low-pass Filter module and turn its Gain control fully clockwise.
> 16. Turn the Tuneable Low-pass Filter module's Cut-off Frequency Adjust control fully clockwise.
> 17. Modify the set-up by adding the Rectifier followed by the Low-pass Filter to form an envelope detector.
> 18. Compare the original digital signal with the recovered digital signal.

## BLOCK DIAGRAM
<img width="3500" height="1899" alt="image" src="https://github.com/user-attachments/assets/22e10dc2-b859-45e1-b720-d962323f8723" />

<img width="2990" height="2318" alt="image" src="https://github.com/user-attachments/assets/4156d99b-f07d-4698-87a2-3a6e0cae1616" />



## PART C: RESTORING THE RECOVERED DIGITAL SIGNAL USING A COMPARATOR
> 19. Modify the set-up by connecting the filter output to the Comparator module.
> 20. Set the Variable DCV module's Variable DC control to about the middle of its travel.
> 21. Compare the signals. If they are not the same, vary the Variable DCV module's Variable DC control until they match.

## BLOCK DIAGRAM
<img width="3500" height="1683" alt="image" src="https://github.com/user-attachments/assets/24f6d283-2a52-460a-9526-f82e6bf0399d" />

<img width="3091" height="2318" alt="image" src="https://github.com/user-attachments/assets/f3e2b16e-6661-477f-a83f-de989ae6749e" />



## DATA ANALYSIS
>The experiment on Amplitude Shift Keying (ASK) demonstrates how digital data can be transmitted by varying the amplitude of a carrier signal. In ASK modulation, the carrier signal maintains a constant frequency and phase, but its amplitude changes depending on the binary input data. Typically, when the input bit is 1, the carrier signal is transmitted with full amplitude, while for a 0, the carrier amplitude is reduced or removed completely. This technique is also known as On-Off Keying (OOK) in its simplest form.

>During the experiment, the digital input signal and the carrier signal were combined in the modulator to produce an ASK waveform. The resulting signal consisted of bursts of the carrier corresponding to the binary data sequence. When observed on the oscilloscope, the amplitude of the carrier clearly followed the pattern of the digital input signal. At the receiver side, the modulated signal was passed through a demodulation process, typically using an envelope detector or comparator, to recover the original digital signal. This process illustrates how digital information can be transmitted over analog communication channels using modulation techniques. However, it was also observed that ASK is sensitive to noise and interference because any disturbance affecting the signal amplitude can lead to incorrect detection of the transmitted data

## QUESTION AND ANSWERS
> 1. What is the relationship between the digital signal and the presence of the carrier in the ASK signal?
> 2. What is the ASK signal’s voltage when the digital signal is logic-0?
> 3. What feature of the ASK signal suggests that it’s an AM signal?
> 4. Why is the recovered digital signal not a perfect copy of the original?
> 5. What can be used to “clean-up” the recovered digital signal?
> 6. How does the comparator turn the slow rising voltages of the recovered digital signal into sharp transitions?

>> ANSWWRS

> 1. The carrier is transmitted when the digital signal is logic high (1) and is suppressed when the digital signal is logic low (0).
> 2. Approximately 0V (zero amplitude).
> 3. The amplitude of the carrier wave changes according to the digital signal; the envelope of the carrier follows the digital data pattern.
> 4. The low-pass filter cannot pass all high-frequency components of the square wave, resulting in rounded edges and slight distortion.
> 5. A comparator circuit.
> 6. The comparator compares the signal to a reference threshold. If the input exceeds the threshold, it outputs a maximum voltage; if it is below, it outputs minimum voltage. This clipping action produces sharp transitions and restores the square wave shape.

## SUMMARY OF LEARNINGS
>A high-frequency carrier was gated with a digital data stream to produce an ASK signal in this experiment. The logic 1 and logic 0 were represented, respectively, by the carrier's presence or absence. After that, a rectifier and low-pass filter envelope detector was used to demodulate the ASK signal. The comparator was able to successfully restore the digital signal by serving as a decision threshold device, despite the fact that the limited filtering caused distortion in the recovered signal. This experiment demonstrated the robustness of digital communication systems by demonstrating how digital signals can be reliably reconstructed over analog channels.
