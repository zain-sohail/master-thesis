# From Noisy Data to Scientific Insights

![noisy_target_denoised](https://github.com/user-attachments/assets/ac778208-6c03-4f5b-a534-6f2bd91aae28)

My thesis work tackled the challenge of making sense of extremely noisy ♦︎, high-dimensional data from multidimensional photoemission spectroscopy (MPES), covering statistical and physical  understanding of the measurement process to developing a state-of-the-art denoising schemes.

## What I Did

-	**Wrangling Raw Data**: Started with raw single-event MPES datasets, creating multidimensional images of different noise levels.
-	**Statistical Analysis**: Characterized the electron counting statistics and the correction of the double (and multi-hit) counting from the detector (using a kNN-based scheme).
-	**Exploring Classical Methods**: Tested BM3D with variance stabilization (via the Anscombe transform) for moderately noisy datasets. It works great, but only at lower noise levels.
-	**Dataset Design**: Using only a single (less) noisy dataset, designed training and validation sets.
-	**Deep Learning**: Trained a 3D U-Net model using Noise2Noise, successfully denoising images in the ultra-low-count regimes where traditional methods give up.
-	**Real-World Validation**: Put everything to the test by running inference on new data, proving that the model could reveal features in 10 minutes that would take hours of conventional acquisition to capture.

<div style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/b1ef68d1-8c0c-4e55-a6bb-f98ff5d2c6b1" alt="same_energy_3d_cylinder" width="400" />
  <p><em>Simplified visualization of electron events on the 3D delay-line detector as a function of time. These events are binned to form images. In this setup, thousands of electrons might be detected every second. In laser based setups, this can go up to millions.</em></p>
</div>


## Why It Matters

This work solves a real problem: saving time and resources at some of the world’s most advanced research facilities, such as the free-electron lasers FLASH. By optimizing data acquisition, researchers can focus on exploring new physics instead of waiting around for their data to converge.

♦︎ While some physicists might disagree on the term 'noise' since the measurment process is inherently probabilistic, but these inherent fluctuations is how it is defined within this work.
