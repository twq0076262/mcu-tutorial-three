# 14. 单片机 I2C 总线与 EEPROM

前几章我们学了一种通信协议叫做 UART 异步串行通信，这节课我们要来学习第二种常用的通信协议 I2C。I2C 总线是由 PHILIPS 公司开发的两线式串行总线，多用于连接微处理器及其外围芯片。I2C 总线的主要特点是接口方式简单，两条线可以挂多个参与通信的器件，即多机模式，而且任何一个器件都可以作为主机，当然同一时刻只能有一个主机。

从原理上来讲，UART 属于异步通信，比如电脑发送给单片机，电脑只负责把数据通过 TXD 发送出来即可，接收数据是单片机自己的事情。而 I2C 属于同步通信，SCL 时钟线负责收发双方的时钟节拍，SDA 数据线负责传输数据。I2C 的发送方和接收方都以 SCL 这个时钟节拍为基准进行数据的发送和接收。

从应用上来讲，UART 通信多用于板间通信，比如单片机和电脑，这个设备和另外一个设备之间的通信。而 I2C 多用于板内通信，比如单片机和我们本章要学的 EEPROM 之间的通信。

本章配套视频教程请查看：[第14章 I2C 总线与 EEPROM]()