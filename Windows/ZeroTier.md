# ZeroTier

## 1.  Windows 系统下 `ping` 命令不能正常工作

1.1 打开 Windows Defender 防火墙；

1.2 点击进入高级设置，在入站规则中查找 “文件和打印机共享(回显请求 - ICMPv4-In)” ，共有2项；

1.3 右键单击各项选择启用规则，设置完毕后再执行 `ping` 命令就可以正常工作了。

**ZeroTier**官网解决方法[Troubleshooting & FAQ](https://docs.zerotier.com/zerotier/troubleshooting/)原文如下：

> **Ping is not working**
>
> First, make sure your device is authorized on the network and you're using the ZeroTier assigned Managed IP address. Aside from that, some OSes block  pings in their local firewall by default.
>
> **Windows**
>
> Windows does block pings by default. To enable pings on Windows, follow the following steps
>
> 1. Click the search bar on your taskbar and search for "Windows Firewall" then click it to open
> 2. Click "Advanced Settings" on the left.
> 3. From the left pane of the resulting window, click "Inbound Rules"
> 4. In the right pane, find the rules titled "File and Printer Sharing (Echo Request - ICMPv4-In).
> 5. Right click each rule and choose "Enable Rule"