### 高德地图定位插件（IOS、ANDROID）
1、android版本是利用高德地图提供的定位功能手机定位。
2、IOS是通过自带的定位功能定位，然后再通过高德地图转化为高德坐标


#### 一，申请密钥
请参照：[申请密钥Android定位SDK](http://lbs.amap.com/api/android-location-sdk/guide/create-project/get-key/)

#### 二，安装插件

```
cordova plugin add https://github.com/king12555/cordova-plugin-GaoDeLocation.git --variable API_KEY=your key（Android版本的key，因为ios版本无需用到高德的KEY）

```

#### 三，使用方法

```
// 进行定位
GaoDe.getCurrentPosition(successCallback, failedCallback);
```

获得定位信息，返回JSON格式数据:

```
{
  latitude : 纬度,
  lontitude: 经度,
  ...
}
```  
#### 四，查看当前安装了哪些插件

```
cordova plugin ls
```

#### 五，删除插件

```
cordova plugin rm cordova-plugin-GaoDeLocation
```

#### 六，Android版本需要主要在application的时候加入高德初始化代码

SDKInitializer.initialize(getApplicationContext());







