# img2stamps
<pre>
The idea here is to take an image, photo or camera stream to generate a 3D printable stamp.

In linux Mint / Ubuntu:
sudo apt update
sudo apt install python3-opencv python3-numpy python3-pil python3-tk openscad


in a virtual enviornment, or on some non linux OS install with:
pip install opencv-python pillow numpy 

depends on openscad, I'd reccomend a nightly build, with manifold rendering selected.
Once you generate an output.scad I reccomend leaving openscad open to re-render. 


Beware large images may take a long time to render,
or require editing the scaling value DOWNSCALE
DOWNSCALE basicly chooses the square of the number of impage pixels
to render as a single cube. 

looks like a started writing a gui at one point. 

Example Usage:

$ ./img2stamps.py 
Usage: ./img2stamps.py [-c] [-n] [imagefile.png]
  -c : Capture from camera
  -n : Invert highs and lows
  Default file 't.png' not found.

./img2stamps.py  b.png 
Original image size: 268 x 278
Done. Output written to: output.scad

./img2stamps.py -n b.png 
Original image size: 268 x 278
Done. Output written to: output.scad

when you are satisfied, export you scad file to stl or whatever, to 3D print it. 


<img src="https://github.com/FOSSBOSS/img2stamps/blob/main/imgs/aaa.png">
<br>
same image inverted:
<br>
<img src="https://github.com/FOSSBOSS/img2stamps/blob/main/imgs/bb.png">





</pre>
