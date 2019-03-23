## 使用Docker编译openwrt widora系统

### 编译方法
# 1. 安装配置Docker
根据不同的主机操作系统安装配置Docker，并启动运行。

# 2. 用git下载文件
$ git clone https://github.com/leo421/openwrt_widora_docker.git

# 3. 更新feeds
$ cd openwrt_widora_docker<br>
$ ./widora.sh ./scripts/feeds update -a<br>
$ ./widora.sh ./scripts/feeds install -a<br>

# 4. 配置
$ ./widora.sh make menuconfig

# 5. 编译
$ ./widora.sh make V=s -j4

# 6. image文件
编译后生成的image文件在如下目录中： <br>
openwrt_widora/bin/ramips/: <br>
openwrt-ramips-mt7688-Widoraxxxxx-squashfs-sysupgrade.bin

### 提示
##### 1. 如果安装过程中，有些包无法下载，可以去 http://119.27.163.136:88 找一下，下载后放到opwnwrt_widora/dl目录中。

