#### lottie-web-caption-animation
> Bodymovin导出json使用lottie-web实现字幕标题动画样例

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

> 注：图层对应的id或class需要在AE里面为对应图层添加

> 示例图

![示例图](/image/sample.gif)