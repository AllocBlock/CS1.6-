# cycler
[#点实体](wiki/point_entity) #模型

用于展示模型的点实体。模型会和玩家碰撞。支持模型动画，动画会循环播放。

?> 本实体如果用来显示模型，模型会有碰撞体积，玩家会被模型阻挡，攻击模型后模型会出绿血。如果不希望这种事情发生，可以使用[cycler_sprite](wiki/entity/cycler_sprite)

!> 引擎BUG：对着模型按E会引发交互（会听到交互音效），不建议和按钮放到一起使用

## 属性 (property)
> **名称** *targetname* = *空* | 字符串

实体的名称，用于被其他实体引发，可参考：[引发机制](wiki/trigger)

> **实体角度 (倾斜 旋转 滚动)** *angles* = *0 0 0* | 角度

旋转角度

> **渲染模式** *rendermode* = *空* | 单选

- 普通0 - 无光 = *空*
- 纯颜色1 (仅固体实体) = *1*
- 纹理2 - 微光(全亮) = *2*
- 发光3 (仅图标动画) = *3*
- 固体4 - 无光 = *4*
- 附加5 = *5*

常用的有三个。普通：平时正常的样式；固体：配合{开头的纹理实现透明（如梯子）；发光：配合黑底的纹理实现半透明（如光柱）；

> **渲染效果** *renderfx* = *空* | 单选

- 普通 (0) = *空*
- 脉冲 缓慢 (1) = *1*
- 脉冲 快速 (2) = *2*
- 脉冲 缓慢大范围 (3) = *3*
- 脉冲 快速大范围 (4) = *4*
- 滤波 缓慢 (9) = *9*
- 滤波 快速 (10) = *10*
- 滤波 极快 (11) = *11*
- 闪烁 缓慢 (12) = *12*
- 闪烁 快速 (13) = *13*
- 恒定的发光模式 (14) = *14*
- 扭曲 (仅模型) (15) = *15*
- 扭曲+渐隐 (16) = *16*
- 发光外壳(仅模型)(19) = *19*

> **透明度 (0-255 0=完全透明)** *renderamt* = *255* | 整数

> **渲染色 (R G B)** *rendercolor* = *空* | 颜色

> **模型文件** *model* = *空* | 路径

模型文件路径，模型放入models文件夹内，路径格式类似 ```models/myModels/myModel.mdl```，注意前面有 ```models/```。

> **身体子模型** *body* = *0* | 整数

> **皮肤** *skin* = *0* | 整数

> **动作** *sequence* = *0* | 整数

> **初始帧** *frame* = *0* | 整数

## 标记 (flag)
> **死亡模式中禁用** *= 2048*
