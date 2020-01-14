WPC DCS / DSP Notes
---------

### DCS specifications

[From "Ask Uncle Willy" #3: July 7, 1995](http://www.planetarypinball.com/mm5/Williams/archives/willy3.htm)

* Mono
* 16 bit
* 32Khz sample rate (mentioned as 31,250 samples per / seems wrong - wth?) 

"Frames" are 240 samples long (with 8 samples of overlap on each end for 256 samples and 256 FFT bins)

### Encoding / Compression process

* Digital Audio File as input / source data
* "fields" are broken down into "frames" of 240 samples each
* one "frame" is 7.68ms of audio
* each "frame" is transformed by a 256-point FFT
    * with simple COSINE windowing...
    * ...and 8 samples fo overlap on each end
* RESULTING SPECTRUM is further broken down into **16 bands** and **QUANTIZED** according to:  
    * ...MASKING-CURVES 
    * ...and USER-CONTROLLED PARAMETERS
* QUANTIZING LEVELS and resulting data for each "frame" 
    * ...are ENTROPY ENCODED 
    * ...into VARIABLE-LENGTH packets
* PACKETS for each file are:
    * ...combined with HEADER BLOCKS 
    * ...and stored as files that are later used to generate ROM images


### Decoding / De-compression process

* takes place on DSP chip
    * HEADER + PACKET of compressed data is read from ROM
    * ...and DE-COMPRESSED into a "frame"
    * ...via ENTROPY DECODING of data stream 
    * ...and DE-QUANTIZING into FRAME of FREQUENCY DOMAIN data
    * ...VOLUME LEVELm x-FADE etc. also done in FREQUENCY DOMAIN
    * ...resulting frame is INVERSE-TRANSFORMED into TIME DOMAIN and serial-clocked to DAC
    
### DFT vs. DCT 

[StackExchange](https://dsp.stackexchange.com/questions/13/what-is-the-difference-between-a-fourier-transform-and-a-cosine-transform)

> The Discrete Fourier Transform (DFT) and Discrete Cosine Transform (DCT) perform similar functions: 
they both decompose a finite-length discrete-time vector into a sum of scaled-and-shifted basis functions. 
The difference between the two is the type of basis function used by each transform; 
the DFT uses a set of harmonically-related complex exponential functions, 
while the DCT uses only (real-valued) cosine functions.

> The DFT is widely used for general spectral analysis applications that find their way into a range of fields. 
It is also used as a building block for techniques that take advantage of properties of signals' frequency-domain 
representation, such as the overlap-save and overlap-add fast convolution algorithms.

> The DCT is frequently used in lossy data compression applications, such as the JPEG image format. The property 
of the DCT that makes it quite suitable for compression is its high degree of "spectral compaction;" at a qualitative 
level, a signal's DCT representation tends to have more of its energy concentrated in a small number of coefficients
when compared to other transforms like the DFT. This is desirable for a compression algorithm; if you can approximately 
represent the original (time- or spatial-domain) signal using a relatively small set of DCT coefficients, then you can 
reduce your data storage requirement by only storing the DCT outputs that contain significant amounts of energy.


