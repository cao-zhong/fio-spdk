# fio-spdk
NVMe SSD test scripts, support both conventional test on top block dev and SPDK
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

> 使用spdk模式测试时请使用Centos8.5或更换与Centos8.5内核版本相同或更新的版本使用

