# env_beverage
[#点实体](wiki/point_entity)

用于生成拉罐饮料模型的点实体，可用来做自动售货机。引发后TODO：补充。

?> 必须引发：本实体需要被引发才会产生效果。

?> 默认朝右：实体默认朝向X轴正方向（即俯视图向右侧），调整实体角度（hammer中旋转、或设置实体角度属性）可以改变方向。

!> 只有第一次引发时会产生饮料，后面引发不会再产生。

## 属性 (property)
> **名称** *targetname* = *空* | 字符串

实体的名称，用于被其他实体引发，可参考：[引发机制](wiki/trigger)

> **实体角度 (倾斜 旋转 滚动)** *angles* = *0 0 0* | 角度

旋转角度

> **饮料总数** *health* = *100000* | 整数

> **饮料类型** *skin* = *空* | 单选

- 可口可乐 = *空*
- 雪碧 = *1*
- Diet Coke = *2*
- 橙汁 = *3*
- Surge = *4*
- Moxie = *5*
- 随机 = *6*

## 标记 (flag)
> **死亡模式中禁用** *= 2048*
