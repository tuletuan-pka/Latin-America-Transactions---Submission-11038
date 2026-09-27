# Single-Layer High-Isolation Dual-Band MIMO Antenna for Sub-6 GHz 5G and WiFi Applications

**Submission ID:** 11038  
**Journal:** *IEEE Latin America Transactions* (Accepted)

[![IEEE Latin America Transactions](https://img.shields.io/badge/IEEE-Latin%20America%20Transactions-00629B.svg)](https://ieeexplore.ieee.org/)
[![Submission ID](https://img.shields.io/badge/Submission%20ID-11038-orange.svg)](#)
[![Status](https://img.shields.io/badge/Status-Accepted-success.svg)](#)
[![Simulation](https://img.shields.io/badge/CAD%20%2F%20EM-Ansys%20HFSS%20%28AEDT%29-red.svg)](https://www.ansys.com/products/electronics/ansys-hfss)
[![License](https://img.shields.io/badge/License-MIT%20%2F%20Academic-blue.svg)](#license)

---

## 👥 Authors & Affiliations

- **Yem Vu-Van** – *School of Electrical and Electronic Engineering, Hanoi University of Science and Technology (HUST), Hanoi, Vietnam*  
  Email: `yem.vuvan@hust.edu.vn`
- **Thao Hoang-Thi-Phuong** – *Faculty of Electronics and Telecommunications, Electric Power University (EPU), Hanoi, Vietnam*  
  Email: `thaohp@epu.edu.vn`
- **Quyen Nguyen-Xuan** – *School of Electrical and Electronic Engineering, Hanoi University of Science and Technology (HUST), Hanoi, Vietnam*  
  Email: `quyen.nguyenxuan@hust.edu.vn`
- **Cuong Do-Manh** *(Corresponding Author)* – *PHENIKAA School of Engineering, PHENIKAA University, Hanoi 12116, Vietnam*  
  Email: `duong.domanh@phenikaa-uni.edu.vn`

---

### 🌟 Key Highlights
- **Single-Layer & Low Profile:** Fabricated on Taconic RF-35 substrate ($\varepsilon_r = 3.5$, $\tan\delta = 0.0018$, thickness $t = 1.5\text{ mm}$), compact dimensions of $60 \times 30 \times 1.5\text{ mm}^3$ ($0.94\lambda \times 0.47\lambda \times 0.02\lambda$ at 4.6 GHz).
- **Independent Dual-Band Operation:** Sub-6 GHz n79 5G NR ($4.62 - 4.75\text{ GHz}$) and 5-GHz WLAN/WiFi ($5.50 - 5.72\text{ GHz}$).
- **Transmission Zero Decoupling:** Shorting vias act as reactive loading elements to bring even- and odd-mode reflection coefficients into equality ($\Gamma_e \approx \Gamma_o$), creating dual transmission zeros.
- **Superior Isolation:** Measured $29 - 43\text{ dB}$ (lower band) and $25 - 33\text{ dB}$ (upper band).
- **Excellent MIMO Diversity:** Envelope Correlation Coefficient ($\text{ECC} < 0.005$), Channel Capacity Loss ($\text{CCL} < 0.4\text{ bits/s/Hz}$), Mean Effective Gain ($\text{MEG} \approx -3\text{ dB}$), and $\text{TARC} < -10\text{ dB}$.

---

## 📊 Performance Summary

| Parameter | Lower Band (Sub-6 GHz 5G NR n79) | Upper Band (5-GHz WiFi / WLAN) |
| :--- | :---: | :---: |
| **Operating Frequency** | $4.62 - 4.75\text{ GHz}$ ($130\text{ MHz}$) | $5.50 - 5.72\text{ GHz}$ ($220\text{ MHz}$) |
| **Fractional Bandwidth** | $2.8\%$ | $3.9\%$ |
| **Port Isolation ($|S_{21}|$)** | $> 29\text{ dB}$ (Peak $43\text{ dB}$) | $> 25\text{ dB}$ (Peak $33\text{ dB}$) |
| **Peak Realized Gain** | $4.8 - 5.4\text{ dBi}$ | $5.2 - 6.8\text{ dBi}$ |
| **Radiation Efficiency** | $\approx 90\%$ | $\approx 90\%$ |
| **Envelope Correlation Coeff. (ECC)** | $< 0.005$ | $< 0.005$ |
| **Channel Capacity Loss (CCL)** | $< 0.4\text{ bits/s/Hz}$ | $< 0.4\text{ bits/s/Hz}$ |

---

## 📁 Repository Structure & Data Mapping

All figures and numerical evaluations presented in the paper can be reproduced using the datasets and model files in this repository:

```text
├── Final-LatinTrans - High-Isolation Dual-band MIMO.pdf   # Full accepted manuscript
├── Simulation File.aedt                                  # Complete Ansys HFSS / AEDT 3D simulation project
├── Figs. 1-3-4-6-9.txt                                    # Note on structural & field distribution figures in HFSS
│
├── Fig. 2.csv                                             # Simulated |S11| and realized gain of single-element dual-band antenna
├── Fig. 5.csv                                             # Simulated S-parameters (|S11|, |S21|) of coupled MIMO antenna
├── Fig. 7.csv                                             # Simulated S-parameters of decoupled MIMO antenna (Design 1)
├── Fig. 8.csv                                             # Parametric study on shorting via position (x-sweep) for Design 1
├── Fig. 10.csv                                            # Simulated S-parameters of final decoupled MIMO antenna (Design 2)
├── Fig. 11.csv                                            # Even- and odd-mode eigen-reflections (magnitude & phase)
├── Fig. 12.csv                                            # Parametric study on 2nd via set position (dv1_y) for Design 2
├── Fig. 14.csv                                            # Simulated vs. Measured S-parameters (|S11|, |S21|)
├── Fig. 15.csv                                            # Simulated vs. Measured realized gain across frequency
├── Fig. 16(a)z.csv                                        # 2D Radiation patterns (Phi & Theta cuts) at 4.64 GHz
├── Fig. 16(b).csv                                         # 2D Radiation patterns (Phi & Theta cuts) at 5.68 GHz
│
├── Fig. 17 - Simulated CCL.csv                            # Channel Capacity Loss (CCL) vs. Frequency
├── Fig. 17 - Simulated ECC.csv                            # Envelope Correlation Coefficient (ECC) vs. Frequency
├── Fig. 17 - Simulated MEG.csv                            # Mean Effective Gain (MEG1 & MEG2) vs. Frequency
└── Fig. 17 - Simulated TARC.csv                           # Total Active Reflection Coefficient (TARC) vs. Frequency
```

### Detailed File Descriptions

1. **`Simulation File.aedt`**:
   - Ansys Electronics Desktop (HFSS) project file containing:
     - 3D CAD modeling of the single-element patch antenna (Fig. 1).
     - Surface current distributions at 4.6 GHz and 5.6 GHz (Fig. 3).
     - Coupled 2-port MIMO antenna configuration (Fig. 4).
     - Decoupled MIMO Design 1 (Fig. 6) and final Decoupled MIMO Design 2 (Fig. 9).
     - Setup sweeps for S-parameters, far-field radiation patterns, and eigen-mode analysis.

2. **Decoupling Mechanism & Modal Analysis (`Fig. 11.csv`)**:
   - Contains raw numerical data for Even-mode ($\Gamma_e$) and Odd-mode ($\Gamma_o$) reflection coefficient magnitudes and phases:
     $$\Gamma_e = S_{11} + S_{21}, \quad \Gamma_o = S_{11} - S_{21}, \quad S_{21} = \frac{\Gamma_e - \Gamma_o}{2}$$
   - Demonstrates the transmission zero behavior where $\Gamma_e \approx \Gamma_o$ at 4.73 GHz and 5.75 GHz.

3. **Parametric Studies (`Fig. 8.csv`, `Fig. 12.csv`)**:
   - `Fig. 8.csv`: S-parameter response for shorting via displacement $x \in \{0.5, 2.5, 4.5, 6.5\}\text{ mm}$.
   - `Fig. 12.csv`: Upper-band $|S_{21}|$ response for second via set placement $dv1\_y \in \{2.5, 4.5\}\text{ mm}$.

4. **MIMO Diversity Metrics (`Fig. 17 - *.csv`)**:
   - Validates that the design complies with strict multi-antenna operational criteria:
     - **ECC:** $\le 0.005$ (well below the $0.5$ standard threshold).
     - **TARC:** $\le -10\text{ dB}$ across operating bands under arbitrary excitation phases.
     - **CCL:** $< 0.4\text{ bps/Hz}$ limit.
     - **MEG:** $|MEG_1 / MEG_2| \approx 0\text{ dB}$, with nominal values close to $-3\text{ dB}$.

---

## 💡 Acknowledgments

This research was funded and supported by the **Vietnam National Foundation for Science and Technology Development (NAFOSTED)** under Grant number **`102.04-2023.28`**.

---

## 📄 License

The datasets, simulation files, and documentation in this repository are released under the [MIT License](LICENSE) for open academic and research use.
