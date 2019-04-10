## 分析过程



### 项目目标

利用Biosan技术保障中心维修部的历史维修报告记录文本，提取出各种设备的历史故障数据（包括使用年限、维修服务内容、故障描述、故障模块、故障时间等，部分设备的实验数据（例如质谱仪等）），建立一套运维模式，预测仪器发生故障的风险，对风险较高的设备进行干预（重点巡检和维护）。



### 文本预览

#### 问题描述内容

```
1235仪器偶尔提示TipInAir。
偶尔17-OHP实验提示TipInAir4331
Lis与Leica软件对接问题。
FISH扫描对焦失败。
双标实验F点偏高，400万以上；筛查阳性率低于平时，只有2%-3%；
GSL120黑屏重启，显卡温度高。GSL120年度保养。
1、加样针误报clot，不多，每次实验一两个，但客户不接受；2、洗板机头容易堵（我今天过去检查）
1235产筛实验结果，标准品第四点异常，diff偏差超过50%。
GSP性能检测。
近期第二次发生找不到增强液的报错已安排杨露鉴去检查
1235产筛实验，标准品D点偏低，同时，质控中值也偏低，样本中，只要是4号针加样的样本，都有偏低的倾向，因此需要检查加样针的加样精度。（已安排潘盛过去）
1、洗板机堵孔，昨日多次清洁后正常，今天又堵，清洁无效2、最近两次实验高值质控低出控，第一次原因不明，第二次确认为质控复融问题，科室希望做仪器维护排除仪器问题（1个月前已做年度维护，后更换滤光片和导轨）
杭州市妇产科医院2号1235仪器，联机报错，1号针注射器工作异常
客户反映GSL120加油针不灵活；1235做性能验证，并出具报告；
1.新筛实验有报bloodmissing的报错2.170hp实验缓冲液位置报错tipinair3.实验结果出控，复孔标准品的差异很大.客户希望进行相关性能测试
1235实验过程中突然在去血片过程中出现真空错误，疑似发生严重漏气
近期加样枪两次问题，一次去吸头时的up-downmoversteppingerror，一次去黑帽时的up-downmoversteppingerror，并且提示取不到黑帽；还有长期以来的真空错误
MB8扫描对焦模糊；初步判断为显微镜Z轴磨损，待下周二与奥林帕斯售后仪器上门维修。
KM2明场捕获图像质量不理想，要求调试参数；3台KM系统维护保养；
客户反映最近阳性标本复查重复性下降，cv超过10%的标本增多。需要仪器保养与性能验证。
早孕实验报错“foamdetected”，导致不吸样，加样针涂层损坏严重，需要更换
1235联机报错epprom读取错误，怀疑node1IC14故障需要更换
确认空气过滤器需要更换，销售已报价。
维修洗板机堵，并执行年度维护；
例行执行半年度维护
1235 更换电脑 系统重装软件重装
执行1235半年度维护
执行1235季度维护
GSL120底座有噪音，初步判断是风扇发出的声音，需更确认问题换风扇
CDS-5通风管路清理。
1、1420仪器做PKU的时候，标准曲线拉不卡，荧光值一直在下降，由原来第六点8000，一直降到6000左右，14年底突然降到3000多，现在3000都不到了，需要找找原因。2、1235全自动做TSH，最近质控上下波动很厉害，需检查下是否需要清洁去血片头及洗板头。
去血片头Z方向移动故障
1235年度维护
由吴挺补充
2351158样本仓移动故障，皮带无规则左右抖动
1297注射器泵异响，需要检查，泵的运动部分需要清洁润滑
KM1客户放映前一天分析完的数据，第二天打开case后数据丢失；第二，电脑关机时提示声卡文件错误；
扫描仪扫描故障
客户第一次独立使用1235实验，不小心导致加样针位置偏差，需要重新校准加样针和位置
1420无法联机，重新安装软件无法解决，怀疑是数据通讯模块故障
P9的计算机在打孔过程中容易发生死机
早孕实验x-conv移动故障 导致实验中止
120仪器底部风扇噪音大
加样枪移液过程中有滴液现象需要检测维修如有需要更换加样枪
洗板测试失败，提示timeout。
1235洗液和蒸馏水桶有漏点 造成真空报错 客户要求工程师上门检测 必要时更换水桶
右枪在加样过程中pipetteerror
1235在洗板测试过程中报timeout
计算机启动黑屏，无法联机
GSL120提示Error：UserBreak。
1235防蒸发帽偶尔掉落。
洗涤工作站工作无响应，上周五经吴挺测试正常，客户仍不放心，周三实验室需跟踪
DX半年度保养；
1235半年度保养，并IPV检测；
例行维护
例行维护
1420进板有时会发生报错，提示移动故障
```



#### 服务报告内容

```
1、校准右枪Flag传感器位置；2、对换左右枪；3、待观察
1、校准右枪TipSensor压力；2、移除空气过滤器，真空报错正常；3、待观察；
leica软件生成xml文件，包含病人信息及图像信息；Lis直接调用xml文件内容，实现对接；
1、测试发现客户未调试好曝光时间；2、培训客户调试曝光时间，测试扫描正常；
检查仪器Flash值为1380，反馈滤光片腐蚀；用增强液及无水酒精清洁反馈滤光片；Flash下降至1180；用Eu定标液重新校准FLASH值至1080；测试实验双标F点降低至330万，恢复正常；
问题：GSL120黑屏，怀疑显卡故障，年度维护处理：到场后，客户已更换显卡，电脑能正常工作。根据客户反应，最近一次有一张玻片拍到空白照片。检查后发现仪器光源不稳定，摄像头画面明暗闪烁。询问得知客户最近自行跟换灯泡，检查灯泡发现瓦数不对，正常使用100w的灯泡，客户换上去的是30w换100w灯泡后光源稳定仪器全套校准结果：隔夜扫片正常。
检查确认仪器大概率不存在问题，首先每次实验报clot的数量减少，只有一两个，其次是报错并不集中于某一根针，3次报错分别是三根不同的加样针。进行的操作是检查了加样针的固定和排线的链接，重新校准了液面感应。并对样本上机前处理，同许主任进行了交流。针对浙江等地的经验，即上机前用竹签再挑一下，许主任暂时是抵触的，需要俞勇再去教育一下。客户反应的另一个洗板机头容易堵的情况，检查下来没有发现什么异常，清洁了洗板机头。
对四根加样针进行精度测试：P1=25.33，P2=25.17，P3=25.12，P4=25.23，正常；进行洗板测试，发现部分孔注水不满，吸的时候对应的单数列第四个点吸的水吸不干，残留三分之一左右；实验标准曲线不好是由于洗板机头问题，清洁洗板机头，并指导客户如何清洁；
-washertest正常-MeasurementModuleTest正常-HighVolumePipetteTest正常-LowVolumePipetteTest正常
问题：开机自检报错，机器无法运行；措施：1.查看历史记录，发现实验前未放置稀释杯，导致实验无法往下走2.维护增强液管路，对管路进行疏通，未发现异物结果：1.增强液测试通过；2.开机自检正常；3.跟一次实验正常；
对四根加样针进行精度测试，发现第四根针在加水之后针尖挂水滴；把第四根针与第三根互换，发现第三根（原来的第四根针）挂水滴，说明是针的问题；由于另外三根针也有锈迹，更换一套4根针，精度测试P1=25.10，P2=25.02，P3=24.90，P4=24.81，符合范围；查看历史记录，发现去血片时候有报真空错误，最近一次实验每块板子报两个；查看真空泵，发现2号真空泵停止工作，把2号与3号对换，发现3号（原来的2号）依然停止工作；与主任沟通后更换停止工作的3号真空泵，与空气过滤器（过滤器原来的坏了，吴挺拆下来之后仪器未安装过滤器，现在安装一个新的）；
嘉兴妇保洗板头反复堵塞，清洁洗板头、电磁阀，测试正常。右枪加样准确度测试正常，定标液测试正常。仪器状态正常。
更换2号注射器泵，Rinse测试正常；2板实验正常；
清洁120加油针，调试加油针角度，校准坐标；恢复正常；
1235右枪加样时会有试剂滴出，右枪有磨损。右枪压力调整，测试正常，建议更换。洗板测试、加增强液测试、去血片测试、定标液测试正常。
问题：仪器第五板去血片报5个真空错误，第六板去血片报10个真空错误，导致操作超时，流程停止；措施:报真空错误怀疑1.系统漏气2.抽负压效率低；真空泵工作间隔大于2min，排除系统漏气；抽负压效率低原因：1.泵工作效率低，如停止工作2.气路堵塞；连续做了8板去血片测试后，泵依旧工作；最后怀疑气路堵塞，拆掉过滤器后，仪器正常；总结：气路堵塞的情况，真空泵的出气量可以感觉到比较小，抽真空的时间会比较长；
聊城市妇幼保健院问题：1235右枪近期两次up-downmoveerror处理：查看历史记录，最近一次报错是在打枪头时出现，是由打枪头时戳到托盘上的废枪头引起前一次报错是由于打枪头时未正常将枪头打掉，导致配试剂过程中，取防蒸发帽过程错误。测试右枪气压和机械步进误差均正常，配试剂测试均正常。清洁右枪枪头，检查右枪坐标均正常。试剂仓步进误差正常针对历史记录中的真空错误较多问题，清洁去血片头，调紧去血片头的压轮。去血片测试气压正常。跟踪一次实验未出现异常。结果：可正常使用。
将扫描主机移到地面上，画面晃动减弱，图像捕获清晰；
问题：捕获时条带不清晰，保养3台显微镜。处理：1，清洁各镜头，平台，科勒照明调整。2，捕获，比原先市时清晰。3，设置快捷键。结果：仪器使用正常。
富阳区妇幼保健院：1235年度维护：1.机械测试正常；增强液加样精度正常；洗板机残余量正常；加样枪测试正常；2.检测单元正常，Eu：103.9万，Sm：10.5万，flash：1212.3.加样针精度测试正常4.填写校验报告。仪器性能正常，对于之前出现一次阳性标本复查正常情况，可能为其他原因导致。
```



### 问题分析

需要回答的问题是，下次对某台仪器需要什么时候去维护

所以预测的主体，应该是仪器而不是客户

其次，存在一次维护修复多台仪器的可能，所以训练样本的条数并不是数据的行数，需要对所有数据进行拆分，对每条仪器的护理动作单独提出来才行



最简单的思路：

定义每一家客户，每一台仪器，每一个核心部件（模块）的目前情况[《1235模块关键词定义》](../source/md/1235关键词按模块分类.md)

定义这一核心部件一般在多长时间会坏，预测下一次坏的时间

仪器维护的时间是所有核心部件的维护加权合。





根据这一分析思路，认为目前的数据需要提取的信息包括：

1. 每个客户分别有哪些仪器，每台仪器的装机时间和维修次数，维修的内容需要细分，每个部位分别经过了多少次维修，目前情况如何评价
2. 需要定义每一类型仪器在某个部位坏了之后的寿命，或者某个部位某次维修之后，下次报错可能需要的时间。这个时间的定义可以是实验批次即老师操作的次数，也有可能是样本量。如果是样本量，需要读取每个客户的单批次实验样本量和总年度样本量，就跟汽车的里程一样计算寿命。
3. 如何细分大问题和小问题，可能一句话里既包括大问题又包括小问题，问题的分类需要和工程师沟通。



存在的数据偏差：

1. 不同工程师的报告风格不同，这与对应带教师父的要求严格程度有关，比如质谱工程师的记录就要比其他人的记录要相对详细，可能会带入更多问题。
2. 2015年的部分数据存在明显的缺失，可能是系统导出的不完整，是否可以直接丢弃这部分样本，值得考究。



通过观察 **问题描述** 及 **服务报告**内容，可以看到：

1. 问题中存在定期维护的内容，存在修理一台仪器同时维护另一台仪器的情况，需要观察定期维护的内容和其他有什么区别。

   这部分信息在**服务部门**字段有提及一部分，但并不全

2. 问题描述的部分是解释这次维修服务去解决的问题，服务报告是具体解决问题的方法。

3. 部分问题描述被记录在服务报告里，考虑是否应该把这两列合并处理

4. 服务报告的末尾一般有本次服务的结论，是否修好，可以选择提取一部分然后做人工的修正得出维修结果

   在另一列**问题是否解决**含有一部分此类结论，但是存在大部分的缺失

5. 存在一列**故障描述**包含了部分问题描述的内容



有一个核心问题是，如何衡量这次维护所修复的问题大小

1. 可以参考维修总费用这一列，存在一部分的缺失但是大部分是0。如何定义高额维修费用之后仪器的状态也是一个关键点。并且存在一次维护对多台仪器维护的可能，在拆分样本的时候如何对这一数据进行拆分，也是关键所在

2. 根据工程师提供的问题定义划分



### 目标设定



如果将维修后的下一次维修时间作为预测目标：


```mermaid
graph TD
A0 --> E1[客户信息]
E1 --> E12[客户重要程度_成本预估]
E1 --> E11[仪器使用频次]
A0[系统提取结构化数据] --> D11[仪器历史状态]
A[报告记录输入] --> |文本预处理|C{输入分流}
C --> |切词命名实体识别|B2[维修报告]
B2 --> C2{特征提取}
C2 --> |命名实体识别|D1[仪器信息_具体哪台仪器]
D1 --> D11
C2 --> |命名实体识别|D2[本次问题部位]
C2 --> |情感分析|D3[问题严重程度]
C2 --> |命名实体识别|D4[维修后的情况]
D11 --> D12[该部位上一次坏的时间]
D2 --> D12 
D12 --> |结合当前时间计算|D13[维修到坏的时间间隔]
D3 --> B3
D4 --> B3
B3{模型预测} --> D15[下一次坏的时间]
E12 --> D14[下一次维护该部位的时间]
D13 --> B3
E11 --> B3
C --> |关键词匹配|B1[维护报告]
B1 --> E13[上一次维护时间]
E13 --> D14
D15 --> D14
```

![](../source/fig/flow1.png)