
# Obsidian 本地链接桥接
让你在任意地方 以 本地链接(`localhost`)的形式 打开指定的 Obsidian 笔记

## 首页     
[首页]提供转链服务 , 会将 Obsidian 笔记链接转换为本地桥接链接。
比如
```
obsidian://open?vault=DevWorld&file=03%20Doing%2FMissions.base
```
转换为：
- 明文链接
```
http://localhost/ob/?vault=DevWorld&file=03%20Doing%2FMissions.base
```
- Base64 链接
```
http://localhost/ob/?vault=DevWorld&b64=MDMgRG9pbmcvTWlzc2lvbnMuYmFzZQ%3D%3D
```

## 使用链接打开Obsidian对应的笔记
在任意支持点击"http://..." 链接的环境中，点击转换后的本地桥接链接即可直接打开 Obsidian 对应的笔记。
比如：
- 浏览器中
- `Win` + `R`
- 文件资源管理器
- 邮件正文中
- 文本编辑器中

## 部署方式
### 在IIS中部署
- 在默认网站下创建一个虚拟目录，命名为 `ob`
- 配置其物理路径为 当前项目的根目录
- 确保应用程序池的身份具有该目录的访问权限



