# 简介
* 支持Type C有线及WiFi STA、WiFi AP无线使用；
* J-Link：OB-STM32F072-CortexM；
* 主控：全志V831；
* WiFi+BT：XR829（BT暂未使用）；
* PMU：AXP2101；
* 输出支持短路保护；
# 使用方法
## 开关机
    长按POWER按键。
## USB
    长按KEY键，将模式切换到STATE灯熄灭，进入USB模式，此模式与普通J-Link功能相同；
## WiFi STA
    长按KEY键，将模式切换到STATE灯慢闪，此模式J-Link WiFi将通过WEB配置的SSID和密码连接AP。
    未连接时，ERROR灯闪烁，连接成功后，ERROR灯熄灭；
    当前仅支持通过DHCP获取IP，可在AP设备列表中查看J-Link WiFi的IP地址，也可将WiFi WiFi切换到AP模式，并在WEB中查看之前获取到的IP地址。
## WiFi AP
    长按KEY键，将模式切换到STATE灯快闪，此模式J-Link WiFi将作为AP，SSID为J-Link_XXXXXXXX，密码为jlink，J-Link WiFi自身IP为192.168.1.1。
