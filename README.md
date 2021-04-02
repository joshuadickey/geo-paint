# geo-paint

GEOPHYSICAL SIGNAL IN-PAINTING:

Geophysical sensor data is fundamental for AFTAC’s nuclear treaty monitoring mission. Our global sensor grid provides near-real time waveforms from air land and sea with over 98% data availability. However, this data can sometimes suffer corruption for short periods of time, due to digital artifacts, communications interruptions, sensor self-noise, or even natural molestation of the sensor. These short period spikes and data gaps are problematic for AFTAC’s processing algorithms, as the corrupted waveforms can include discontinuities which wreak havoc on downstream filtering. This project proposes a deep neural network methodology for removing and replacing these corrupted waveforms and data gaps with smooth natural signal. The project will borrow from recent state-of-the-art research in image and audio in-painting, and the algorithm will be formulated as a sequence-to-sequence model, where an uncorrupted gapless sequence is supplied as a label and a corrupted, gap-filled version of the same sequence is supplied as an input. Under this training regime, data is both readily available and virtually unlimited… any healthy segment of seismic, hydro-acoustic or infrasound data can be utilized. The model will be optimized based on a joint loss function. The first loss function focuses on signal reconstruction, using mean squared error loss to regress on the original signal data that was removed. The second loss function focuses on signal continuity, seeking to preserve the natural smoothness of the sample space through implementation of a generative adversarial network (GAN). This project fills an important need for both AFTAC and the broader geophysical scientific community.
