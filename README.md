
实现原理： 
核心是使用了heatmap.js这个库，这个库生成的热力图是用canvas绘制的，那么在Cesium中，我们只要将canvas转图片，当初材质贴到我们的对象上就行。其中Cesium加载热力图canvas生成的图片有两种方式，第一种是通过material来贴到entity或者geometry上，第二种是通过imageryprovider当作图层来加入，目前我这边以第一种方式来引入。

***
调用方法：
1、固定位置气泡窗：
```
new Heatmap(viewer, {
        list: list
    })
```
***
支持原heatmap.js的参数传参，具体可见src/js/heatmap.js类

