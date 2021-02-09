---
layout: page
title: Research Summary
permalink: /research/ 
---
## 4G/5G PHY Layer Security
{% include image.html url="/images/Jamming_attacks_efficacy.png" caption="" width="393" height="288" align="right" %}  
The overarching contribution of this research was the qualitative, quantitative, and empirical investigation of the resiliency of critical control channels of 4G [1] and 5G [2] networks to intentional and unintentional RF interference. A key outcome was the analysis and mitigation of reference signal/pilot and non-pilot interference (PI/NPI) [3], [4], [5]. Prior to this research, it was a widely held notion that pilot signals must always be protected from interference [6], [7]. While this is true for demodulation reference signals, my work in [5] demonstrated *for the first time* that this is not always the case. Specifically, it showed that PI is desirable for cellular systems employing link adaptation based on pilot-aided channel state information (CSI) estimates and limited feedback. It also showed that ultra-low latency communications are vulnerable to NPI, and advocated the use of hybrid CSI estimation methods (methods that use pilot-aided as well as blind estimates) for robust link adaptation.

#### References
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

#### References
1. L. Bernado, T. Zemen, F. Tufvesson, A. F. Molisch, and C. F. Mecklenbrauker, "Delay and Doppler Spreads of Nonstationary Vehicular Channels for Safety-Relevant Scenarios," *IEEE Transactions on Vehicular Technology*, vol. 63, no. 1, pp. 82–93, Jan 2014.
2. **R. M. Rao**, V. Marojevic, and J. H. Reed, "Adaptive Pilot Patterns for CA-OFDM Systems in Nonstationary Wireless Channels," *IEEE Transactions on Vehicular Technology*, vol. 67, no. 2, pp. 1231–1244, Feb 2018.
3. **R. M. Rao**, V. Marojevic, and J. Reed, "Rate-Maximizing OFDM Pilot Patterns for UAV Communications in Nonstationary A2G Channels," *in Proc. IEEE Vehicular Technology Conference (VTC-Fall2018)*, pp. 1-5, August 2018.

### 4G LTE meets Massive MIMO
{% include image.html url="/images/Agile_BF_scheduler_scheme.png" caption="" width="380" height="194" align="right" %}  
The use of massive MIMO technologies were introduced in LTE-Advanced Pro (3GPP Release 14). Even though LTE-A Pro/5G massive MIMO base stations can improve the rate of 4G networks in theory, this is inhibited by the incompatibility of LTE's CSI feedback mechanism with that of 5G. To bridge this gap, I designed a coordinated *agile beamformer-scheduler* system that is backward-compatible with 4G LTE in [1], shown here. While the massive MIMO array generated rapidly time-varying (agile) narrow beams to improve SINR in all regions of the cell at different times, scheduler coordination ensured that users actually experiencing the instantaneous SINR gain are served. This scheme significantly enhanced the cell throughput performance when compared to legacy LTE schemes, demonstrating that it is possible to leverage 5G infrastructure to provide significant coverage and rate enhancements in 4G LTE networks.

#### References
1. **R. M. Rao**, D. Bethanabhotla, and R. C. Palat, “Enhancing Throughput Using Agile Beam Switching and User Scheduling in Cellular Systems,” *in Proc. IEEE 90th Vehicular Technology Conference (VTC2019-Fall)*, pp. 1-7, 2019.

### Pulsed Radar-Cellular Coexistence
{% include image.html url="/images/Fig_TVT_Act_vs_pilaid_SINR_frep_320.png" caption="" width="418" height="372" align="right" %}
Unlike conventional cellular systems, intermittent pulsed radar interference in shared spectrum results in two channel states: (a) *'fading channel (FC) state'* in the absence of radar, and (b) *'interference channel (IC) state'* in the presence of radar, as shown in the figure. In [1], I demonstrated that limited CSI feedback schemes based on pilot-aided estimates fail to estimate the IC's CSI, rendering the cellular system vulnerable to link adaptation failure. I resolved this in [2], where I proposed a comprehensive semi-blind SINR estimation framework using pilot-aided estimates and a robust max-min heuristic to compute the wideband SINR of radar-impaired subframes. To handle channel bimodality, I proposed (a) *dual CSI feedback*, where all users report their quantized CSI for both channel states, and (b) *radar indicator feedback*, where a single user per cell feeds back quantized information about future radar-impaired subframes. Unifying these schemes resulted in huge simultaneous improvements in the downlink throughput, BLER, and latency.

#### References
1. **R. M. Rao**, V. Marojevic and J. H. Reed, "Probability of Pilot Interference in Radar-Cellular Coexistence: Insights on Demodulation, CSI Estimation, and Limited Feedback," *IEEE Communications Letters*, vol. 24, no. 8, pp. 1678-1682, 2020.
2. **R. M. Rao**, V. Marojevic and J. H. Reed, "Semi-Blind Post-Equalizer SINR Estimation and Dual CSI Feedback for Radar-Cellular Coexistence," *IEEE Transactions on Vehicular Technology*, vol. 69, no. 9, pp. 9720-9735, 2020.
 
## Mathematical Modeling and Performance Analysis of Underlay Spectrum Sharing Scenarios
{% include image.html url="/images/Fig1_Radar_mMIMO_SpecShare_Illustration.png" caption="" width="380" height="257" align="right" %}
Tractable mathematical modeling of large spectrum sharing networks can yield fundamental insights into macro-scale performance trends, which are hard to obtain using sophisticated protocol-oriented system-level simulation studies. In [1],[2], I developed a tractable stochastic geometry-based framework to analyze performance of underlay radar-massive MIMO cellular spectrum sharing scenarios. Major novelties of this work was the modeling of 3D beamforming capabilities of the radar and the BSs, which uncovered the relationship between the cell-size and worst-case BS transmit beamforming gain. The analytical framework presented in this work (a) enables network designers to systematically isolate and evaluate the impact of each deployment parameter on the worst-case radar performance, and (b) complements industry-standard simulation methodologies, by establishing a baseline performance for each  set of deployment parameters.
	
In [3], we proposed a mathematical framework to harmonize spectral efficiency and coverage performance in underlay spectrum sharing scenarios between 3D UAV and D2D networks, using tools from stochastic geometry and machine learning. A major novelty was the flexibility of this framework to incorporate arbitrary distributions of UAVs in 3D space.

#### References
1. **R. M. Rao**, H. S. Dhillon, V. Marojevic, J. H. Reed, "Analysis of Worst-Case Interference in Underlay Radar-Massive MIMO Spectrum Sharing Scenarios," *in Proc. IEEE Global Communications Conference (Globecom)*, pp. 1-6, Waikoloa, HI, 2019.
2. **R. M. Rao**, H. S. Dhillon, V. Marojevic and J. H. Reed, “Underlay Radar-Massive MIMO Spectrum Sharing: Modeling Fundamentals and Performance Analysis,” *under major revision, available arxiv:2008.02100*.
3. B. Shang, L. Liu, **R. M. Rao**, V. Marojevic, J. H. Reed, "3D Spectrum Sharing for Hybrid D2D and UAV Networks," *IEEE Transactions on Communications*, vol. 68, no. 9, pp. 5375-5389, 2020.
