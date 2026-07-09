\# Simple RF Cartography Engine



\## Summary



This project implements a prototype RF cartography engine that combines software-defined radio, spectral estimation, camera-based visualization, machine learning classification, and embedded hardware–software integration.



The system uses an Analog Devices ADALM-PLUTO SDR with a directional Yagi-Uda antenna to capture RF activity around a 2.46 GHz center frequency. Captured I/Q samples are converted into power spectral density estimates using a manually implemented Welch PSD pipeline. The resulting spectral data is then visualized as a heatmap overlay on a live camera feed, allowing the operator to observe changes in RF activity within a visual region of interest.



This is an early-stage RF cartography prototype. The current implementation visualizes total spectral activity associated with a camera-frame region of interest; it does not yet perform triangulation, beamforming, or true spatial localization.



\## Motivation



RF environments are increasingly dense, mobile, and difficult to interpret visually. A practical RF cartography system would allow an operator or autonomous platform to associate radio-frequency activity with physical space, producing a useful interface for spectrum monitoring, interference detection, wireless diagnostics, and future autonomous sensing platforms.



This project explores the first stage of that idea: combining SDR-based sensing, PSD estimation, camera overlays, ML classification, and embedded data movement into a working prototype.



\## System Architecture



```text

RF Environment

&#x20;   ↓

Directional Antenna

&#x20;   ↓

ADALM-PLUTO SDR

&#x20;   ↓

I/Q Sample Capture

&#x20;   ↓

Welch PSD Estimation

&#x20;   ↓

PSD Vectorization

&#x20;   ↓

ML Signal Classification

&#x20;   ↓

Camera Frame Capture

&#x20;   ↓

Heatmap Overlay / ROI Visualization

&#x20;   ↓

Display Output

