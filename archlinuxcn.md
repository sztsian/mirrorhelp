# Arch Linux CN 源使用帮助

### 地址

https://mirrors.shu.edu.cn/archlinuxcn

### 说明

Arch Linux中文社区仓库是由Arch Linux中文社区驱动的非官方用户仓库。包含中文用户常用软件、工具、字体、美化包等。

### 使用方法

在`/etc/pacman.conf`文件末尾添加以下两行：

```bash
[archlinuxcn]
Server = https://mirrors.shu.edu.cn/archlinuxcn/$arch
```

之后安装`archlinux-keyring`包导入GPG key。

### 相关链接

- 官方主页：http://www.archlinuxcn.org/
- 官方仓库地址：http://repo.archlinuxcn.org