# FIO-SPDK脚本使用说明


此工具主要应用于NVMe SSD测试，单盘测试默认可覆盖多种IO模型，也可根据需求自定义IO模型

集成自动化测试与数据整理一体

此工具内部包含：

- 硬盘信息收集工具
- fio测试工具
- fio测试配置文件
- spdk工具



## 目录

- 注意事项与帮助
- 选择配置文件
- nvme、spdk模式
- 绑核、绑numa
- 单盘、多盘测试



## 注意事项与帮助

> 使用spdk模式测试时请使用Centos8.5或更换内核版本到4.18.0-348.7.1.el8_5.x86_64（CentOS Linux release 8.5.2111）或更新

```shell
example:
 ./fio-spdk.sh [-t nvme|spdk] -d "nvme0n1 nvme1n1" [-c "0-7 8-15" | -n "0 1"] [-j job_cfg_file]
         -t: nvme|spdk, test using nvme driver or spdk. default is nvme. optional
         -d: drive list. mandatory option
         -c: cpu core bind list. bind list is corresponding to drive list. optional
         -n: numa node bind list. -n takes precendence when both -c and -n are used. optional
         -j: job config file. default config file is "job_cfg_common". optional
```

