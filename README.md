# VVR-Framework

## Geometric classes
| Library | Details | Use |
|--|--|--|
| **VVRFramework** | Namespace _vvr_ <br> e.g. vvr::Point2D | For rendering. <br>All classes inherit IRenderable and thus <br>have a draw method. This method only <br>works if called from within Scene::draw. <br>Otherwise it produces no effect. |
|**GeoLib**|TNot in any namespace. <br>Classes name starts with C2D. <br>e.g. C2DPoint|For 2D geometric operations.|
|**MathGeolib**|Namespace _math_ <br>e.g. math::float3|For 3D geometric operations.|

## Facilitation classes and methods
| Class/Method | Use |
|--|--|
| class vvr::**Canvas** | Class used to aggregate pointers from multiple <br> geometry objects in the vvr library. With one call <br> of draw it renders all the objects it contains. |
| void vvr::Canvas::**add**(Shape*) | The method of the Canvas class with which we add <br> a geometric shape. The pointer it accepts as a parameter <br> must point to an object we have already created with new. |
| void vvr::Canvas::**add**(C2DXXX) | Series of methods that exist for convenience in case we want<br>  to add to a Canvas, some object that we have in the form of a<br>  GeoLib class. The conversion from GeoLib to vvr is done automatically.  |
| vvr::xxx **math2vvr**(math::xxx) | Series of methods that convert objects from MathGeoLib to vvr. |
| **draw**(C2DPointSet) | Function to plot a set of points. |
| **draw**(C2DLineSet) | Function to visualize a set of line segments. |
| **draw**(C2DPolygon) | Function to plot a polygon. |

