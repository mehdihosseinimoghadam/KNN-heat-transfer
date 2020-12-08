# KNN heat transfer
AN easy implementation of heat transfer for point cloud data with out any need to solve the heat equation, just using the KNN algorithms.
This can be used in Data science, computational geometry (e.g. [Vector Heat Method](https://www.cs.cmu.edu/~kmcrane/Projects/VectorHeatMethod/paper.pdf)
 ) and mechanical engineering.
 
 ```python
 ##import your point cloud data
 
plydata = PlyData.read("./bun_zipper_res2.ply")
point = np.vstack((
    plydata['vertex']['x'],
    plydata['vertex']['y'],
    plydata['vertex']['z']
)).T
 
 
## feed point cloud to diffuse function

points = pd.DataFrame(point)
(data,indices) = diffuse(points,1,70,10)
 
 ````
 
 
 ![Heated](heat.gif?raw=true "Title")
 
