- 安装
```
gzip -d ./clash-linux-amd64-v1.11.4.gz
mv clash-linux-amd64-v1.11.4 clash #重命名
chmod u+x clash #赋权
./clash # 执行一次初始化
```
下载Country.mmdb
```
cd /root/.config/clash
wget https://github.com/Dreamacro/maxmind-geoip/releases/download/20220612/Country.mmdb
```
- 临时设置代理
```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
取消：
unset http_proxy https_proxy all_proxy

```
