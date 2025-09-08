# make-a-3D-triangle-basically-a-polygon-with-3-vertices-and-show-it-in-Figure-1-using-Python.
This Python code uses matplotlib to plot a 3D triangle on Figure 1. It defines three vertices in 3D space, connects them to form a polygon, and displays it with cyan fill and red edges for visualization.
Install matplotlib
pip install matplotlib

Create a new file, e.g. triangle3d.py.

Paste this code into the file:

import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d.art3d import Poly3DCollection

fig = plt.figure(1)
ax = fig.add_subplot(111, projection='3d')

vertices = [[0,0,0],[1,0,0],[0,1,1]]
triangle = [vertices]
ax.add_collection3d(Poly3DCollection(triangle, facecolors='cyan', linewidths=1, edgecolors='r', alpha=0.7))

ax.set_xlim(-1,2); ax.set_ylim(-1,2); ax.set_zlim(-1,2)
plt.show()


Run the script: python triangle3d.py (or run the cell in Jupyter).

See Figure 1 pop up showing the 3D triangle.

To change the triangle shape — edit the three vertices coordinates.

To save the figure instead of showing: add plt.savefig('triangle.png', dpi=200) before plt.show().

(Optional, Jupyter) use %matplotlib notebook for interactive rotation.

Want the steps in Bangla or a version that makes a filled triangular pyramid instead?
