# [Experiment Report] OFDM and SC-FDE System Implementation and Simulation Performance Analysis

1. Experimental Objective
1.1 Master the working principles of OFDM and SC-FDE, as well as their corresponding system configurations, and be able to analyze and summarize the performance and advantages and disadvantages of both systems;
1.2 Understand the structure of CP-OFDM systems and implement codes, and complete the simulation code for CP-SCFDE, ZP-OFDM, and ZP-SCFDE based on the CP-OFDM simulation code;
1.3 Analyze the performance of the above four schemes and provide a complexity explanation for ZF-OFDM and ZP-SCFDE.

II. Experimental Principles
2.1 Working principles of OFDM and SC-FDE systems
OFDM technology is a multicarrier modulation technique with partial spectrum overlap. Its main principle is: after serial-to-parallel conversion, the channel is divided into many orthogonal subchannels, and narrowband modulation and transmission are performed on each subchannel. This reduces inter-subchannel interference and improves spectral efficiency. The signal bandwidth on each subchannel is less than the channel's correlation bandwidth, so the frequency selective fading on each subchannel is flat, greatly eliminating symbol inter-symbol interference. Additionally, at the transmitter, a cyclic prefix (CP/ZP) needs to be inserted before each transmission block to avoid interference between the previous transmission block and the current one. At the receiver, after removing the cyclic prefix, the received block is the result of sending signal and channel impulse response circular convolution. Finally, due to the use of IFFT and FFT methods, the application complexity of OFDM is greatly reduced.
SC-FDE technology is a promising anti-interference method in broadband wireless transmission. It changes the time domain equalization structure at the receiving end from traditional single carrier transmission to frequency domain equalization. SC-FDE sends high-rate single carrier signals after modulation, and by adding a cyclic prefix (CP/ZP), it avoids interference from the previous transmission block to the current one. At the receiving end, FFT and IFFT transformations achieve frequency domain equalization, which is essentially the frequency domain analysis of the received signal.
1. The OFDM system, during transmission, maps N digit signals onto N subcarriers using an IFFT and then sends them in the time domain. This effectively modulates these N digital symbols onto N subcarriers, constituting multi-carrier transmission. In contrast, SCFDE does not perform an IFFT; instead, it directly adds a cyclic prefix (CP/ZP) before sending, thus sharing little with traditional digital communication in terms of carrier number. Therefore, it is considered single-carrier transmission.
2.2 System Block Diagrams of OFDM and SC-FDE
2.2.1 System Block Diagram of CP-SCFDE
2.2.2 System Block Diagram of ZP-OFDM
2.2.3 System Block Diagram of ZP-SCFDE
2.3 Performance Characteristics and Comparative Analysis of OFDM and SC-FDE Systems
The most notable advantage of the OFDM system is its improved frequency band utilization efficiency. Additionally, by transforming high-speed data streams into serial-to-parallel format, the duration of each subcarrier's data symbol is relatively increased, reducing the impact of channel frequency selective fading. Furthermore, the use of a cyclic prefix eliminates inter-block interference and facilitates channel equalization. However, this system requires strict orthogonality between carriers, and both frequency deviation and phase noise can degrade the orthogonality among subcarriers, affecting system performance. Additionally, the OFDM system has a high peak-to-average power ratio, necessitating a wider linear range for the transmitter's power amplifier, which reduces the power efficiency of the radio frequency power amplifier.
SC-FDE shares similar performance with OFDM and effectively combines the advantages of OFDM technology with those of conventional single-carrier transmission, addressing the shortcomings of OFDM. Its main features include: firstly, due to the use of ordinary single-carrier modulation methods, it reduces the peak-to-average power ratio and sensitivity to carrier frequency offset and phase noise compared to the OFDM system, allowing more relaxed constraints on receiver analog components. Secondly, it achieves performance similar to that of the OFDM system even under long channel delay spread conditions. Its computational complexity is comparable to that of OFDM, significantly lower than that of single-carrier time-domain equalizer systems.
III. Simulation Code
See the CPSCFDE.m, ZPOFDEM.m, and ZPSCFDE.m code in the attachment.
IV. Experimental Results and Analysis
4.1 Experimental simulation results
4.1.1 Simulation results of CP-OFDM
4.1.2 Simulation results of CP-SCFDE
\t  
4.1.3 Simulation results of ZP-OFDM
4.1.4 Simulation Results of ZP-SCFDE
2. Error Rate Comparison
The simulation results of the experiment show that when the signal-to-noise ratio is low, the bit error rate (BER) of CP-SCFDE is higher than that of CP-OFDM and ZP-OFDM. Conversely, the BER of CP-OFDM and ZP-OFDM are comparable. When the signal-to-noise ratio is high, the BER decreases in order: CP-OFDM, ZP-OFDM, CP-SCFDE. However, overall, for the same equalization method, the BER of ZP-SCFDE modulation is the lowest.
3. Complexity Analysis
From the perspective of simulation time execution (under conditions of equal subcarrier numbers, cyclic prefixs, symbol lengths, and frame symbol counts), the time complexity of ZP-OFDM is slightly higher than that of ZP-SCFD. This result is also reasonable from the perspective of their system block diagrams, as the ZP-SCFDE system lacks an IFFT/FFT processing module compared to the ZP-OFDM system. Therefore, in this regard, the complexity may be lower.
\tEnd

## Images

![[Experimental Report] OFDM and SC-FDE System Implementation and Simulation Performance Analysis](01.jpg)
![[Experimental Report] OFDM and SC-FDE System Implementation and Simulation Performance Analysis](02.jpg)
![[Experimental Report] OFDM and SC-FDE System Implementation and Simulation Performance Analysis](03.jpg)
![[Experimental Report] OFDM and SC-FDE System Implementation and Simulation Performance Analysis](04.jpg)
![[Experimental Report] OFDM and SC-FDE System Implementation and Simulation Performance Analysis](05.jpg)
![[Experimental Report] OFDM and SC-FDE System Implementation and Simulation Performance Analysis](06.jpg)
![[Experimental Report] OFDM and SC-FDE System Implementation and Simulation Performance Analysis](07.jpg)
![[Experimental Report] OFDM and SC-FDE System Implementation and Simulation Performance Analysis](08.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
