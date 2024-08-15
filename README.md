# FFT-for-accurate-compression of tidal data, and for available energy estimations
This repository contains code which performs FFT-based compression and decompression of Telemac-2D model output datasets. It can be used to compress the Telemac-2D data in spectral form with a higher level of reconstruction accuracy relative to harmonic analysis. Can also be used to forecast annual energy estmations with a higher degree of accuracy than harmonic analysis due to its ability to identify any non-celestial periodicity within the non-tidal component of the tidal signal. Works best when a year of model data is provided for efficient elucidation of frequencies. Need OCMW environment in order for code to work.
The decomposition file splits the tidal signal for each node into tidal, high frequency and low frequency components before reforming them as arrays.
FFT_Compression_step performs FFT of the signals and has an adaptable thresholds to retain X% of FFT coefficients based on magnitude. They are saved as a .pkl file
IFFT_Decompression reconstructs the time series at a specified time using the retained frequencies
