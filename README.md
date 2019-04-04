<p align="center">
  <a href="https://www.skillnull.com"><img src="https://skillnull.com/others/images/brand/MIT.svg" alt="License MIT"></a>
    <a href="https://996.icu"><img src="https://img.shields.io/badge/link-996.icu-red.svg" alt="License"></a>
</p>

### Bodymovin导出json使用lottie-web实现字幕标题动画样例
> [点此查看具体 AE + bodymovin + lottie-web 使用教程](http://skillnull.com/20190108/%E5%89%8D%E7%AB%AF%E8%A7%A3%E6%94%BE%E7%94%9F%E4%BA%A7%E5%8A%9B%E4%B9%8B-%E5%8A%A8%E7%94%BB%EF%BC%88adobe-effects-bodymovin-lottie%EF%BC%89/)

> 主要测试了以下功能：
- lottie.play() // 播放该动画，从目前停止的帧开始播放
- lottie.pause() // 暂停该动画，在当前帧停止并保持
- lottie.togglePause() // 暂停该动画，在当前帧停止并保持，再次点击从当前位置播放
- lottie.stop() // 停止播放该动画，回到第0帧
- lottie.destroy() // 删除该动画，移除相应的元素标签等。在unmount的时候，需要调用该方法
- lottie.setSpeed(2) // 设置播放速度，speed为1表示正常速度
- lottie.goToAndStop(500, false) // 跳到第500ms并停止播放
- lottie.goToAndStop(50, true) // 跳到第50帧并停止播放
- anim.renderer.elements[0].updateDocumentData({t: 'new text', s: 40}, 0) // 改变文本内容
- document.querySelector('#first_text').style.fontStyle = 'italic' // 改变文本样式为斜体
- document.querySelector('#first_text').style.fontWeight = 'bold' // 改变文本样式为加粗
- document.querySelector('#first_text').style.textDecoration = 'underline' // 为文本添加下划线

> __:bangbang: 注:__
- 要实现自定义文本样式是需要对应id或class来获取图层所在节点的
- 图层对应的id或class需要在AE里面为对应图层添加
- 目前只有svg渲染模式支持动态更改文字
- updateDocumentData方法目前只支持更改渲染为文本的内容，即Bodymovin渲染设置里什么都不要勾选，默认是有勾选的
- 本项目只有index.json是加了自定义id和class的
- 想要边框shap自适应文本内容长度，需要在AE里为对应shap添加表达式来实现
- [点此查看Bodymovin和lottie支持的AE特性列表](http://airbnb.io/lottie/supported-features.html)
- 本项目使用的.aep文件仅供学习使用

> 示例图

![示例图](/image/sample.gif)

| 源码中的示例动画名称 | 预览 | 源码中的示例动画名称 | 预览 |
| :-: | :-: | :-: | :-: |
| index | <div align="center"><img width="200" height="auto" src="/image/index.gif"/></div> | demo1 | <div align="center"><img width="200" height="auto" src="/image/demo1.gif"/></div> |
| demo2 | <div align="center"><img width="200" height="auto" src="/image/demo2.gif"/></div> | demo3 | <div align="center"><img width="200" height="auto" src="/image/demo3.gif"/></div> |
| demo4 | <div align="center"><img width="200" height="auto" src="/image/demo4.gif"/></div> | demo5 | <div align="center"><img width="200" height="auto" src="/image/demo5.gif"/></div> |
| demo6 | <div align="center"><img width="200" height="auto" src="/image/demo6.gif"/></div> | demo7 | <div align="center"><img width="200" height="auto" src="/image/demo7.gif"/></div> |
| demo8 | <div align="center"><img width="200" height="auto" src="/image/demo8.gif"/></div> |  |  |
