# OrcaSound
 Orclassifier


The Sound Filtration is used to filter out the unwanted noise present in the audio data. The procedure used here to filter out the noise has been described in the next few points.
1. An FFT is calculated over the noise audio clip
2. Statistics are calculated over FFT of the the noise (in frequency)
3. A threshold is calculated based upon the statistics of the noise (and the desired sensitivity of the algorithm)
4. An FFT is calculated over the signal
5. A mask is determined by comparing the signal FFT to the threshold
6. The mask is smoothed with a filter over frequency and time
7. The mask is applied to the FFT of the signal, and is inverted

More details on the methodology and the code can be found here, https://github.com/timsainb/noisereduce.
