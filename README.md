# Firework
A code of Javascript to show beauty and draw your own beauty !

## describe
Firework JS by Lozyue draw fantastic fireworks on your website by using HTML5 Canvas.

# Usage
- initialize:
```javascript
var lzyFirework = new Fireworks(
	particlesNum=118    // default:150 发射的粒子数目.越小越流畅
	,partSpeed=4    //default:5 粒子运动速度。主要正相关控制粒子飞跃距离(直观就是) 
	,speedVariance=5     //default:10 粒子运动速度跨距,影响多个因素，直观影响粒子密集程度。粒子速度处于 U(partSpeed,speedVariance)的这个邻域上
	,friction=8    //直观理解为摩擦力。调整烟花大小时可调整此参数进一步装修
	,bindClick=true    // BOOL类型 是否绑定点击事件（用户点击canvas发射烟花）
	,showTarget=false    //是否显示目标位置，可用于调试时,效果亲自尝试即知，一般不开启
	,lineWidth=2    //正相关画的烟花和焰火粒子的大小（不是正比）
	,lzySlow=2    //发射速度模式 0|FALSE 加速上升; 1 匀速; >=2 分段变速;如果设置值大于2,则会应用到烟花（最小）上升速度上;此外烟花最小上升速度默认为 5
)
//var lzyFirework = new Fireworks(88,3,1,8,true,0,2,2); //example Two (The param suit for Mobile) 
```
- Interfaces:
方法：
`lzyShoot(queueFire,interval=false)`：发射自定义烟花队列方法

> `@parame queueFire`：一个对象数组，数组包含发射点的坐标和目标位置的坐标（二维数组？我也不知道叫啥）

    `interval`：是否排队发射，内部采用interval实现。需要一个个发射就传递一个毫秒数即可

`lzyRandomShoot(control=1,radius=0)` ：内置的随机放烟花函数。模拟真实效果
```
/**
 *参数: 均为 int 型
 * control: 表示随机发射烟花的频率.默认值1使用 1700 恰好一个周期.大于1的值将会被应用到频率上
 *          而设置为 0 或 FALSE 则会停止烟花发射
 * radius : 表示随机烟花位置波动半径。（其实是单向矩形）也许越大越随机吧。随机的事，谁说的定呢！
 *          为 0 默认使用内置判断。PC端188，移动端49 
*/
```

`fireInterval(functionName,intervalGap);`：替代调用setInterval 
**不能使用匿名函数
函数必须直接挂载在window全局对象上**

`delInterval()`：替代clearInterval
**会清除所有*fireInterval* 设置的定时器**

# Instruction
- [Blog Page](https://vip.hnyz.fun/uncategorized/24.html)

And that's all for this Library. No more updates!ᶘ ͡°ᴥ͡°ᶅ
