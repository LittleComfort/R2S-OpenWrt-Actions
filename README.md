# NanoPi R2S-OpenWrt-Actions

适用于 NanoPi R2S 的 GitHub Actions

使用 Lean 的源码

#### 默认登录地址及密码

- 192.168.1.1

  password

#### 建议的安全性设置

- 设置一个安全的密码：

  进入 系统➡️管理权 界面设置密码。


- 禁止从wan访问ssh，更换端口：

  进入 系统➡️管理权➡️SSH访问，将接口限制为 lan，将端口设置为其它非常用端口。


- 只允许本地设备访问Luci：

  编辑 /etc/config/uhttpd，将原来的0.0.0.0和[::]地址改为本地lan的地址。

  完成后重启服务：
  ```bash
  /etc/init.d/uhttpd restart
  ```
  😊
