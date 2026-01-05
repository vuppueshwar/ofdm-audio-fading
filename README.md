# ofdm-audio-fading
# OFDM-Based Audio Transmission over Wireless Fading Channels

This project implements a complete **QPSK-based OFDM audio transmission system** and evaluates its performance over realistic wireless channels including **AWGN, Rayleigh, and Rician fading**. The system demonstrates the impact of multipath fading and the effectiveness of **pilot-assisted channel estimation and equalization**.

---

## 📌 Project Overview

- Modulation: **QPSK**
- OFDM Subcarriers: **64**
- Cyclic Prefix Length: **16**
- Channel Models:
  - AWGN
  - Rayleigh Fading
  - Rician Fading (configurable K-factor)
- Channel Estimation: **Pilot-based Least Squares (LS)**
- Equalization: **Zero-Forcing (ZF)**

The input is a real **audio signal**, which is transmitted through the OFDM system and reconstructed at the receiver for qualitative and quantitative evaluation.

---

## 🧱 System Architecture

1. Audio signal preprocessing and normalization  
2. Bitstream generation (16-bit PCM)  
3. QPSK modulation  
4. OFDM modulation with pilot insertion  
5. Wireless channel simulation  
6. Channel estimation and equalization (Rayleigh & Rician)  
7. OFDM demodulation and audio reconstruction  
8. Performance analysis and visualization  

---

## 📊 Performance Analysis

The system evaluates performance using:
- Constellation diagrams
- Time-domain audio waveforms
- Spectrogram analysis
- Signal-to-Noise Ratio (SNR)
- Mean Squared Error (MSE)
- Constellation spread metrics

Comparisons are made between:
- AWGN (baseline)
- Rayleigh fading (with and without channel estimation)
- Rician fading (with and without channel estimation)

---

## 📁 Project Structure

```text
communication/
│
├── ofdm_audio_main.m              # Main simulation script
├── README.md                      # Project documentation
├── original_audio.wav             # Original audio signal
├── received_awgn.wav              # Received audio (AWGN)
├── received_rayleigh_no_est.wav   # Rayleigh fading (no estimation)
├── received_rayleigh_with_est.wav # Rayleigh fading (with estimation)
├── received_rician_no_est.wav     # Rician fading (no estimation)
├── received_rician_with_est.wav   # Rician fading (with estimation)
├── constellation_diagrams.png
├── channel_estimation_comparison.png
├── audio_spectrograms.png
└── audio_quality_metrics.txt
