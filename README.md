# Dom-Animate

补间动画
序列帧动画
svg动画
3D动画
骨骼动画


Why Use TimeAxio?

* 动画描述与动画控制，高度抽象又完美解耦
* 通过简单动画组合，支持构建多种复杂动画
* 帧渲染优先级算法，简化动画描述并创造符合预期的动画
  

动画库：
https://juejin.cn/post/6844903830098804743

引擎：
http://www.fly63.com/nav/more/12




## 框架定位:

轻量级DOM & SVG 动画引擎


命令式？？
声明式？？
面向对象？？


属性类型：
* attribute
* css
* transform
* text

值类型：
* 数值
* 颜色
* transform值

值转化：
type:'',
prop:'',
from: {numbers,strings},
to:{numbers,strings},





<img src="./design.svg" />

## 设计接口: 调用方式，参数，方法

```
new Animate(options)
```

·

```
const move = Animate(
    {
        el: '',
        props:{
            x:[10,100],
            y:[100,200],
        },
        step: 5,
        duration: 5000, // 时长
        easing: 'easeInOutCirc',    // 缓动    
        delay: 1000
    }
)
```
```
el:'',
keyFrames:[
    {x:,y:}
    {x:,y:}
    {x:,y:}
],
duration: ---,
delay: 
```

move.reset();
move.finish();
move.clear();
move.pause();
move.reverse().play();
move.loop(1);




重新定义动画属性：

move.reset({
    x:'',
    y:''
})




const ani = new Animate();

ani.add({
    el:'',
    props:{},
    delay:'',
})

ani.play();
### Target 目标元素



### Attrs 动画属性



### Options 动画设置

| 参数      | 类型               |     |
| --------- | ------------------ | --- |
| duration  | Number             |     |
| loop      | Boolean            |     |
| direction | String             |     |
| easing    | String \| Function |     |
| auto      | Boolean            |     |
| begin     | Function           |     |
| complete  | Function           |     |
|           |                    |     |
|           |                    |     |



### Methods 方法



| 方法     |     | --- |
| -------- | --- | --- |
| play     |     |     |
| pause    |     |     |
| reset    |     |     |
| complete |     |     |
| process  |     |     |



## 架构设计: 工程(webpack)，测试(jest)，TS



## 程序实现

设计模式（类，通信方式，策略模式）, 模块设计（循环引擎，缓动模块，参数预处理，动画数据，动画主类）



渲染引擎 engine.js

缓动模块 easing.js
    Coding: https://github.com/danro/jquery-easing/blob/master/jquery.easing.js
    Demo：https://easings.net/


数据模块 data.js（颜色，百分比，数值，角度）

动画主类 main.js







