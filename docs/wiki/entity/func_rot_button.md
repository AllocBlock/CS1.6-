# func_rot_button
[#固体实体](wiki/solid_entity)

用于制作会转动的开关的固体实体。和普通开关的主要区别是引发时会转动。

?> 相关实体 [func_button](wiki/entity/func_button)：可破碎的物体；[func_guntarget](wiki/entity/func_guntarget)：枪靶；[button_target](wiki/entity/button_target)：标靶开关（攻击它时引发）；

?> 需要轴心：需要配合origin纹理![origin](../../images/tex_origin.png)使用。TODO：待补充

## 属性 (property)
> **名称** *targetname* = *空* | 字符串

实体的名称，用于被其他实体引发，可参考：[引发机制](wiki/trigger)

> **属主** *master* = *空* | 字符串

填写[multisource](wiki/entity/multisource)的名称，详见[multisource](wiki/entity/multisource)

> **目标** *target* = *空* | 字符串

目标实体的名称，用于引发其他实体，可参考：[引发机制](wiki/trigger)

> **引发前延时** *delay* = *0* | 小数

将要引发目标时，不再是立刻引发，而是延迟一段时间再引发。单位为秒，精确到0.1秒。

> **删除的目标 (无法复原)** *killtarget* = *空* | 字符串

删除指定的实体，刷新不会恢复删除的实体，只有重新载入地图才能恢复。

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

> **实体效果 (数字可相加)** *effects* = *空* | 多选

- 无 = *空*
- 1 (粒子漩涡) = *1*
- 2 (枪口火焰) = *2*
- 4 (强光) = *4*
- 8 (弱光) = *8*
- 16 (假定环境光线向上) = *16*
- 32 (不插入下一帧) = *32*
- 64 (发光图标) = *64*
- 128 (不可见/无网络传输) = *128*

> **纹理发光样式** *style* = *空* | 单选

- 普通 = *空*
- 捆绑到同名光源 = *-3*
- 闪烁的荧光 = *10*
- 脉冲 缓慢 强大 = *2*
- 脉冲 缓慢 = *11*
- 脉冲 温和 = *5*
- 闪烁 A = *1*
- 闪烁 B = *6*
- 烛光 A = *3*
- 烛光 B = *7*
- 烛光 C = *8*
- 滤波 快速 = *4*
- 滤波 缓慢 = *9*
- 水下光线 = *12*

> **最小灯光等级 (0.0-2.0)** *_minlight* = *空* | 字符串

> **内容物 (非固体时)** *skin* = *空* | 单选

- 无 = *空*
- 空 = *-1*
- 水 = *-3*
- 毒液 = *-4*
- 熔岩 = *-5*
- 水2 = *-6*
- 梯 (攀爬区域) = *-16*

> **声音样式 (sound/buttons/)** *sounds* = *空* | 单选

- 无 = *空*
- 电钮1 button1.wav = *1*
- 电钮2 button2.wav = *2*
- 电钮3 button3.wav = *3*
- 电钮4 button4.wav = *4*
- 电钮5 button5.wav = *5*
- 电钮6 button6.wav = *6*
- 电钮7 button7.wav = *7*
- 电钮8 button8.wav = *8*
- 电钮9 button9.wav = *9*
- 电钮10 button10.wav = *10*
- 电钮11 button11.wav = *11*
- 门闩锁住 latchlocked1.wav = *12*
- 门闩解锁 latchunlocked1.wav = *13*
- 普通电灯开关 lightswitch2.wav = *14*
- 转门 lever1.wav = *21*
- 转门 lever2.wav = *22*
- 转门 lever3.wav = *23*
- 转门 lever4.wav = *24*
- 转门 lever5.wav = *25*

> **转动角度** *distance* = *90* | 整数

> **转动速度** *speed* = *90* | 整数

速度，单位/秒

> **复位前延时 (-1=永不复位)** *wait* = *3* | 整数

> **通过武器攻击引发** *health* = *空* | 单选

- 否 = *空*
- 是 = *1*

如果设置不是空而且大于0，则开关不再能按E引发，而是变成用武器攻击引发，这个值的大小对应了耐久度。

> **?新目标** *changetarget* = *空* | 字符串

修改目标实体的目标。类似[trigger_changetarget](wiki/entity/trigger_changetarget)的作用。

## 标记 (flag)
> **内容物非固体** *= 1*

> **反向运动** *= 2*

> **锁定** *= 32*

> **绕X轴旋转** *= 64*

勾选后，变成以X轴为转轴旋转。默认情况下是绕Z轴旋转的。

> **绕Y轴旋转** *= 128*

勾选后，变成以X轴为转轴旋转。默认情况下是绕Z轴旋转的。

> **通过接触引发** *= 256*

> **死亡模式中禁用** *= 2048*
