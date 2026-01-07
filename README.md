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

<img src="https://github.com/FOSSBOSS/img2stamps/blob/main/imgs/aaa.png">
<br>
same image inverted:
<br>
<img src="https://github.com/FOSSBOSS/img2stamps/blob/main/imgs/bb.png">


# 2026: Openscad build supports multi-color export 3MF
<pre>
  This means  we can output colors to scad models which is very interesting. 
$openscad s.scad -o s.3mf
Geometries in cache: 1
Geometry cache size in bytes: 439384
CGAL Polyhedrons in cache: 0
CGAL cache size in bytes: 0
Total rendering time: 0:00:00.159
Top level object is a 3D object (PolySet):
   Convex:       yes
   Facets:      4902


More testing still needed.  
</pre>
