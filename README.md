# SLAM_PYNQ 2020年新工科联盟-Xilinx暑期学校项目。
同步建图与定位（Simultaneous Location and Mapping，SLAM）是智能体在未知领域获得自身位置并记录运行轨迹的自主探索方法。目前 SLAM 系统已经融入大众的生活，比如自动驾驶汽车、SONY 的 AR 游戏设备、地震现场的无人机伤员救援以及军事领域的目标跟踪。但是，时下的 SLAM 系统都具有较大的计算量，仅在具有强大算力的 CPU 和 GPU 平上才能够实现实时处理。因此，无法将这些算法部署在计算能力受限的微型机器人平台上。
为了解决时下的 SLAM 系统都具有较大的计算量，仅在具有强大算力的 CPU 和 GPU平台上才能够实现实时处理的问题，本项目提出了一个软硬件协同设计的加速器架构 HCA- SLAM（Hardware-software Codesigned Accelerator for SLAM）。HCA-SLAM 架构的硬件数据流与软件完全匹配，并通过将 ORB SLAM2 中并行度较高且重复计算量大的特征点提取和匹配部分发送到自定义的硬件加速器并行执行来实现整体的加速。
HCA-SLAM首先通过HLS 工具设计并将其中核心模块更改为自主设计的verilog IP以满足快速prototype和性能优化的目标。
