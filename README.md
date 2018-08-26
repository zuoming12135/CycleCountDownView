# CycleCountDownView
环形倒计时
实现了环形倒计时
调用简单，只需设置基本的属性
```
//drawView = MZDrawView(frame: CGRect(x: 100, y: 100, width: 100, height: 200))
// 自定义圆的起始点
drawView = MZDrawView(frame: CGRect(x: 100, y: 100, width: 100, height: 100), angle: CGFloat.pi * (0.5))
drawView?.backPathColor = UIColor.red
drawView?.cycleColor = UIColor.cyan
drawView?.duration = 10
// 半径 (不设置的话就默认为MZDrawView的最大内切圆的半径)
drawView?.radius = 20
self.view.addSubview(drawView!)

// 可以添加倒计时的时间喔
@IBAction func update(_ sender: Any) {
        self.drawView?.update(time: 20)
    }
```
