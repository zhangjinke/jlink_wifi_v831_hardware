# 简介
* 支持Type C有线及WiFi STA、WiFi AP无线使用；
* J-Link：OB-STM32F072-CortexM；
* 主控：全志V831；
* WiFi+BT：XR829（BT暂未使用）；
* PMU：AXP2101；
* 输出支持短路保护；
# J-Link参数
* 内核支持：Cortex-M；
* 接口支持：SWD、VCOM；
* SWD速度：2MHz；
* VCOM波特率：2400bps~1Mbps；
* 支持自动升级。
# 使用方法
## 开关机
    长按POWER按键。
## USB
    长按KEY键，将模式切换到STATE灯熄灭，进入USB模式，此模式与普通J-Link功能相同；
## WiFi STA
    长按KEY键，将模式切换到STATE灯慢闪，此模式J-Link WiFi将通过WEB配置的SSID和密码连接AP。
    未连接时，ERROR灯闪烁，连接成功后，ERROR灯熄灭；
    当前仅支持通过DHCP获取IP。IP查看方法：
    1. 通过Tools内的C2000 Software搜索设备；
    2. 在AP设备列表中查看J-Link WiFi的IP地址；
    3. 将J-Link WiFi切换到AP模式，并在WEB中查看之前获取到的IP地址。
## WiFi AP
    长按KEY键，将模式切换到STATE灯快闪，此模式J-Link WiFi将作为AP，SSID为J-Link_XXXXXXXX，密码为jlink，J-Link WiFi自身IP为192.168.1.1。
## WEB
### 主页面
    使用浏览器访问J-Link WiFi的IP，可进入主页面。在主页面左上角可查看电池剩余电量、电池电压、充电状态、STA模式时的WiFi RSSI、J-Link S/N。主页面右上角可查看J-Link WiFi型号与软件版本号。
    中间为密码输入框，密码为12345678，输入密码并点击确认后，可进入网络配置页面。
### 网络配置页面
    在此页面可查看设备MAC地址，配置STA模式时连接的SSID和密码。
### MAC地址设置页面
    访问IP/m可进入MAC地址设置页面，在此页面可查看设备当前MAC地址，以及修改MAC地址，点击修改按钮后，设备将自动重启。