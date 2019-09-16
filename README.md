# Kaixo-Vicomtech
GitHub-en repositorioak sortzen

#Puntu bat eremu konbexu baten barruan dago? true=bai, false=ez

from shapely.geometry import Point, Polygon
polygon = Polygon([(0, 0), (1, 1), (1, 0)])
# boundary of the polygon = LinearRing
linearring = LinearRing(list(polygon.exterior.coords))
print linearring
LINEARRING (0 0, 1 1, 1 0, 0 0)
# contains
polygon.contains(linearring)
# a vertex 
point = Point(1,1)
polygon.contains(point)

#to check vertex points
polygon.touches(linearring)
polygon.touches(point)
polygon.intersect(linearring)
polygon.intersect(point)
