![theundebruijn](theundebruijn_853x480_50fps_0008.gif)  
<sub><sup>_a quick conversion trick to optimise gif filesize using temp transparency_  
\# convert 8 bit rgba .tiff's to 256 colorspace gifs (alpha to rgb black)  
`ffmpeg -framerate 50 -i %04d.tif -loop 0 output.gif`  
\# we now replace the exact black and introduce a new background color — this is much more efficient than preserving a flat color from the original .tiff output  
`gifsicle -U --disposal=previous --change-color="#000000" "#FCD137" -O2 output.gif > output_gifsicle.gif`</sup></sub>  
