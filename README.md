# Firework
A code of Javascript to show beauty and draw your own beauty !

# Usage
- initialize:
```
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
```
- Interfaces:
`lzyRandomShoot(control=1,radius=0)`
