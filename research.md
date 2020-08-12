---
layout: page
title: Research Summary
permalink: /research/ 
---
## 4G/5G PHY Layer Security
{% include image.html url="/images/Jamming_attacks_efficacy.png" caption="" width="393" height="288" align="right" %}  
The overarching contribution of this research was the qualitative, quantitative, and empirical investigation of the resiliency of critical control channels of 4G [1] and 5G [2] networks to intentional and unintentional RF interference. A key outcome was the analysis and mitigation of reference signal/pilot and non-pilot interference (PI/NPI) [3], [4], [5]. Prior to this research, it was a widely held notion that pilot signals must always be protected from interference [6], [7]. While this is true for demodulation reference signals, my work in [5] demonstrated *for the first time* that this is not always the case. Specifically, it showed that PI is desirable for cellular systems employing link adaptation based on pilot-aided channel state information (CSI) estimates and limited feedback. It also showed that ultra-low latency communications are vulnerable to NPI, and advocated the use of hybrid CSI estimation methods (methods that use pilot-aided as well as blind estimates) for robust link adaptation.

### References
1. M. Lichtman, R. P. Jover, M. Labib, **R. M. Rao**, V. Marojevic, and J. H. Reed, "LTE/LTE-A Jamming, Spoofing, and Sniffing: Threat Assessment and Mitigation," *IEEE Communications Magazine*, vol. 54, no. 4, pp. 54–61, April 2016.
2. M. Lichtman, **R. M. Rao**, V. Marojevic, J. Reed and R. P. Jover, "5G NR Jamming, Spoofing, and Sniffing: Threat Assessment and Mitigation," *in Proc. IEEE International Conference on Communications Workshops (ICC Workshops)*, pp. 1-6, May 2018.
3. **R. M. Rao**, S. Ha, V. Marojevic, and J. H. Reed, "LTE PHY Layer Vulnerability Analysis and Testing Using Open-Source SDR Tools," *in Proc. IEEE Military Communications Conference (MILCOM)*, pp. 744–749, October 2017.
4. V. Marojevic, **R. M. Rao**, S. Ha and J. H. Reed, "Performance Analysis of a Mission-Critical Portable LTE System in Targeted RF Interference," *in Proc. IEEE 86th Vehicular Technology Conference (VTC-Fall)*, pp. 1-6, September 2017.
5. **R. M. Rao**, V. Marojevic, and J. H. Reed, "Analysis of Non-Pilot Interference on Link Adaptation and Latency in Cellular Networks," *in Proc. of the IEEE 89th Vehicular Technology Conference (VTC-Spring)*, pp. 1–5, April 2019.
6. T. C. Clancy, "Efficient OFDM Denial: Pilot Jamming and Pilot Nulling," *in Proc. IEEE International Conference on Communications (ICC)*, pp. 1-5, June 2011.
7. M. Karlsson, E. Björnson and E. G. Larsson, "Jamming a TDD Point-to-Point Link Using Reciprocity-Based MIMO," *IEEE Transactions on Information Forensics and Security*, vol. 12, no. 12, pp. 2957-2970, Dec. 2017.

## Novel Link Adaptation Frameworks for Current and Future Cellular Systems
There are diverse use-cases in 5G and beyond-5G networks, each with potentially different channel conditions. Therefore to improve performance, it makes sense to customize the link adaptation scheme to meet the performance requirements of the use-case under consideration. In this contribution, I developed new link adaptation frameworks for the following scenarios.

### Vehicular and UAV Communications
{% include image.html url="/images/Pilot_adapt_V2V_UAV_illustrate.png" caption="" width="376" height="248" align="right" %}  
Vehicular and UAV channels are known to be highly nonstationary [1], with different fading characteristics when compared to conventional cellular fading channels. To leverage this, I designed a rate-maximizing PHY layer adaptation protocol illustrated here, where the pilot overhead is dynamically adapted along the time axis as a function of the coherence time of the channel, and along the frequency axis as a function of the coherence bandwidth of the channel [2], [3]. Furthermore, I designed 'channel statistics codebooks' to quantize the fading conditions, and facilitate real-time waveform adaptation using limited CSI feedback schemes, to yield significant rate enhancements when compared to fixed pilot configurations.

### References
1. L. Bernado, T. Zemen, F. Tufvesson, A. F. Molisch, and C. F. Mecklenbrauker, "Delay and Doppler Spreads of Nonstationary Vehicular Channels for Safety-Relevant Scenarios," *IEEE Transactions on Vehicular Technology*, vol. 63, no. 1, pp. 82–93, Jan 2014.
2. **R. M. Rao**, V. Marojevic, and J. H. Reed, "Adaptive Pilot Patterns for CA-OFDM Systems in Nonstationary Wireless Channels," *IEEE Transactions on Vehicular Technology*, vol. 67, no. 2, pp. 1231–1244, Feb 2018.
3. **R. M. Rao**, V. Marojevic, and J. Reed, "Rate-Maximizing OFDM Pilot Patterns for UAV Communications in Nonstationary A2G Channels," *in Proc. IEEE Vehicular Technology Conference (VTC-Fall2018)*, pp. 1-5, August 2018.
