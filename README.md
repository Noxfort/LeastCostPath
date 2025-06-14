## The Least Cost Path Plugin for QGIS


This algorithm finds the least cost path with given cost raster and points. 

![Interface](example/images/interface.png)
![Result](example/images/result.png)

Please ensure all the input layers have the same CRS.

 - Cost raster layer: Numeric raster layer that represents the cost of each spatial unit. It should not contains negative value. Pixel with `NoData` value represent it is unreachable.
 
 - Cost raster band: The input band of the cost raster.
 
 - Start-point layer: Layer that contains just one start point.
 
 - End-point(s) layer: Layer that contains the destination point(s).

 - Rivers cost raster layer (optional): An optional numeric raster layer that represents additional cost for rivers.

 - Rivers cost raster band (optional): The input band for the rivers cost raster.

 - Urban Perimeter cost raster layer (optional): An optional numeric raster layer. Areas with valid (non-NoData) values in this raster will be considered highly restrictive, and the path will avoid passing through them (making the cost infinite).

 - Urban Perimeter cost raster band (optional): The input band for the urban perimeter cost raster.

 - Vegetation cost raster layer (optional): An optional numeric raster layer that represents additional cost for vegetation.
 
 - Vegetation cost raster band (optional): The input band for the vegetation cost raster.
 
- Only connect with the nearest end points: If more than one destination are provided, it will find the least cost path to all the end points by default. If enabled, the least cost path will only connect start point with the nearest end point.

 - \[Optional\] Include liner referencing (PolylineM type): If selected, this algorithm will output the least cost path in `PolylineM` type, with the accumulated cost as linear referencing value.
 
 
**Contributors:**

@gjx-123, @ClaireXing, @GXIU, @Shangss, @Gooong
