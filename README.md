# 2016 pPb 8 TeV ZDC calibration
* This git repo is meant for ZDC energy calibrations for pPb 2016 data.
* Run range is from 286178 to 286496, where the Pb is going to the ZDC- side.
* This producer produces the following items:
  * vector<double> ADC, raw ADC readout from ZDC (order-> -Side, EM1-5, HAD1-4, +side, EM1-5, HAD1-4).
  * vector<double> nominalfC, uncalibrated nominal fC (order-> -Side, EM1-5, HAD1-4, +side, EM1-5, HAD1-4).
  * vector<double> regularfC, calibrated regular fC (order-> -Side, EM1-5, HAD1-4, +side, EM1-5, HAD1-4).
  * double Sum, sum of EM and HAD energy from both ZDC+ and ZDC-
  * double SumP, sum of EM and HAD energy from ZDC+
  * double SumN, sum of EM and HAD energy from ZDC-
  * double emSumP, sum of EM energy from ZDC+
  * double emSumN, sum of EM energy from ZDC-
  * double hadSumP, sum of HAD energy from ZDC+
  * double hadSumP, sum of HAD energy from ZDC-
  * In principle, all vectors should contain 180 numbers (9 channels from each side, and 10 time slices per channel).
  * For unknown reasons, 20% of the ZDC digis are missing from the events. If that's the case, the vectors have less than 180 numbers, and the sum energies are set to -999. Please ignore those events in your analysis.
* An example python config is included in the test folder.
* Let me know if you have questions.
