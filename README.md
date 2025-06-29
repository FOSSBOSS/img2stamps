# img2stamps
<pre>
The idea here is to take an image, photo or camera stream to generate a 3D printable stamp.

python pkgs:
pip install opencv-python pillow numpy

Beware large images may take a long time to render.
depends on openscad, I'd reccomend a nightly build, with manifold rendering selected.
Once you generate an output.scad I reccomend leaving openscad open to re-render. 


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

<pre>
