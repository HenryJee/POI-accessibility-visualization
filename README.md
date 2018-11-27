# POI-accessibility-visualization
Visualization of the accessibility of POI, emergency room here as example
This small project aims to analyze how hospitals in Shenzhen, China is serving the cities, and how available and accessible they are by the urban residents.

Tools: Rhino + Grasshopper + Depthmap X + GHPython

We are using OpenStreetMap data as road data resource and using Python 3.7 beautifulsoup+requests to get POI (the geolocation of all the hospitals in Shenzhen) data from Baidu Map. Data from Baidu Map is a GCJ-02 system rather than WSG-84 geo-coding system, which is more commonly used by Google and other scholars. Also, GCJ-02 geolocating system is encrypted under the government demand but cracked and published. We wrote a Piece of GHPython code to convert the big geolocation data that we have scrapped into WSG-84 geo-code, which can be imported into Rhino and coordinates with OpenStreetMap data.

The connectivity data is generated using Depthmap X software,which is also C++ open-sourced on Github at https://varoudis.github.io/depthmapX/

The serving range (1km 3km 5km) is generated using Python and grasshopper in Rhino. Algorithm is written all by myself.


Credit: https://github.com/wandergis/coordTransform_py

https://varoudis.github.io/depthmapX/

http://lbsyun.baidu.com/index.php?title=androidsdk/guide/retrieval
