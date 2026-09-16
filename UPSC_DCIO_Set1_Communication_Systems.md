# UPSC DCIO Communication Systems — Set 1 (50 Questions)

## Usage note
- This set is **originally written** for preparation and revision.
- Questions are **modeled on UPSC DCIO and comparable competitive-exam patterns**; they are not verbatim reproductions of copyrighted papers.
- References are mapped to standard textbook concepts for grounded study.

## Topic mix in this set
- Analog Communication: Q1–Q8
- Digital Communication: Q9–Q20
- Microwave Communication: Q21–Q28
- Radar Communication: Q29–Q35
- Satellite Communication: Q36–Q42
- Random Variables & Probability: Q43–Q50

---

## Analog Communication (Q1–Q8)

### Q1
- **Exam/Year Pattern**: UPSC DCIO-style, 2013 pattern
- **Question**: In AM (DSB-LC), modulation index is 0.6 and carrier power is 1 kW. Find total transmitted power.
- **Answer Key**: **1.18 kW**
- **Conceptual Solution**: Total AM power is carrier plus sideband powers. For single-tone AM: \(P_t=P_c(1+\mu^2/2)\).
- **Derivation**: \(P_t=1000(1+0.6^2/2)=1000(1+0.18)=1180\,\text{W}\).
- **Common Mistakes**: Using \(1+\mu^2\) instead of \(1+\mu^2/2\); confusing \(\mu\) with percentage.
- **Textbook Reference**: Haykin, *Communication Systems*, AM power relation chapter.
- **Likely Exam Relevance**: Very high (direct numerical).

### Q2
- **Exam/Year Pattern**: UPSC DCIO-style, 2015 pattern
- **Question**: For an FM signal with \(\Delta f=75\,\text{kHz}\) and modulating frequency \(f_m=15\,\text{kHz}\), find modulation index and approximate bandwidth by Carson’s rule.
- **Answer Key**: **\(\beta=5\), BW \(\approx 180\,\text{kHz}\)**
- **Conceptual Solution**: \(\beta=\Delta f/f_m\); Carson rule: \(B\approx2(\Delta f+f_m)\).
- **Derivation**: \(\beta=75/15=5\); \(B=2(75+15)=180\,\text{kHz}\).
- **Common Mistakes**: Taking \(2\Delta f\) only; mixing PM and FM definitions.
- **Textbook Reference**: Lathi, FM bandwidth and Carson rule section.
- **Likely Exam Relevance**: Very high.

### Q3
- **Exam/Year Pattern**: UPSC DCIO-style, 2011 pattern
- **Question**: A message signal has bandwidth 4 kHz. What minimum sampling frequency is required for faithful PCM conversion?
- **Answer Key**: **8 kHz**
- **Conceptual Solution**: Nyquist theorem requires \(f_s\ge2W\).
- **Derivation**: \(f_s\ge2\times4\,\text{kHz}=8\,\text{kHz}\).
- **Common Mistakes**: Using \(W\) instead of \(2W\); forgetting anti-alias filter assumption.
- **Textbook Reference**: Taub & Schilling / Lathi sampling theorem section.
- **Likely Exam Relevance**: High foundational.

### Q4
- **Exam/Year Pattern**: UPSC DCIO-style, 2016 pattern
- **Question**: In DSB-SC modulation, if local oscillator at receiver has phase error \(\phi\), recovered output scales by which factor?
- **Answer Key**: **\(\cos\phi\)**
- **Conceptual Solution**: Coherent detection multiplies by \(\cos(\omega_ct+\phi)\); low-pass term becomes proportional to \(m(t)\cos\phi\).
- **Derivation**: \(s(t)=m(t)\cos\omega_ct\), multiply with \(2\cos(\omega_ct+\phi)\Rightarrow m(t)\cos\phi+\text{HF term}\).
- **Common Mistakes**: Assuming complete loss for any nonzero \(\phi\); confusing with frequency offset case.
- **Textbook Reference**: Proakis/Salehi, coherent demodulation basics.
- **Likely Exam Relevance**: High conceptual.

### Q5
- **Exam/Year Pattern**: UPSC DCIO-style, 2018 pattern
- **Question**: Which modulation gives better noise immunity in high-SNR broadcast systems: AM or FM? State one quantitative reason.
- **Answer Key**: **FM; higher post-detection SNR improvement with larger deviation ratio**
- **Conceptual Solution**: FM suppresses amplitude noise via limiter and benefits from threshold/high-SNR behavior.
- **Derivation**: Qualitatively, output SNR of FM includes \(\beta^2\)-linked improvement in wideband FM region.
- **Common Mistakes**: Claiming FM always better regardless of channel bandwidth constraints.
- **Textbook Reference**: Haykin, angle modulation noise analysis chapter.
- **Likely Exam Relevance**: Medium-high theory.

### Q6
- **Exam/Year Pattern**: UPSC DCIO-style, 2014 pattern
- **Question**: In an SSB-SC transmitter, why is bandwidth half of DSB-SC for same message bandwidth \(W\)?
- **Answer Key**: **Only one sideband transmitted, so BW = \(W\) instead of \(2W\)**
- **Conceptual Solution**: Message spectrum shifts to \(f_c\pm f\); DSB sends both mirrored copies, SSB sends one.
- **Derivation**: DSB span \([f_c-W,f_c+W]\Rightarrow2W\); SSB keeps only USB or LSB \(\Rightarrow W\).
- **Common Mistakes**: Confusing occupied RF range with baseband width.
- **Textbook Reference**: Lathi, SSB generation and bandwidth efficiency.
- **Likely Exam Relevance**: High.

### Q7
- **Exam/Year Pattern**: UPSC DCIO-style, 2019 pattern
- **Question**: A pre-emphasis network in FM primarily boosts which part of message spectrum before transmission?
- **Answer Key**: **High-frequency components**
- **Conceptual Solution**: Noise at demodulator output rises with frequency; pre-emphasis boosts high frequencies before channel.
- **Derivation**: Combined pre-emphasis and de-emphasis yields near-flat response but reduced high-frequency noise contribution.
- **Common Mistakes**: Saying low frequencies are boosted.
- **Textbook Reference**: Haykin, FM noise and pre/de-emphasis.
- **Likely Exam Relevance**: Medium-high.

### Q8
- **Exam/Year Pattern**: UPSC DCIO-style, 2017 pattern
- **Question**: In envelope detection of AM, choose correct RC condition relative to carrier period \(T_c\) and modulation period \(T_m\).
- **Answer Key**: **\(T_c\ll RC\ll T_m\)**
- **Conceptual Solution**: RC must filter out carrier ripple but still track envelope variation.
- **Derivation**: If RC too small → ripple; too large → diagonal clipping.
- **Common Mistakes**: Reversing inequalities.
- **Textbook Reference**: Communication receivers chapter (envelope detector design).
- **Likely Exam Relevance**: Very high objective question type.

---

## Digital Communication (Q9–Q20)

### Q9
- **Exam/Year Pattern**: UPSC DCIO-style, 2012 pattern
- **Question**: A binary symmetric channel has bit error probability \(p=10^{-3}\). Find probability of correct bit reception.
- **Answer Key**: **0.999**
- **Conceptual Solution**: Correct reception probability = \(1-p\).
- **Derivation**: \(1-10^{-3}=0.999\).
- **Common Mistakes**: Confusing with packet-level correctness.
- **Textbook Reference**: Proakis, discrete channel models.
- **Likely Exam Relevance**: High basic probability in digital comm.

### Q10
- **Exam/Year Pattern**: UPSC DCIO-style, 2015 pattern
- **Question**: For BPSK over AWGN, BER is expressed in terms of \(E_b/N_0\) as?
- **Answer Key**: **\(P_b=Q\!\left(\sqrt{2E_b/N_0}\right)\)**
- **Conceptual Solution**: Optimum coherent binary detection yields Gaussian tail error probability.
- **Derivation**: Decision variable mean separation \(2\sqrt{E_b}\), noise variance \(N_0/2\) leads to argument \(\sqrt{2E_b/N_0}\).
- **Common Mistakes**: Using \(Q(\sqrt{E_b/N_0})\).
- **Textbook Reference**: Proakis, BPSK performance derivation.
- **Likely Exam Relevance**: Very high.

### Q11
- **Exam/Year Pattern**: UPSC DCIO-style, 2016 pattern
- **Question**: In 16-QAM, bits per symbol are?
- **Answer Key**: **4 bits/symbol**
- **Conceptual Solution**: \(M\)-ary modulation carries \(\log_2 M\) bits/symbol.
- **Derivation**: \(\log_2(16)=4\).
- **Common Mistakes**: Using \(\sqrt{M}\).
- **Textbook Reference**: Digital modulation chapter.
- **Likely Exam Relevance**: Very high quick objective.

### Q12
- **Exam/Year Pattern**: UPSC DCIO-style, 2017 pattern
- **Question**: A raised-cosine filter has roll-off factor \(\alpha=0.25\), symbol rate \(R_s=1\) Msps. Find null-to-null RF bandwidth.
- **Answer Key**: **1.25 MHz**
- **Conceptual Solution**: Baseband Nyquist bandwidth for raised cosine: \(B=(1+\alpha)R_s/2\); passband null-to-null is \((1+\alpha)R_s\).
- **Derivation**: \((1+0.25)\times1=1.25\,\text{MHz}\).
- **Common Mistakes**: Forgetting factor 2 between baseband and passband views.
- **Textbook Reference**: Proakis, pulse shaping and ISI.
- **Likely Exam Relevance**: High.

### Q13
- **Exam/Year Pattern**: UPSC DCIO-style, 2014 pattern
- **Question**: Why is Gray coding preferred in QAM symbol mapping?
- **Answer Key**: **Adjacent symbols differ by 1 bit, reducing BER impact of nearest-neighbor errors**
- **Conceptual Solution**: Most errors are to nearest constellation points.
- **Derivation**: Symbol error causes minimum bit flips under Gray assignment.
- **Common Mistakes**: Claiming it changes SER significantly (it mainly improves BER mapping).
- **Textbook Reference**: Digital modulation mapping section.
- **Likely Exam Relevance**: High conceptual.

### Q14
- **Exam/Year Pattern**: UPSC DCIO-style, 2018 pattern
- **Question**: In PCM with 8-bit quantizer, how many quantization levels are available?
- **Answer Key**: **256**
- **Conceptual Solution**: \(L=2^n\) for \(n\)-bit uniform quantizer.
- **Derivation**: \(2^8=256\).
- **Common Mistakes**: Using \(2n\).
- **Textbook Reference**: PCM fundamentals.
- **Likely Exam Relevance**: Very high.

### Q15
- **Exam/Year Pattern**: UPSC DCIO-style, 2019 pattern
- **Question**: What is the principal benefit of differential encoding before BPSK demodulation in uncertain carrier phase environments?
- **Answer Key**: **Eliminates need for absolute carrier phase reference (resolves \(\pi\)-phase ambiguity)**
- **Conceptual Solution**: Information carried in phase change, not absolute phase.
- **Derivation**: Decision compares current symbol with previous symbol phase.
- **Common Mistakes**: Thinking differential coding improves AWGN BER of coherent BPSK.
- **Textbook Reference**: DPSK/BPSK detection chapter.
- **Likely Exam Relevance**: Medium-high.

### Q16
- **Exam/Year Pattern**: UPSC DCIO-style, 2020 pattern
- **Question**: If code rate is \(R_c=k/n=1/2\), and source bit rate is 1 Mbps, what coded bit rate is transmitted?
- **Answer Key**: **2 Mbps**
- **Conceptual Solution**: Coded rate expands by factor \(n/k=1/R_c\).
- **Derivation**: \(1/0.5=2\Rightarrow2\,\text{Mbps}\).
- **Common Mistakes**: Multiplying by \(R_c\) instead of dividing.
- **Textbook Reference**: Error control coding fundamentals.
- **Likely Exam Relevance**: High numericals.

### Q17
- **Exam/Year Pattern**: UPSC DCIO-style, 2013 pattern
- **Question**: For BFSK coherent detection with orthogonal tones, compare required \(E_b/N_0\) to BPSK for same BER.
- **Answer Key**: **BFSK needs about 3 dB more than BPSK**
- **Conceptual Solution**: Orthogonal BFSK has lower distance efficiency than BPSK.
- **Derivation**: BER forms imply doubling in required \(E_b/N_0\) roughly (≈3 dB penalty).
- **Common Mistakes**: Treating coherent BFSK and BPSK as identical in BER.
- **Textbook Reference**: Proakis, binary modulation comparisons.
- **Likely Exam Relevance**: High comparison question.

### Q18
- **Exam/Year Pattern**: UPSC DCIO-style, 2011 pattern
- **Question**: Define ISI and state Nyquist first criterion in one line.
- **Answer Key**: **ISI is interference from neighboring symbols; Nyquist criterion requires pulse samples at symbol instants to be 1 at origin and 0 at all other symbol intervals.**
- **Conceptual Solution**: Receiver decision time samples should not contain contributions from adjacent symbols.
- **Derivation**: \(p(0)=1,\;p(nT)=0\;\forall n\neq0\).
- **Common Mistakes**: Confusing with channel equalization condition.
- **Textbook Reference**: Nyquist pulse shaping chapter.
- **Likely Exam Relevance**: Very high theory short note.

### Q19
- **Exam/Year Pattern**: UPSC DCIO-style, 2021 pattern
- **Question**: For binary data rate \(R_b\), what minimum theoretical baseband bandwidth is required for ideal Nyquist signaling?
- **Answer Key**: **\(R_b/2\)**
- **Conceptual Solution**: Symbol rate for binary equals bit rate; Nyquist minimum baseband bandwidth = \(R_s/2\).
- **Derivation**: \(B_{min}=R_b/2\).
- **Common Mistakes**: Giving \(R_b\) directly.
- **Textbook Reference**: Digital baseband transmission theory.
- **Likely Exam Relevance**: High.

### Q20
- **Exam/Year Pattern**: UPSC DCIO-style, 2022 pattern
- **Question**: A communication system uses 64-QAM at symbol rate 500 ksym/s. Compute gross bit rate.
- **Answer Key**: **3 Mbps**
- **Conceptual Solution**: Bits/symbol = \(\log_2 64 =6\).
- **Derivation**: \(R_b=R_s\log_2M=500\times10^3\times6=3\times10^6\,\text{bps}\).
- **Common Mistakes**: Taking \(\log_{10}\) instead of \(\log_2\).
- **Textbook Reference**: M-ary QAM throughput relation.
- **Likely Exam Relevance**: Very high objective numerical.

---

## Microwave Communication (Q21–Q28)

### Q21
- **Exam/Year Pattern**: UPSC DCIO-style, 2014 pattern
- **Question**: Define cutoff frequency of a rectangular waveguide in dominant TE10 mode in terms of broad dimension \(a\).
- **Answer Key**: **\(f_c=c/(2a)\)**
- **Conceptual Solution**: TE10 has one half-wave variation across \(a\), none across \(b\).
- **Derivation**: \(f_{c,mn}=\frac{c}{2}\sqrt{(m/a)^2+(n/b)^2}\Rightarrow m=1,n=0\).
- **Common Mistakes**: Using \(b\) instead of \(a\).
- **Textbook Reference**: Pozar/Ramo-Whinnery waveguide theory.
- **Likely Exam Relevance**: Very high.

### Q22
- **Exam/Year Pattern**: UPSC DCIO-style, 2016 pattern
- **Question**: Why are hollow metallic waveguides preferred over coax at very high microwave frequencies?
- **Answer Key**: **Lower conductor/dielectric loss and higher power handling**
- **Conceptual Solution**: Coax suffers higher attenuation due to skin effect and dielectric loss at high GHz range.
- **Derivation**: Attenuation trends increase with frequency in coax more rapidly than waveguide dominant-mode transport.
- **Common Mistakes**: Saying waveguide has no cutoff issue.
- **Textbook Reference**: Microwave engineering transmission media comparison.
- **Likely Exam Relevance**: High conceptual.

### Q23
- **Exam/Year Pattern**: UPSC DCIO-style, 2012 pattern
- **Question**: VSWR is 3. Find magnitude of reflection coefficient \(|\Gamma|\).
- **Answer Key**: **0.5**
- **Conceptual Solution**: \(\text{VSWR}=(1+|\Gamma|)/(1-|\Gamma|)\).
- **Derivation**: \(|\Gamma|=(S-1)/(S+1)=(3-1)/(3+1)=0.5\).
- **Common Mistakes**: Forgetting magnitude and sign distinction.
- **Textbook Reference**: Transmission line basics.
- **Likely Exam Relevance**: Very high numerical.

### Q24
- **Exam/Year Pattern**: UPSC DCIO-style, 2019 pattern
- **Question**: In Smith chart use, what does center point represent?
- **Answer Key**: **Matched load, normalized impedance \(z=1+j0\), \(\Gamma=0\)**
- **Conceptual Solution**: Center means no reflection.
- **Derivation**: \(\Gamma=(z-1)/(z+1)=0\Rightarrow z=1\).
- **Common Mistakes**: Confusing center with short/open.
- **Textbook Reference**: Pozar, Smith chart fundamentals.
- **Likely Exam Relevance**: High.

### Q25
- **Exam/Year Pattern**: UPSC DCIO-style, 2017 pattern
- **Question**: A 20 dB directional coupler has input power 10 W. Coupled port power is?
- **Answer Key**: **0.1 W**
- **Conceptual Solution**: Coupling in dB: \(C=10\log_{10}(P_{in}/P_c)\).
- **Derivation**: \(P_c=P_{in}/10^{C/10}=10/100=0.1\,\text{W}\).
- **Common Mistakes**: Treating dB as linear subtraction in watts.
- **Textbook Reference**: Microwave passive components chapter.
- **Likely Exam Relevance**: Medium-high.

### Q26
- **Exam/Year Pattern**: UPSC DCIO-style, 2020 pattern
- **Question**: Why is klystron typically used as a microwave oscillator/amplifier rather than low-frequency source?
- **Answer Key**: **Velocity modulation and cavity resonance are efficient at microwave frequencies**
- **Conceptual Solution**: Transit-time effects become meaningful at microwave frequencies.
- **Derivation**: Bunching mechanism requires electron transit comparable to RF period.
- **Common Mistakes**: Overgeneralizing as “higher gain at all frequencies.”
- **Textbook Reference**: Microwave tubes chapter.
- **Likely Exam Relevance**: Medium.

### Q27
- **Exam/Year Pattern**: UPSC DCIO-style, 2018 pattern
- **Question**: For free-space path loss, if distance doubles (frequency fixed), attenuation changes by?
- **Answer Key**: **+6 dB loss**
- **Conceptual Solution**: FSPL \(\propto d^2\), so power ratio becomes 4.
- **Derivation**: \(10\log_{10}(4)=6.02\,\text{dB}\).
- **Common Mistakes**: Confusing voltage ratio with power ratio.
- **Textbook Reference**: Friis transmission equation.
- **Likely Exam Relevance**: Very high.

### Q28
- **Exam/Year Pattern**: UPSC DCIO-style, 2021 pattern
- **Question**: State one practical function of isolator in microwave bench.
- **Answer Key**: **Protects source from reflected power and stabilizes measurements**
- **Conceptual Solution**: One-way device absorbs reverse wave.
- **Derivation**: Reverse attenuation high, forward insertion low.
- **Common Mistakes**: Confusing isolator with circulator routing function.
- **Textbook Reference**: Microwave measurement components.
- **Likely Exam Relevance**: High lab-application objective.

---

## Radar Communication (Q29–Q35)

### Q29
- **Exam/Year Pattern**: UPSC DCIO-style, 2013 pattern
- **Question**: Write basic monostatic radar range equation dependency for received power on range \(R\).
- **Answer Key**: **\(P_r\propto 1/R^4\)**
- **Conceptual Solution**: Two-way spreading: transmit path \(1/R^2\), return path \(1/R^2\).
- **Derivation**: Standard radar equation contains \((4\pi)^3R^4\) in denominator.
- **Common Mistakes**: Writing \(1/R^2\) as in one-way link.
- **Textbook Reference**: Skolnik, basic radar equation.
- **Likely Exam Relevance**: Very high.

### Q30
- **Exam/Year Pattern**: UPSC DCIO-style, 2015 pattern
- **Question**: If pulse width is \(1\,\mu s\), what is radar range resolution (approx)?
- **Answer Key**: **150 m**
- **Conceptual Solution**: \(\Delta R=c\tau/2\).
- **Derivation**: \(3\times10^8\times10^{-6}/2=150\,\text{m}\).
- **Common Mistakes**: Missing factor 1/2.
- **Textbook Reference**: Radar pulse characteristics.
- **Likely Exam Relevance**: Very high.

### Q31
- **Exam/Year Pattern**: UPSC DCIO-style, 2019 pattern
- **Question**: PRF is 1 kHz. Find maximum unambiguous range.
- **Answer Key**: **150 km**
- **Conceptual Solution**: \(R_{unamb}=c/(2\,\text{PRF})\).
- **Derivation**: \(3\times10^8/(2\times10^3)=1.5\times10^5\,\text{m}=150\,\text{km}\).
- **Common Mistakes**: Using pulse width instead of PRI.
- **Textbook Reference**: Radar timing and ambiguities.
- **Likely Exam Relevance**: Very high.

### Q32
- **Exam/Year Pattern**: UPSC DCIO-style, 2016 pattern
- **Question**: Doppler frequency shift in monostatic radar for radial speed \(v\) and wavelength \(\lambda\) is?
- **Answer Key**: **\(f_d=2v/\lambda\)**
- **Conceptual Solution**: Outgoing and returning paths each contribute shift.
- **Derivation**: Two-way Doppler doubles one-way shift.
- **Common Mistakes**: Using \(v/\lambda\).
- **Textbook Reference**: MTI/Doppler radar basics.
- **Likely Exam Relevance**: Very high.

### Q33
- **Exam/Year Pattern**: UPSC DCIO-style, 2018 pattern
- **Question**: Why is matched filter used in radar receiver?
- **Answer Key**: **Maximizes output SNR for known signal in AWGN**
- **Conceptual Solution**: Matched filter impulse response is time-reversed conjugate of transmitted pulse.
- **Derivation**: Cauchy–Schwarz based optimization gives peak SNR at sampling instant.
- **Common Mistakes**: Saying it only amplifies signal amplitude.
- **Textbook Reference**: Radar signal processing fundamentals.
- **Likely Exam Relevance**: High conceptual.

### Q34
- **Exam/Year Pattern**: UPSC DCIO-style, 2020 pattern
- **Question**: A target has RCS of 10 m² and another 1 m², with all else same. Received power ratio is?
- **Answer Key**: **10:1**
- **Conceptual Solution**: Radar equation has direct proportionality to \(\sigma\) (RCS).
- **Derivation**: \(P_r\propto\sigma\Rightarrow10/1=10\).
- **Common Mistakes**: Taking square root relation.
- **Textbook Reference**: Radar cross-section concept.
- **Likely Exam Relevance**: Medium-high.

### Q35
- **Exam/Year Pattern**: UPSC DCIO-style, 2022 pattern
- **Question**: State one key advantage of pulse compression radar.
- **Answer Key**: **Simultaneously high range resolution and high transmitted energy**
- **Conceptual Solution**: Long coded pulse gives energy; matched filtering compresses to short effective pulse.
- **Derivation**: Compression ratio \(\approx BT\) improves resolution equivalent to short pulse \(1/B\).
- **Common Mistakes**: Assuming pulse compression increases peak transmit power requirement.
- **Textbook Reference**: Modern radar waveforms chapter.
- **Likely Exam Relevance**: High modern radar topic.

---

## Satellite Communication (Q36–Q42)

### Q36
- **Exam/Year Pattern**: UPSC DCIO-style, 2012 pattern
- **Question**: Why are GEO satellites preferred for fixed broadcast TV services?
- **Answer Key**: **Earth-station antenna can remain fixed due to near-constant satellite position**
- **Conceptual Solution**: GEO period matches Earth rotation.
- **Derivation**: Orbital period 24 h at equatorial circular orbit gives stationary longitude viewpoint.
- **Common Mistakes**: Saying GEO gives lowest path loss (LEO can be lower).
- **Textbook Reference**: Pratt/Bostian satellite orbit basics.
- **Likely Exam Relevance**: Very high.

### Q37
- **Exam/Year Pattern**: UPSC DCIO-style, 2014 pattern
- **Question**: Uplink frequency is generally kept higher than downlink in many satellite bands. Why?
- **Answer Key**: **Satellite transmitter power is limited; lower downlink frequency reduces free-space and atmospheric losses**
- **Conceptual Solution**: Ground stations can provide higher uplink power and larger antennas.
- **Derivation**: FSPL \(\propto f^2\), so lower \(f\) helps downlink budget.
- **Common Mistakes**: Treating this as universal for all systems without band planning context.
- **Textbook Reference**: Satellite link budget sections.
- **Likely Exam Relevance**: High.

### Q38
- **Exam/Year Pattern**: UPSC DCIO-style, 2017 pattern
- **Question**: Define EIRP in one expression.
- **Answer Key**: **\(\text{EIRP}=P_tG_t\)** (or in dB: \(\text{EIRP}_{dBW}=P_{t,dBW}+G_{t,dBi}-L_{tx,dB}\) if losses included)
- **Conceptual Solution**: Effective isotropic radiated power represents directional radiated strength.
- **Derivation**: Isotropic-equivalent power by multiplying transmitter power with antenna gain.
- **Common Mistakes**: Subtracting gain instead of adding in dB form.
- **Textbook Reference**: Link equation terminology.
- **Likely Exam Relevance**: Very high.

### Q39
- **Exam/Year Pattern**: UPSC DCIO-style, 2018 pattern
- **Question**: For a bent-pipe transponder, identify its main operation.
- **Answer Key**: **Receive, frequency translate, amplify, and retransmit without baseband decoding**
- **Conceptual Solution**: Acts as RF repeater.
- **Derivation**: No regeneration of digital payload at satellite in simple transponder architecture.
- **Common Mistakes**: Confusing with regenerative onboard processing satellites.
- **Textbook Reference**: Satellite payload architectures.
- **Likely Exam Relevance**: High.

### Q40
- **Exam/Year Pattern**: UPSC DCIO-style, 2019 pattern
- **Question**: Round-trip GEO satellite delay is roughly close to which value?
- **Answer Key**: **About 240 ms for one Earth–satellite–Earth hop; about 480 ms for round-trip (two hops)**
- **Conceptual Solution**: Propagation delay dominates due to ~36,000 km altitude.
- **Derivation**: One hop path \\(\\approx 2\\times36,000\\,\\text{km}=72,000\\,\\text{km}\\), so delay \\(\\approx72,000/300,000\\,\\text{s}=0.24\\,\\text{s}\\).
- **Common Mistakes**: Confusing one-way with round-trip and application-level RTT.
- **Textbook Reference**: Satellite propagation delay discussion.
- **Likely Exam Relevance**: Medium-high.

### Q41
- **Exam/Year Pattern**: UPSC DCIO-style, 2021 pattern
- **Question**: What is rain fade and which frequency bands are more vulnerable?
- **Answer Key**: **Rain-induced attenuation; stronger in Ku/Ka and above compared with C-band**
- **Conceptual Solution**: Scattering/absorption increase with frequency.
- **Derivation**: Specific attenuation models show higher dB/km with higher GHz bands.
- **Common Mistakes**: Assuming L-band suffers similar severe fade.
- **Textbook Reference**: Satellite propagation impairments chapter.
- **Likely Exam Relevance**: High practical topic.

### Q42
- **Exam/Year Pattern**: UPSC DCIO-style, 2022 pattern
- **Question**: In multiple access for satellite networks, which method assigns distinct time slots to users on same carrier?
- **Answer Key**: **TDMA**
- **Conceptual Solution**: Users share frequency but transmit in scheduled non-overlapping times.
- **Derivation**: Frame structure partitioned into burst slots.
- **Common Mistakes**: Mixing TDMA with FDMA/CDMA.
- **Textbook Reference**: Satellite multiple access techniques.
- **Likely Exam Relevance**: Very high objective.

---

## Random Variables & Probability (Q43–Q50)

### Q43
- **Exam/Year Pattern**: UPSC DCIO-style, 2013 pattern
- **Question**: If \(X\sim\mathcal{N}(\mu,\sigma^2)\), define standardized variable \(Z\).
- **Answer Key**: **\(Z=(X-\mu)/\sigma\)**
- **Conceptual Solution**: Standardization maps normal RV to zero-mean, unit-variance form.
- **Derivation**: Affine transform of Gaussian preserves Gaussianity.
- **Common Mistakes**: Using \(\sigma^2\) in denominator.
- **Textbook Reference**: Papoulis & Pillai, normal distribution basics.
- **Likely Exam Relevance**: Very high prerequisite.

### Q44
- **Exam/Year Pattern**: UPSC DCIO-style, 2015 pattern
- **Question**: For exponential RV with parameter \(\lambda\), find mean and variance.
- **Answer Key**: **Mean \(1/\lambda\), variance \(1/\lambda^2\)**
- **Conceptual Solution**: Direct moments from pdf \(f(x)=\lambda e^{-\lambda x}, x\ge0\).
- **Derivation**: Integrate \(E[X]=\int_0^\infty x\lambda e^{-\lambda x}dx\), \(E[X^2]\) similarly.
- **Common Mistakes**: Interchanging mean and variance formulas.
- **Textbook Reference**: Random variable moments chapter.
- **Likely Exam Relevance**: High.

### Q45
- **Exam/Year Pattern**: UPSC DCIO-style, 2016 pattern
- **Question**: Two independent zero-mean RVs \(X,Y\) have variances 4 and 9. Find \(\mathrm{Var}(X+Y)\).
- **Answer Key**: **13**
- **Conceptual Solution**: Variances add for independent RVs.
- **Derivation**: \(\mathrm{Var}(X+Y)=\mathrm{Var}(X)+\mathrm{Var}(Y)+2\mathrm{Cov}(X,Y)=4+9+0\).
- **Common Mistakes**: Adding standard deviations.
- **Textbook Reference**: Second-order moments and covariance.
- **Likely Exam Relevance**: Very high.

### Q46
- **Exam/Year Pattern**: UPSC DCIO-style, 2017 pattern
- **Question**: If noise PSD is \(N_0/2\) (two-sided), noise power over bandwidth \(B\) (low-pass equivalent) is?
- **Answer Key**: **\(N_0B\)**
- **Conceptual Solution**: Integrate two-sided PSD over \([-B,B]\).
- **Derivation**: \(\int_{-B}^{B}(N_0/2)df=N_0B\).
- **Common Mistakes**: Using \(N_0B/2\) incorrectly.
- **Textbook Reference**: AWGN model in communication theory.
- **Likely Exam Relevance**: Very high.

### Q47
- **Exam/Year Pattern**: UPSC DCIO-style, 2018 pattern
- **Question**: Correlation coefficient \(\rho_{XY}=0\) implies what always true statement?
- **Answer Key**: **X and Y are uncorrelated (not necessarily independent)**
- **Conceptual Solution**: Zero covariance is weaker than independence except special distributions (e.g., jointly Gaussian).
- **Derivation**: \(\rho=0\Rightarrow\mathrm{Cov}(X,Y)=0\).
- **Common Mistakes**: Claiming independence always follows.
- **Textbook Reference**: Joint distributions and dependence concepts.
- **Likely Exam Relevance**: Very high conceptual trap.

### Q48
- **Exam/Year Pattern**: UPSC DCIO-style, 2019 pattern
- **Question**: If \(X\) is uniform on \([0,1]\), find \(P(X>0.7)\).
- **Answer Key**: **0.3**
- **Conceptual Solution**: Uniform probability equals interval length.
- **Derivation**: \(\int_{0.7}^{1}1\,dx=0.3\).
- **Common Mistakes**: Using 0.7 directly.
- **Textbook Reference**: Uniform distribution basics.
- **Likely Exam Relevance**: Medium-high quick numerical.

### Q49
- **Exam/Year Pattern**: UPSC DCIO-style, 2020 pattern
- **Question**: State central limit theorem relevance to communication noise modeling.
- **Answer Key**: **Sum of many independent small disturbances tends to Gaussian, justifying AWGN approximation**
- **Conceptual Solution**: Thermal/electronic noise sources aggregate to near-normal process.
- **Derivation**: Normalized sum convergence in distribution to Gaussian.
- **Common Mistakes**: Assuming exact Gaussian for any small sample count.
- **Textbook Reference**: Probability foundations + noise modeling chapter.
- **Likely Exam Relevance**: High theory.

### Q50
- **Exam/Year Pattern**: UPSC DCIO-style, 2022 pattern
- **Question**: For Poisson RV with mean \(\lambda\), what is variance?
- **Answer Key**: **\(\lambda\)**
- **Conceptual Solution**: Poisson has equal mean and variance.
- **Derivation**: From mgf/pmf moments, \(E[X]=\lambda\), \(E[X^2]-E[X]^2=\lambda\).
- **Common Mistakes**: Writing \(\lambda^2\).
- **Textbook Reference**: Discrete distributions chapter.
- **Likely Exam Relevance**: Very high objective.

---

## Compact Answer Key (Q1–Q50)
1) 1.18 kW; 2) \(\beta=5\), 180 kHz; 3) 8 kHz; 4) \(\cos\phi\); 5) FM; 6) BW halved in SSB; 7) High-frequency boost; 8) \(T_c\ll RC\ll T_m\); 9) 0.999; 10) \(Q(\sqrt{2E_b/N_0})\); 11) 4; 12) 1.25 MHz; 13) Gray minimizes bit errors; 14) 256; 15) Resolves phase ambiguity; 16) 2 Mbps; 17) BFSK needs ~3 dB more; 18) Nyquist zero-ISI condition; 19) \(R_b/2\); 20) 3 Mbps; 21) \(c/(2a)\); 22) Lower high-frequency loss & better power handling; 23) 0.5; 24) Center is match; 25) 0.1 W; 26) Transit-time/velocity modulation suited to microwaves; 27) +6 dB loss; 28) Protect source from reflections; 29) \(1/R^4\); 30) 150 m; 31) 150 km; 32) \(2v/\lambda\); 33) Max-SNR detector; 34) 10:1; 35) High resolution + high energy; 36) Fixed earth pointing in GEO; 37) Lower-loss downlink choice; 38) EIRP \(=P_tG_t\); 39) Bent-pipe repeater; 40) ~240 ms per Earth-sat-Earth hop; 41) Rain fade severe at Ku/Ka; 42) TDMA; 43) \((X-\mu)/\sigma\); 44) mean \(1/\lambda\), var \(1/\lambda^2\); 45) 13; 46) \(N_0B\); 47) Uncorrelated not independent; 48) 0.3; 49) CLT supports Gaussian noise model; 50) variance \(=\lambda\).

## Standard Textbook Base (used across solutions)
1. Simon Haykin, *Communication Systems*.
2. B. P. Lathi, *Modern Digital and Analog Communication Systems*.
3. John G. Proakis & Masoud Salehi, *Digital Communications*.
4. M. I. Skolnik, *Introduction to Radar Systems*.
5. D. M. Pozar, *Microwave Engineering*.
6. A. Papoulis & S. U. Pillai, *Probability, Random Variables and Stochastic Processes*.
