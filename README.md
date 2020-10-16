# apollo-shoulders
Standing on Apollo's Shoulders: a Microseismometer for the Moon - Electronic Supplement

Seismometers deployed on the Moon by the Apollo astronauts from 1969 to 1972 detected moonquakes and impacts and added to our understanding of the lunar interior. Several lunar missions are currently being planned, including the Commercial Lunar Payload Services (CLPS), the Lunar Geophysical Network (LGN) and the astronaut program Artemis. We propose a microseismometer for the Moon: the Silicon Seismic Package (SSP). The SSP's sensors are etched in silicon, and are predicted to have a noise floor below 2e-10 (m/s)^2)/Hz^(1/2) between 0.3 and 3 Hz (similar to the Apollo instruments between 0.3 and 0.5 Hz, and better than Apollo above 0.5 Hz). The SSP will measure horizontal and vertical motion with the three sensors in a triaxial configuration, is robust to high shock and vibration, has an operational range from -80 C to +60 C, allowing deployment under harsh conditions. The first-generation version of this sensor, the SEIS-SP, was deployed on Mars in 2018 as part of the InSight mission's seismic package. We will reconfigure the seismometer for the lower gravity of the Moon. We estimate that a single SSP instrument operating for one year would detect around 74 events above a signal-to-noise ratio of 2.5, as well as an additional 500+ above the noise floor. A mission lasting from lunar dawn until dusk, carried on a CLPS lander, could test the instrument in-situ, and provide invaluable information for an extensive future network.

Nunn, Ceri; Pike, William T.; Standley, Ian M.; Calcutt, Simon B.; Kedar, Sharon; Panning, Mark P.

This Electronic Supplement contains python notebooks to reproduce the figures in this paper, including the parameters and equations used to produce the figures in the paper. It also contains example signals and noise from the Moon and Mars, and other background information. 

**** Note, if you have trouble browsing the Jupyter notebooks, use the free site nbviewer, and copy and paste the url of the 
notebook into a browser: 
https://nbviewer.jupyter.org/github/cerinunn/apollo-shoulders/blob/master/plot_seismometer_noise.ipynb
https://nbviewer.jupyter.org/github/cerinunn/apollo-shoulders/blob/master/make_and_check_catalogs.ipynb	
https://nbviewer.jupyter.org/github/cerinunn/apollo-shoulders/blob/master/plot_histograms.ipynb
https://nbviewer.jupyter.org/github/cerinunn/apollo-shoulders/blob/master/make_tmp_catalogs.ipynb
*****

-apollo-shoulders: 

  -plot_seismometer_noise.ipynb
  * notebook containing a) parameters and equations to estimate the noise floor of the SP seismometer (for Mars) and the SSP seismometer (for the Moon); and b) spectra of events and noise recorded by the Apollo seismometers. *
  note that this notebook takes a long time to run
  paramter ppsd_hours=24*28 (calculate noise over a 28 day period) 
  for non final versions of the figures, set this parameter much lower (not less than =1)

  -make_and_check_catalogs.ipynb	
  * notebook to view the seismomgrams, view removing the instrument response, and make and view the power spectral density plots (ppsd) *
  contains example seismograms 

  -plot_histograms.ipynb
  * plot various histograms of catalog events

  -make_tmp_catalogs.ipynb	

  -files
  * useful files, including Nakamura (1981) catalog * 
  
  -plots
  * output plots * 
  
  - tmp_Nakamura_npz
  * temporary npz files from full Nakamura catalog for power density plots * 
  
  - tmp_catalogs
  * temporary catalogs for easier handling of the histograms *
  
  - tmp_npz
  * temporary npz files from selected events for power density plots * 
  
  - tmp_selected_events
  * lists of selected events * 

Make the following figures from the paper: 

-plot_seismometer_noise.ipynb
  SP_Mars.pdf
  SSP_Sensor_Noise.pdf 
  SSP_Noise_Fig5.pdf
  LowNoise.pdf
    made of the following figures:
    Apollo_noise_10.pdf
    Apollo_noise_90.pdf
    XA.S14..MHZExample_of_10th_percentile_noise.pdf
    XA.S14..MHZExample_of_90th_percentile_noise.pdf
    XA.S15..MHZExample_of_10th_percentile_noise.pdf
    XA.S15..MHZExample_of_90th_percentile_noise.pdf

-plot_histograms.ipynb
  cumulative_count_S12.pdf
