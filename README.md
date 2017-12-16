# song-bpm-detector

The code determines how many beats per minute are in a song 
using a list of frequencies that must be provided by a text file, converted from a WAVE file, in the command line.

The algorithm to determine the beats per minute were provided
by Marco Ziccardi. His beat detection algorithm can be found
here: 
(http://mziccard.me/2015/05/28/beats-detection-algorithms-1/)

The major difference between his code and this project's is
that the algorithm is optimized by running on a GPU. In the
gpubpm.cu file that I coded, the frequencies are sent to the
GPU and then the massive addition of frequencies is performed
there. The calculated energies of all blocks in the song are 
then sent back to the CPU to finalize the algorithm.
