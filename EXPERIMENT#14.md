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
