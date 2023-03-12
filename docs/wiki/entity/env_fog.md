# env_fog
[#点实体](wiki/point_entity)

在全图范围内产生雾的点实体。

!> 和X-man天书中介绍的不同，本实体开启后全图都会笼罩在雾中，而非X-man天书中描述的可以设置覆盖范围。

## 属性 (property)
> **名称** *targetname* = *空* | 字符串

实体的名称，用于被其他实体引发，可参考：[引发机制](wiki/trigger)

> **雾的密度 (0.01 - 0)** *density* = *0.001* | 字符串

> **雾的颜色 (R G B)** *rendercolor* = *255 255 255* | 颜色

## 标记 (flag)
> **开始时打开** *= 1*

> **死亡模式中禁用** *= 2048*
