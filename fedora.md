# Fedora 源使用帮助


### 地址

https://mirrors.shu.edu.cn/fedora/

### 说明


Fedora 软件源

### 收录架构


x86_64, i386

### 收录版本


所有仍在支持的版本和最新测试版本

### 使用说明

将以下保存为 `fedora-ustc.repo` ：

```bash
  [fedora] 
  name=Fedora $releasever - $basearch - ustc
  failovermethod=priority 
  baseurl=https://mirrors.shu.edu.cn/fedora/releases/$releasever/Everything/$basearch/os/ 
  #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=fedora-$releasever&arch=$basearch 
  enabled=1 
  metadata_expire=7d 
  gpgcheck=1 
  gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-fedora-$releasever-$basearch

  [fedora-debuginfo] 
  name=Fedora $releasever - $basearch - Debug - ustc
  failovermethod=priority 
  baseurl=https://mirrors.shu.edu.cn/fedora/releases/$releasever/Everything/$basearch/debug/ 
  #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=fedora-debug-$releasever&arch=$basearch 
  enabled=0 
  metadata_expire=7d 
  gpgcheck=1
  gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-fedora-$releasever-$basearch

  [fedora-source] 
  name=Fedora $releasever - Source - ustc
  failovermethod=priority 
  baseurl=https://mirrors.shu.edu.cn/fedora/releases/$releasever/Everything/source/SRPMS/ 
  #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=fedora-source-$releasever&arch=$basearch 
  enabled=0 
  metadata_expire=7d 
  gpgcheck=1 
  gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-fedora-$releasever-$basearch
```

将以下保存为 `fedora-updates-ustc.repo` ：

```bash
  [updates]
  name=Fedora $releasever - $basearch - Updates - ustc
  failovermethod=priority 
  baseurl=https://mirrors.shu.edu.cn/fedora/updates/$releasever/$basearch/ 
  #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=updates-released-f$releasever&arch=$basearch 
  enabled=1 
  gpgcheck=1 
  gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-fedora-$releasever-$basearch

  [updates-debuginfo] 
  name=Fedora $releasever - $basearch - Updates - Debug -ustc
  failovermethod=priority 
  baseurl=https://mirrors.shu.edu.cn/fedora/updates/$releasever/$basearch/debug/ 
  #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=updates-released-debug-f$releasever&arch=$basearch 
  enabled=0 
  gpgcheck=1 
  gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-fedora-$releasever-$basearch

  [updates-source] 
  name=Fedora $releasever - Updates Source - ustc
  failovermethod=priority 
  baseurl=https://mirrors.shu.edu.cn/fedora/updates/$releasever/SRPMS/ 
  #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=updates-released-source-f$releasever&arch=$basearch 
  enabled=0 
  gpgcheck=1 
  gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-fedora-$releasever-$basearch 
 ```

先备份 `/etc/yum.repos.d/fedora.repo` 和 `/etc/yum.repos.d/fedora-updates.repo`

将 `fedora-ustc.repo` 和 `fedora-updates-ustc.repo` 放入 `/etc/yum.repos.d/` 中。

运行 `sudo dnf makecache` 生成缓存。

### 相关链接

- 官方主页: https://getfedora.org/
- 邮件列表: https://fedoraproject.org/wiki/Communicating_and_getting_help
- 论坛: https://forums.fedoraforum.org/
- 文档: https://docs.fedoraproject.org/
- Wiki: https://fedoraproject.org/wiki/
- 镜像列表: https://admin.fedoraproject.org/mirrormanager