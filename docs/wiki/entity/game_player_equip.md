# game_player_equip
[#点实体](wiki/point_entity)

用于发枪的点实体。默认会在回合开始时对所有玩家自动引发，也可以被手动引发，引发后给引发者发枪械、弹药、匕首、医疗包和盔甲等装备。

!> 地图中使用该实体后，无论有没有勾选“只能引发”，玩家不会再发默认武器了（CT是匕首+USP，T是匕首+Glock18）。如果没有勾选“只能引发”，每回合开始玩家会得到这个实体指定的装备（上局的装备依旧保留）；而如果勾选了“只能引发”，因为不再发默认武器，如果玩家是新加入的、或者上回合死亡了，玩家只会变空手，什么武器都没有。建议使用这个实体时配合[player_weaponstrip](wiki/entity/player_weaponstrip)，每回合开始先剥夺武器，然后发固定的枪，这样能保证每回合开始的枪都一样。

!> 发的武器不能太多，不然可能导致地图崩溃闪退。

## 属性 (property)
> **名称** *targetname* = *空* | 字符串

实体的名称，用于被其他实体引发，可参考：[引发机制](wiki/trigger)

> **属主** *master* = *空* | 字符串

填写[multisource](wiki/entity/multisource)的名称，详见[multisource](wiki/entity/multisource)

> **[容易导致玩家武器过多出错]** *classname* = *空* | 字符串

> **刀** *weapon_knife* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **USP45 (45acp口径)** *weapon_usp* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **Glock 18 (9mm口径)** *weapon_glock18* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **Desert Eagle (50ae口径)** *weapon_deagle* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **P-228 (357sig口径)** *weapon_p228* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **Beretta Elites (9mm口径)** *weapon_elite* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **Five-Seven (57mm口径)** *weapon_fiveseven* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **Benelli M3 (12 Gauge)** *weapon_m3* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **Benelli XM1014 (12 Gauge)** *weapon_xm1014* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **MP5/Navy (9mm口径)** *weapon_mp5navy* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **TMP (9mm口径)** *weapon_tmp* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **FN P90 (57mm口径)** *weapon_p90* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **Mac-10 (45acp口径)** *weapon_mac10* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **UMP 45 (45acp口径)** *weapon_ump45* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **AK-47 (762nato口径)** *weapon_ak47* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **SG552 (556nato口径)** *weapon_sg552* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **M4A1 (556nato口径)** *weapon_m4a1* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **Aug (556nato口径)** *weapon_aug* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **Scout (762nato口径)** *weapon_scout* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **AWP (338magnum口径)** *weapon_awp* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **G3/SG-1 (762nato口径)** *weapon_g3sg1* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **SG550 (556nato口径)** *weapon_sg550* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **M249 (556natobox口径)** *weapon_m249* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **Famas (556nato口径)** *weapon_famas* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **Galil (556natobox口径)** *weapon_galil* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **防暴盾牌** *weapon_shield* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **防弹衣** *item_kevlar* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **防弹衣+头盔** *item_assaultsuit* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **闪光弹** *weapon_flashbang* = *空* | 单选

- 否 = *空*
- 1 = *1*
- 2 = *2*

> **高爆手榴弹** *weapon_hegrenade* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **烟雾弹** *weapon_smokegrenade* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **拆弹钳** *item_thighpack* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **C4炸弹** *weapon_c4* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **9mm Parabellum 弹药** *ammo_9mm* = *空* | 单选

- 否 = *空*
- 1 梭 (30发) = *1*
- 2 梭 = *2*
- 3 梭 = *3*
- 4 梭 (填满) = *4*

> **.45 ACP 弹药** *ammo_45acp* = *空* | 单选

- 否 = *空*
- 1 梭 (12发) = *1*
- 2 梭 = *2*
- 3 梭 = *3*
- 4 梭 = *4*
- 5 梭 = *5*
- 6 梭 = *6*
- 7 梭 = *7*
- 8 梭 = *8*
- 9 梭 (填满) = *9*

> **.50 Deagle 弹药** *ammo_50ae* = *空* | 单选

- 否 = *空*
- 1 梭 (7发) = *1*
- 2 梭 = *2*
- 3 梭 = *3*
- 4 梭 = *4*
- 5 梭 (填满) = *5*

> **5.7mm 弹药** *ammo_57mm* = *空* | 单选

- 否 = *空*
- 1 梭 (50发) = *1*
- 2 梭 (填满) = *2*

> **.357 SIG 弹药** *ammo_357sig* = *空* | 单选

- 否 = *空*
- 1 梭 (13发) = *1*
- 2 梭 = *2*
- 3 梭 = *3*
- 4 梭 (填满) = *4*

> **12 Gauge 弹药** *ammo_buckshot* = *空* | 单选

- 否 = *空*
- 1 梭 (8发) = *1*
- 2 梭 = *2*
- 3 梭 = *3*
- 4 梭 (填满) = *4*

> **7.62mm NATO 弹药** *ammo_762nato* = *空* | 单选

- 否 = *空*
- 1 梭 (30发) = *1*
- 2 梭 = *2*
- 3 梭 (填满) = *3*

> **5.56mm NATO 弹药** *ammo_556nato* = *空* | 单选

- 否 = *空*
- 1 梭 (30发) = *1*
- 2 梭 = *2*
- 3 梭 (填满) = *3*

> **5.56mm NATO Box 弹药** *ammo_556natobox* = *空* | 单选

- 否 = *空*
- 1 梭 (30发) = *1*
- 2 梭 = *2*
- 3 梭 = *3*
- 4 梭 = *4*
- 5 梭 = *5*
- 6 梭 = *6*
- 7 梭 (填满) = *7*

> **.338 AWP 弹药** *ammo_338magnum* = *空* | 单选

- 否 = *空*
- 1 梭 (10发) = *1*
- 2 梭 = *2*
- 3 梭 (填满) = *3*

> **医药包** *item_healthkit* = *空* | 单选

- 否 = *空*
- 1 医药包 = 15 生命值 = *1*
- 2 医药包 = 30 生命值 = *2*
- 3 医药包 = 45 生命值 = *3*
- 4 医药包 = 60 生命值 = *4*
- 5 医药包 = 75 生命值 = *5*
- 6 医药包 = 90 生命值 = *6*
- 7 医药包 = 100 生命值 = *7*

> **盔甲能量** *item_battery* = *空* | 单选

- 否 = *空*
- 1 电池 = 15 盔甲值 = *1*
- 2 电池 = 30 盔甲值 = *2*
- 3 电池 = 45 盔甲值 = *3*
- 4 电池 = 60 盔甲值 = *4*
- 5 电池 = 75 盔甲值 = *5*
- 6 电池 = 90 盔甲值 = *6*
- 7 电池 = 100 盔甲值 = *7*

> **长跳飞行包** *item_longjump* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **产生火花数量** *spark_shower* = *空* | 字符串

> **产生可打爆的气罐** *item_airtank* = *空* | 单选

- 否 = *空*
- 是 = *1*

> **产生弹来弹去的grenade** *grenade* = *空* | 单选

- 否 = *空*
- 是 = *1*
- 多个 = *2*

## 标记 (flag)
> **只能引发** *= 1*

勾选后，回合开始时不会自动引发，只能手动引发。但回合开始的默认武器依旧会消失。

> **死亡模式中禁用** *= 2048*
