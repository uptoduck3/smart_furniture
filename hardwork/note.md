# 硬件部分学习笔记

问：时钟晶振和旁路时钟源的区别

旁路时钟源和时钟晶振都是用于提供时钟信号的元件，但它们的作用和工作原理有所不同。

时钟晶振是一种电子元件，它利用晶体振荡的特性来产生稳定的时钟信号。晶振的频率通常在几千赫兹到几百兆赫兹之间，可以通过外部电路进行调节。时钟晶振通常用于计算机、通信设备、电子钟表等需要高精度时钟信号的场合。

旁路时钟源是一种电路设计技术，它通过在系统中添加一个独立的时钟源来提供时钟信号，以保证系统的稳定性和可靠性。旁路时钟源通常由一个独立的时钟发生器和一个时钟选择器组成，可以选择使用内部时钟信号或外部时钟信号。旁路时钟源通常用于需要高可靠性和高稳定性的系统，如航空航天、军事、医疗等领域。

因此，时钟晶振和旁路时钟源虽然都是用于提供时钟信号的元件，但它们的应用场合和工作原理有所不同。

问：stm32f103使用hal库时使用led时，把gpio设置为pull-up和pull-down有什么区别？

在使用STM32F103芯片时，GPIO可以设置为三种模式：输入模式、输出模式和复用模式。在输出模式下，可以设置GPIO的输出类型和输出速度，同时还可以设置GPIO的上拉和下拉电阻。

当GPIO被设置为输出模式时，上拉和下拉电阻的作用是在GPIO输出低电平或高电平时提供一个稳定的电平。具体来说，当GPIO被设置为上拉时，当GPIO输出低电平时，上拉电阻会将GPIO拉高到VDD电平，当GPIO输出高电平时，上拉电阻不会对GPIO产生影响。相反，当GPIO被设置为下拉时，当GPIO输出高电平时，下拉电阻会将GPIO拉低到GND电平，当GPIO输出低电平时，下拉电阻不会对GPIO产生影响。

因此，当使用LED时，如果将GPIO设置为上拉，当GPIO输出低电平时，LED将会亮起，当GPIO输出高电平时，LED将会熄灭。相反，如果将GPIO设置为下拉，当GPIO输出高电平时，LED将会亮起，当GPIO输出低电平时，LED将会熄灭。

总之，选择上拉还是下拉电阻取决于具体的应用场景和硬件连接方式

问：什么情况下使用DMA

当需要传送的数据量比较大的时候来使用DMA来节约CPU的资源。

## 按键和LED原理

所有的开漏输出都需要接上拉电阻