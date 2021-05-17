# geojson

> geojson 地图数据学习
> 基本结构
    { // 可以包括点线面, 一个大的集合
        "type": "FeatureCollection", // 定义这个是个geojson文件, 这里还可以是其他值下面会说
        "features": [] // 这里放要绘制的数据
    }
> 描述多个点(FeatureCollection)
    {
        "type": "FeatureCollection",
        "features": [
                {
                "type": "Feature",
                "properties": {},
                "geometry": {
                    "type": "MultiPoint", // 多点, 也就是连续画多个同样的点
                    "coordinates": [[105.380859375, 31.57853542647338],
                        [105.580859375, 31.52853542647338]
                    ]
                }
            },
        ]
    }
> 描述一条线(LineString)，多个点会连在一起形成一条线
> 描述一个面(Polygon, 也叫多边形)
    {
        "type": "FeatureCollection",
        "features": [
            {
                "type": "Feature",
                "properties": {},
                "geometry": {
                    "type": "Polygon", // 注意这里是三维数组
                    "coordinates": [
                        [
                            [106.10595703125, 33.33970700424026],
                            [106.32568359375, 32.41706632846282],
                            [108.03955078125, 32.2313896627376],
                            [108.25927734375, 33.15594830078649],
                            [106.10595703125, 33.33970700424026]
                        ]
                    ]
                }
            },
        ]
    }
> 描述一个组(geometries)
{
    "type": "FeatureCollection",
    "features": [
        { // 可以包括点线面, 一个独立的集合
            "type": "GeometryCollection",
            "geometries": [
                {
                    "type": "Point",
                    "coordinates": [108.62, 31.02819]
                }, {
                "type": "LineString",
                "coordinates": [[108.896484375, 30.1071178870],
                    [108.2184375, 30.91717870],
                    [109.5184375, 31.2175780]]
                }
            ]
        }
    ]
}
> 不同的样式(properties)
{
    "type": "FeatureCollection",
    "features": [
        {
            "type": "Feature",
            "properties": { // 专门放属性
                "stroke": "#fa9661", // 外边颜色
                "stroke-width": 4.1, // 外边宽
                "stroke-opacity": 0.7, // 外边透明度
                "fill": "#9e290c",  // 填充色
                "fill-opacity": 0.7 // 填充色透明度
            },
            "geometry": {
                "type": "Point",  // 画点
                "coordinates": [105.380859375, 31.57853542647338]
            }
        }
    ]
}


## Build Setup
``` 教程地址
``` 

详情请看 [geojson-基础绘制属性解析](https://segmentfault.com/a/1190000037611134/).
