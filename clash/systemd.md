```
sudo vim /etc/systemd/system/clash.service
填入以下内容：
[Unit]
Description=Clash daemon, A rule-based proxy in Go.
After=network.target

[Service]
Type=simple
Restart=always
ExecStart=/root/clash -d /root/.config/clash #前面为clash路径 后面接配置路径 

[Install]
WantedBy=multi-user.target
```
