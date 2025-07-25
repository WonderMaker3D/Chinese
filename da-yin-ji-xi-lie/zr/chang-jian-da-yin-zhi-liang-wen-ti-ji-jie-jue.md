# 常见打印质量问题及解决

### 堵头

堵头是打印过程中常见的一个问题，分为挤出机堵塞和喷嘴堵塞两种

如何判断：

屏幕进行退丝操作，当屏幕上显示退丝动作完成，检查喷头上方ptfe管内耗材是否已完全退出

1.已完全退出，首先判定为喷嘴堵塞（见喷嘴疏通指南）

2.耗材还在挤出机内部，基本判定为挤出机堵塞（清理步骤见挤出机维护指南）

当以上两种情况都排除，还存在堵塞问题请联系技术支持。

### 首层不粘

1. ZR打印机为开放式机械架构，推荐打印pla等收缩率较小的打印腔温度要求不高的材料，对于打印abs，petc，pc等材料推荐加装封箱。
2. 检查PEI板是否脏污，可以使用酒精擦拭或者洗洁精清洗平台板（需晾干或擦干）。

### 悬垂质量差

**直接原因：打印悬垂表面时，挤出的耗材没有及时冷却、粘接在目标位置上而导致下坠，通常表现如下图：**

![左：悬垂质量较差；右：悬垂质量较好](<../../.gitbook/assets/0 (10).jpeg>)

### 解决方法

出现该问题时，建议尝试以下方法来改善：

首先观察模型的悬空倾斜角度，判断是否过大。一般情况下，悬空倾斜角度大于 45° 时，建议添加支撑；小于 45° 时则无需添加支撑。可以尝试按照后续步骤优化参数，以改善悬垂质量。

![](<../../.gitbook/assets/1 (36).png>)

注意：此处所指的模型悬空倾斜角度，指的是模型倾斜部分的平面与垂直于热床面之间所形成的夹角。与之相比，悬垂降速中的悬垂阈值是指挤出线条中不受下层支撑部分在挤出线宽中的占比，两者并不相同。

#### **模型的悬空倾斜角度大于 45°**

**如果模型的悬空倾斜角度大于 45 度，建议您参考下图，添加支撑结构以提高打印质量。**

![](<../../.gitbook/assets/2 (27).png>)

#### **模型的悬空倾斜角度小于 45°**

**如果模型的悬空倾斜角度小于 45 度，建议您参考以下方法，修改参数以提高打印质量。**

**1.适当降低喷嘴温度。**&#x5F53;悬垂部分的打印速度较慢时，降低喷嘴温度有助于减少对冷却的需求。

![](<../../.gitbook/assets/3 (27).png>)

**2.适当降低整体打印速度，或启用悬垂降速以降低悬垂部分的打印速度。**&#x5FC5;要时，您可以进一步降低悬垂速度。悬垂速度一般设置在 10-60mm/s 之间，悬垂阈值越大，悬空部分的幅度也会增加，此时通常需要使用更低的速度以确保打印质量。

![](<../../.gitbook/assets/4 (27).png>)

**3.适度调大辅助风扇、部件冷却风扇的转速百分比。**&#x5982;果悬垂质量一直很差，需要检查部件冷却风扇和辅助冷却风扇在打印过程是否可正常工作，可在 设备屏幕上控制功能里开关和调节风扇转速百分比来测试。

<figure><img src="../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

**4.打开打印机的前门和上盖盖**以获得更好的散热效果（一般只针对 PLA、PETG、TPU 类材料，其他耗材如此操作易因腔温过低而导致翘曲、层间结合变弱）。

### 模型翘边、脱落或倒塌

模型翘边、脱落或倒塌一般是由模型局部收缩、与打印板的粘接力不足导致的，且翘边后模型表面会有一条凸出横纹，因为模型翘边区域与喷嘴的距离变小，导致正在打印的这一层的挤出线被压扁而溢出。

![](<../../.gitbook/assets/6 (24).png>)

### **潜在原因和解决方法**

#### 1. 模型过于瘦高，重心较高，导致在打印过程中因晃动而出现脱落或倒塌的情况

* 建议增加支撑；
* 降低打印速度和加速度；
* 切片前更改摆放方式，尽量让模型平躺，或将模型切割后打印。

#### **2.** 喷嘴撞击模型

* 如果喷嘴温度不足，在高速打印过程中，耗材熔融不充分，挤出的熔体的粘度较高，流动性较差，易造成喷嘴刮蹭模型。此种情况下，建议适当提高喷嘴温度。另外，如喷嘴或者模型局部粘了料块，也可能导致打印过程中喷嘴撞模型。此种情况下，建议适当将喷嘴清洁干净后，升高温度并降低速度来进行打印。
* 有些填充图案的走线方式在单层之内存在交叉（如网格、三角形等），所以喷嘴在打印填充时会在交叉点发生刮蹭，这通常对打印不会有太大的影响，但如果确实发生了这种情况且影响了某些模型的粘接，可以尝试降低填充速度，或把填充图案改为单层之内没有交叉点的线、直线排列、螺旋体、同心等。

![](<../../.gitbook/assets/7 (10).png>)

&#x20;                                                              降低稀疏填充打印速度

![](<../../.gitbook/assets/8 (8).png>)

#### **3.** 耗材选择与打印设置

模型局部翘边通常是由于与热床的粘接力不足、冷却过快或局部收缩过大导致的。模型尺寸越大，收缩风险越高；填充率越高，收缩可能性也越大。ABS、ASA、PC、POM、PP、PA 和 PA-CF 等材料更容易发生收缩。因此，建议在进行大尺寸打印时尽量避免使用这些材料。相反，建议选择不易翘曲的耗材，如 PLA、PLA-CF、PETG、PETG-CF 和 PET-CF 等

* 床温温度偏低，导致模型与热床的粘接力不足——适当提高热床温度。
* 腔温偏低、风扇转速过高，导致模型冷却过快——适当提高热床温度，并关闭打印机的前门、盖上顶盖，适当调小风扇转速。
* 模型尺寸较大且填充率过高——如果模型尺寸较大且填充率设置得较高，如 60%（默认值是 15%），发生了翘边，可适当调低。另外，填充图案带有较多直线的更容易收缩，可以把填充图案改成螺旋体来降低收缩风险。对于部分对强度要求较高的结构件，可以设置 5 层墙和 25% 左右的填充率，尽量避免使用 50% 以上的填充率，以降低收缩趋势；对于大多数对强度要求较低的非结构件，则可以直接选择默认的 2 层墙和 15% 的填充率。

![](<../../.gitbook/assets/9 (11).png>)

&#x20;                                                                                            螺旋体填充

#### **4.** 模型与打印板的粘接力不足

* 打印板脏污或破损——清洗打印板（用清水和洗涤剂即可），或更换打印板。详情请参考：纹理 PEI 板清理指南。
* Brim 不足——启用 Brim 、调大其宽度。注意：减少 birm 和模型的间隙也有改善效果，但打印后需要修剪 birm 的难度会增⼤。
* 未正确涂胶——在打印板表面均匀涂胶。详情请参考：如何使用平台胶水。
* 热床温度偏低——适当调高热床温度。

辅助防翘小技巧——增加耳状Brim

通常由于材料的**局部收缩或者与打印板的粘接力不足，打印模型会出现翘边的现象，尤其是在打印 ABS 或 ASA 等易收缩的材料时。**&#x901A;常你可以在orcaslice中添加耳状Brim或者增加热床温度，来增强模型首层的粘接。不过有些情况下拆除耳状 Brim 可能会比较麻烦，且不能完全改善翘曲问题。因此，我们还推荐您在orcaslice 中，巧妙地在模型局部添加小圆片，可以帮你改善打印过程中模型翘边的问题，而且模型的后处理也更加方便。

![](<../../.gitbook/assets/10 (6).png>)

![](<../../.gitbook/assets/11 (3).png>)

Orcaslice中也可以更改耳状Brim的直径参数，（需要点击将Brim类型设置为绘制模式，否则切片不会生成）

也可以点击自动生成，不需要的地方可以右键删减。

### 打印层过热、下垂

如下图所示，左侧的圆锥体为部件冷却风扇停转的情况下高速打印；右侧的圆锥体为部件冷却风扇打开的情况下，使用默认设置打印。

![](<../../.gitbook/assets/12 (2).png>)

### 潜在原因和解决方式

#### 1. 部件冷却风扇故障

打印出现过热、下垂的最常见原因是**部件冷却风扇**故障。

如果打印时冷却效果不足，则会导致打印的耗材没有足够的时间冷却和固化。

对于此问题，建议首先尝试在 orcaslice &#x7684;**“设备→Part fan/Auxiliary Fan**”中手动打开部件冷却风扇，将风扇转速调整到 100%，确认风扇是否正常启动。

![](<../../.gitbook/assets/13 (3).png>)

如果风扇正常工作，则问题可能与您的切片文件参数有关。\
如果风扇不工作，则问题可能与部件冷却风扇故障、部件冷却风扇的插头连接不良有关。

#### 2. 打印速度过快

打印速度过快也会导致打印质量差。如果打印速度太快，耗材无法获得充分冷却。使用**运动**和**狂暴**模式提高的打印速度，并不会提高零件冷却性能。

当使用这些模式提高打印速度时，需要提供更强的冷却。

为了获得最佳效果，我们建议在切片参数中调整打印速度，而不是从屏幕选项中调整打印速度。

#### 3. 喷嘴温度过高

如果喷嘴温度设置得过高，耗材可能会在喷嘴内过热，并可能导致打印质量不佳。

应根据使用的打印速度调整喷嘴温度。例如，在 orcaslice 中默认的 PLA 耗材喷嘴温度为 220 ℃，这是适合默认配置文件中打印速度的喷嘴温度。

如果使用**静音**模式打印，由于此时打印速度会降低到原本的 50%，则可能需要将喷嘴温度设置为 210 ℃，意味着不需要太高的喷嘴温度，耗材也可以被高效挤出。

#### 4. 最短层时间太短

在**耗材丝设置**中设置**最短层时间**，是根据冷却效果限制打印速度的一种方法。

此设置可确保打印机至少需要 4 秒钟才能完成一层的打印，然后再进行下一层的打印。如果打印该层的时间少于 4 秒，则会自动降低打印速度以确保耗材充分冷却。

![](<../../.gitbook/assets/14 (3).png>)

根据不同类型的耗材要求对其进行微调。PLA 通常需要尽可能高的冷却参数，而 ABS 和 ASA 等耗材则需要较少的冷却。

如果出现散热不足，最好将**最短层时间**增加几秒钟，确保模型有足够的时间冷却，然后再打印下一层。**注意：通常，在打印非常小的物体时需要注意此问题。较大的模型通常不受此影响，因为打印更大的层需要更长的时间，耗材有足够时间冷却下来。**
