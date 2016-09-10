# 百度地图 JS插件 v2.0.3
###安装：npm install TopuNet-BaiduMap

文件结构：
-------------
        1. jq/baidu_map.js 放入项目文件夹jq（原生规范）或widget/lib（AMD规范）中
        2. inc中的样式文件 放入项目文件夹inc中

页面引用：
-------------
原生引用

        1. 页面底端引用 http://api.map.baidu.com/api?v=2.0&ak=cQoqZZ4o1Yy96sEiIlIVkkek
        2. 后引用最新版 /inc/Jquery.min.js#1.x.x
        3. 后引用 /jq/baidu_map.js

requireJS引用

        依赖baidu_map.js和jquery.min.js#1.x，成功后返回对象baidu_map

功能配置及启用：
--------------
1. 调用方法：

        var baidu_map_para = {
            map_obj_id: "baidu_map", // 地图容器ID。无默认值。
            enableScrollWheelZoom: false, // 允许滚轮缩放。默认值：true
            NavigationControl: true, // 左上角缩放尺。默认值：true
            ScaleControl: false, // 左下角比例尺。默认值：true
            OverviewMapControl: false, // 右下角小地图：true
            CurrentCity: "北京", // 当前城市。默认值：北京
            MapTypeControl: true, // 右上角地图种类，仅当设置当前城市后可用。默认值：true
            PointKeywords: "盈科中心 北京市朝阳区工人体育场北路甲2号", // 定点标注搜索。无默认值
            PointBounce: true, // 定点标注跳动。默认值：true
            PointClick: function(e) {}, // 定点标注点击回调。无默认值。
            // SearchKeywords: "礼士宾馆", // 搜索关键词。无默认值
            Zoom: 16 // 默认缩放比例。默认值：16
        }

        baidu_map.init(baidu_map_para);

2. 在 jq/baidu_map.js line 41 可修改配套样式表路径


更新日志：
-------------
v2.0.3

        1. 通过jshint验证

v2.0.2

        1. 在dist文件夹中，增加package.json
        2. 将dist发布到npm：TopuNet-BaiduMap

v2.0.1

        1. 兼容原生JS和AMD规范
        2. 修改demo

v1.1.1

        1. 加入样式文件，重写部分样式（和公司通用样式有冲突）
        