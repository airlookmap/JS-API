## Question List

1. 页面初始化白屏，无反应？
   
	一般情况下是由于 js-api 版本过低, 或者 appkey 有误或失效。

2. 页面黑屏，看不到三维地图实景数据？ 
   
	在确保 api 接口使用无误情况下，一般是由于设置的 center 坐标有误引起的黑屏。

3. 通过代码添加的 Marker / Polygon / Line 在场景无效果？
   
	首先，先确保添加的坐标点是否正确；其次，需要确保代码是否运行在三维场景加载完成的回调函数中。

4. 进行页面交互时添加的 Marker 无反应，但是初始化有效？  

	一般情况下由于离屏渲染造成的影响，解决方案：1. 强制执行刷新帧 `map.forceRender()`    2. 关闭离屏渲染 `map.requestRenderMode = true`。
