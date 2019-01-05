# EEGProject

+ 用于脑电信号研究的采集装置；
+ **国家重点研发计划项目启动会** “抑郁症复发的预警体系建立和综合干预策略研究“
+ “基于机器学习和云计算的抑郁症服务平台的研发和应用”方案介绍

## EEG_V2.1
1. ads1299参考电压有4.5V；
    + 原因：SPI的DIN通信线上有电阻，导致CH559T的SPI通信没有成功。
2. CH559T 的USB_Hub,前几次能检测到设备，没有找到原因。
    + 增加AMS1117-5v稳压模块，还是没能解决问题；
## EEG_V3.0
1. 制作22路的电极帽
     + ADS1299 - 6 四块构成24路的参考电极帽
2. 焊接成功
    + 参考电压输出4.5V；
    + 级联第一步测试成功，还需要对SPI进行测试
3. 供电方式
    + 采用纽扣电池进行供电
    + 通过两个开关控制供电和充电
## EEGChargeBattery
1. 纽扣电池进行供电。
2. 设计的可充电回路。
3. 通过开关控制串联供电和并联充电

## EEG_V4.0[2018.12.27]

1. 修改CH559L--CC2540模块

2. 添加12*2排母孔
   + 用于CC2540主控的连接；
   + PCB布局的距离控制；
   + 制作一个模块就行

3. 添加3.3v稳压电压模块
   + CC2540需要
   + ADS1299需要

4. 布设了基本的SPI信号线

   + 后面查找其它信号线相关的连接

5. 引出SPI信号接口，用作CC-Debug

6. 引出GPIO口，用于其余信号的控制

7. 两个USB接口

   + 两颗纽扣电池需要进行，串联供电，并联充电

   + 因此电池充电的时候，不能提供电源进行工作
   + 所以 USB_1,充电；USB_2 DM,DP功能