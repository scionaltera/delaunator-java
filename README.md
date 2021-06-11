[![](https://jitpack.io/v/waveware4ai/delaunator-java.svg)](https://jitpack.io/#waveware4ai/delaunator-java)
![](https://codebuild.us-west-2.amazonaws.com/badges?uuid=eyJlbmNyeXB0ZWREYXRhIjoieG1tN3c4ZFZ5eC9CS0EvQ2tFbGxyYUZEVVYwdDV5UWI1dlRxQVpVN21hd3lmSXg1SjRHbk1DSWcvM1VFbzFGSlBqQjI5cmc1M3NOVy9jbFErbUpra2pFPSIsIml2UGFyYW1ldGVyU3BlYyI6IkxZK1c0NzJWYTUwTGczejkiLCJtYXRlcmlhbFNldFNlcmlhbCI6MX0%3D&branch=main)  


# delaunator-java

This library is Java port of [*Delaunator*](https://github.com/mapbox/delaunator), an incredibly fast and robust JavaScript library for Delaunay triangulation of 2D points.

The port was produced by referring to the c++ and c# versions of *Delaunator*.
<p float="middle">
    <img src="resources\delaunator.example.png" alt="delaunay example" width="49.5%"/>
    <img src="resources\delaunator.voronoi.example.png" alt="delaunay example" width="49.5%"/></p>
</p>

## Example

```
List<DPoint> list = new ArrayList<>();
for (int i = 0; i < 10000; i++) {
	double x = Math.random() * 1000;
	double y = Math.random() * 1000;
	DPoint p = new DPoint((int) x, (int) y);
	list.add(p);
}

Delaunator del = new Delaunator(list);
for (DTriangle t : del.getTriangles()) {
	DEdge edgeA = t.ab; // edge A of Tri
	DEdge edgeB = t.bc; // edge B of Tri
	DEdge edgeC = t.ca; // edge C of Tri
	DTriangle[] wingA = edgeA.getWing(); // wing A0, A1 of edge A
	DTriangle[] wingB = edgeB.getWing(); // wing B0, B1 of edge B
	DTriangle[] wingC = edgeC.getWing(); // wing C0, C1 of edge C
}
```
## Ports to other languages

- [delaunator-rs](https://github.com/mourner/delaunator-rs) (Rust)
- [fogleman/delaunay](https://github.com/fogleman/delaunay) (Go)
- [delaunator-cpp](https://github.com/abellgithub/delaunator-cpp) (C++)
- [delaunator-sharp](https://github.com/nol1fe/delaunator-sharp) (C#)
- [delaunator-ruby](https://github.com/hendrixfan/delaunator-ruby) (Ruby)
- [Delaunator-Python](https://github.com/HakanSeven12/Delaunator-Python) (Python)
- [hx-delaunator](https://github.com/dmitryhryppa/hx-delaunator) (Haxe)
- [ricardomatias/delaunator](https://github.com/ricardomatias/delaunator) (Kotlin)
