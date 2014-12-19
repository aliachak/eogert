eogert
======

EOGERT - EOG Event Recognizer Tool

Eogert is a probabilistic online method for detecting fixations, saccades, and blinks from EOG signal.
This implementation is written in Matlab and it uses normpdf routine, found in the statistics toolbox; if your don't have it, don't bother to buy it but just make your own with 

norm_pdf = exp(-0.5 * ((x - mu)./sigma).^2) ./ (sqrt(2*pi) .* sigma).

The main file is *eogert.m* which calls *EMgauss1D.m*. In the current code, the EOG signals are loaded from the *TEST001.mat* file which must therefore also exist in the same folder 
and the signals are read "realtime" from the loaded files. Modify the corresponding code to read the signals over some actual stream (such as socket).

