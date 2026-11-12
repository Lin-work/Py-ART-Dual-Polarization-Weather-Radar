# Py-ART-Dual-Polarization-Weather-Radar

This project analyzes the microphysical and kinematic structures of an approaching frontal system using C-band/S-band dual-polarization Doppler radar observations. By leveraging `Py-ART`, multi-parameter radar fields were extracted, visualized, and evaluated across both Plan Position Indicator (PPI) and Range Height Indicator (RHI) / Quasi-Vertical Profile (QVP) cross-sections to identify convective organization, hydrometeor phase transitions, and melting layer signatures.

---

## 1. Multi-Parameter Polarimetric Analysis (PPI Scan)

*Case Date/Time: 26 March 2022, 15:41 UTC*

### Key Meteorological & Microphysical Findings:
* **Reflectivity ($Z_{HH}$):** Distinct high-reflectivity linear bands are observed northwest of the radar site. The leading intense, narrow line represents a **Narrow Cold-Frontal Rainband (NCFR)**, trailed by a broader stratiform/convective region consistent with a **Wide Cold-Frontal Rainband (WCFR)**.
* **Differential Reflectivity ($Z_{DR}$):** Elevated $Z_{DR}$ values ($> 1\text{ dB}$) collocated with the high-$Z_{HH}$ core confirm liquid precipitation dominated by large, oblate raindrops.
* **Differential Phase ($\Phi_{DP}$):** A distinct propagation phase shift is visible across the rainband—transitioning from $\sim 80^\circ$ ahead of the band to $\sim 50^\circ$ behind it—signifying heavy liquid water path and active attenuation/phase accumulation along the radar beam.
* **Correlation Coefficient ($\rho_{HV}$):** Consistently high values ($> 0.90$) across the domain indicate homogeneous liquid hydrometeors, with localized drops northeast of the radar suggesting mixed-phase particles or non-meteorological echoes.
* **Radial Velocity ($V_r$) & Spectrum Width ($SW$):** $V_r$ demonstrates strong low-level convergence, with southwesterly flow inbound toward the radar and localized outbound flow to the northeast. Low $SW$ values across the stratiform region indicate relatively weak sub-beam wind shear and turbulence.

---

## 2. Vertical Structure & Bright Band Detection (Unfiltered RHI / Azimuthal Cross-Section)

### Signal Processing & Structural Observations:
* **Unfiltered Clutter vs. Meteorological Signal:** Deliberately bypassing `pyart.correct.GateFilter` preserves raw radar returns, illustrating the presence of ground clutter and non-meteorological noise alongside true precipitation echoes.
* **Melting Layer (Bright Band) Signature:** Despite the unfiltered noise floor, a pronounced horizontal layer of enhanced reflectivity is clearly identifiable at **$\sim 4\text{ km}$ altitude along the $300^\circ$ azimuth**, marking the **Bright Band** where falling ice aggregates melt and become coated in liquid water.
* **Spatial Extent:** Peak convective intensity is concentrated within the **$270^\circ\text{--}300^\circ$ azimuthal sector**, with the primary frontal rainband situated within a **$100\text{ km}$ range** from the radar site.
