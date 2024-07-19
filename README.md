# A Median-Based Approach for Robust Parameter Estimation in Anomalous Diffusion Analysis

## Team: Unfriendly AI

### Team Members:
- Roman Lavrynenko (Kharkiv National University of Radio Electronics)
- Lyudmyla Kirichenko (Lodz University of Technology)
- Sophia Lavrynenko (Kharkiv National University of Radio Electronics)

### Contact:
- **Team Leader:** Roman Lavrynenko
- **Email:** [roman.lavrynenko.cpe@nure.ua](mailto:roman.lavrynenko.cpe@nure.ua)

### Method Description:
Our approach focuses on robust parameter estimation in anomalous diffusion analysis using a median-based technique. Below is a detailed description of our method:

#### Key Points:
1. **Two-Dimensional Fractional Brownian Motion:**
   - The displacement components (Δx and Δy) are independent and identically Gaussian distributed.
   - The square of the resulting displacement (Δr²) follows a chi-squared distribution with 2 degrees of freedom, equivalent to an exponential distribution.

2. **Statistical Testing:**
   - Utilizing the Anderson-Darling test to determine if trajectory points sample from a single distribution.
   - This is applied for model determination and segmenting trajectories with different dynamics.

3. **Sliding Window Method:**
   - Temporal boundaries of segments are identified using a sliding window method.
   - Both mean and median of Δr² are calculated in each window. Medians, being less affected by outliers, offer clearer detection of dynamic changes.

4. **Median Usage:**
   - Medians resist outliers, providing more reliable results when determining diffusion coefficient K.
   - Transitioning from mean square displacement to median square displacement improves reliability in the presence of outliers.

5. **Determining Diffusion Exponent (α):**
   - Using the formula MSD(t) = 4Kt^α and transitioning to median square displacement for higher reliability.
   - The exponent α is derived using:
     ```
     α = log(MSD(n · Δt) / MSD(Δt)) / log(n)
     ```

#### Models Used:
- **Single-State Model (SSM):** Based on the Anderson-Darling test for trajectories over time units.
- **Multi-State Model (MSM):** Default model if no other affiliation is determined. Division is based on histogram peaks.
- **Dimerization Model (DIM):** Histogram-based division depending on particle distances.
- **Transient-Confinement Model (TCM):** Uses circles of certain radius for division based on largest and smallest displacements.
- **Quenched-Trap Model (QTM):** Based on histograms with two peaks, division at the minimum between the peaks.

### Publication Interest:
- **Special Issue:** Yes
- **Publication Date:** 10.08.2024

### Additional Information:
- **Twitter:** [Sophia Lavrynenko](https://x.com/Waifu05250596)
