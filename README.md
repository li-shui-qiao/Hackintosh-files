## 黑苹果OC配置文件
* [硬件配置](#硬件配置)
* [实现功能](#实现功能)
* [存在问题](#未实现)

## 硬件配置
1. CPU：i5-10600K
2. GPU：Radeon RX 5500 XT
3. 主板：AsRock B460M-ITX/ac
4. 网卡和蓝牙：BCM94360NG:  

   * 注意：这张卡是魔改pcb从BCM94360上移植的，所以价格较贵。  
   不过好处就是接口就是NGFF M.2插到主板上就能用。觉得价格  
   太高的可以购买苹果拆机网卡配合转接器使用，不想用隔空投送  
   只考虑上网的可以直接购买USB网卡。
   
## 实现功能
* 正常睡眠，唤醒
* Handoff，Airdrop等白苹果功能正常实现
* GPU显示正常，无花屏
* USB接口设备识别正常
* Audio out正常，声音清晰
	
## 未实现
* Audio in未实现，使用layout_id=55。所有  
内置音频口都能出声，具体配置可通过Hackintool  
定制音频接口来完善
* 网络有时会出现大量延迟，可通过定制USB接口解决
* USB接口无法识别USB3.0设备，所有USB3.0设备都  
运行在480M
* USB接口给苹果设备充电异常。EC运行正常，AppleBusPowerController  
挂载正常，可通过定制USB接口解决

## 注意事项
* 已把序列号删除，需自行配置序列号防止被ban
* 根据自己硬件定制的Opencore文件是最适合的，遇到问题和所需工具都可以  
在Opencore官网找到：https://dortania.github.io/OpenCore-Install-Guide/
