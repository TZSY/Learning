有时会出现两个dock栏，是由自带的dock栏导致的。关闭extensions依然会出现。

```
sudo rm -rf /usr/share/gnome-shell/extensions/ubuntu-dock@ubuntu.com
```

删掉自带的dock即可，但是在Ubuntu更新后需要再执行一遍，因为更新会修复自带的dock。