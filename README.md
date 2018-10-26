# EEGProject
## EEG_V2.1
+ ads1299参考电压有4.5V；
+ 原因：SPI的DIN通信线上有电阻，导致CH559T的SPI通信没有成功。
- CH559T 的USB_Hub,前几次能检测到设备，没有找到原因。
+ 增加AMS1117-5v稳压模块
