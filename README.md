# ZYNQ_CARRY4_TDC
Implement a time to digital converter for timing signals, construct a 156 level delay chain using CARRY4 module, combine LUT6 precoding and additive tree decoding mechanism, and ultimately achieve sub nanosecond time resolution.

\**链接**\
	芯片官方文档下载;https://adaptivesupport.amd.com/s/?language=zh_CN#documentation
 \*\
	AMD技术信息门户网站:https://docs.amd.com/p/design-hubs-c
 \*\
	邮箱：1617245902@qq.com


\**参数信息**\
	Board:Xilinx Zynq-7020 FPGA（主芯片XC7Z020CLG484）\
	Working frequency of TDC: 200 MHz\
	The number of stages in the delay chain: 156 \
	RMS: < 200 ps\
	DNL: -1 to +3.65 LSB\
	INL: -13.26 to +6.5 LSB\
	FWHM: < 400 ps\
	Time measurement range: 83 s\
	Dead time: ~20 ns


\**目录结构**\
	\**************** board ****************\
	芯片手册，开发板原理图，用户手册

	\**************** code ****************\
	PL端包含：AXI_BRAM控制器、AXI连接器、BRAM块随机存储，TDC核心功能ip核
	PS端包含：文件系统挂载，读写SD卡，中断系统
	工程代码层级说明图片

	\**************** config ****************\
	控制器配置、系统资源配置、VHDL时序约束、端口配置

	\**************** figure ****************\
	Delay_Chain：CARRY4模块图、延时链原理图、延时链级联结构图、vivado布局图
	Encoder：温度计码译码分组结构、LUT6布局、数据状态机
	ILA结果图、TDC系统框图、系统Block Design视图、上位机视图

	\****************test****************\
	测试性能参数的matlab代码：FWHM\RMS\INL\DNL\LSB
