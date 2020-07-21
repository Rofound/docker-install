# docker 安装指南

## windows 10

### 已安装了 VMware WorkStation

- 从官网下载 window 版 docker 安装器
- 解决Hyper-v和Vmware的共存问题
  - 使用管理员打开 `cmd`
  - 输入指令 `bcdedit /copy {default} /d "Window 10 without Hyper-V"`   // 参数说明：Window 10 without Hyper-V 支持自定义。输出一个ID，复制这个ID。
  - 输入指令 `bcdedit /set {ID-Number} hypervisorlaunchtyper off` // 这里的 ID-Number 就是上文提到的ID

### 未安装 VMware WorkStation

- 从官网下载 window 版 docker 安装器

### 可能出现的问题

- Q: hyper-v导致docker无法启动问题， 原因windows已经开启了hyper-v
- A:
  - 用管理员身份打开 `cmd`
  - bcdedit /set hypervisorlaunchtype off // 禁用hyper-v
  - bcdedit /set hypervisorlaunchtype auto // 重新启用hyper-v
  
## windows 7

- 安装 Docker Toolbox
  - 安装地址：`http://mirrors.aliyun.com/docker-toolbox/windows/docker-toolbox/?spm=5176.8351553.0.0.4bc61991tQpsnV`

## 参考链接

- `https://www.runoob.com/docker/windows-docker-install.html`
- `https://www.cnblogs.com/baby-lily/p/10966992.html`
