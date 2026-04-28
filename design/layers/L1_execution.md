# L1 执行层  ·  Execution Layer
**版本** v0.1 · 2026.04（待写）

---

## 职责边界

L1 是机器人的"动"——以约 50Hz 的频率运行，负责：

- 接收 L2 的关节轨迹指令，输出关节力矩（1kHz）
- 全身控制（WBC）：TSID via Pinocchio
- 轨迹优化：MPC（Aligator/ProxDDP）
- 力/触觉反馈闭环
- EtherCAT 实时驱动（ODrive Pro / VESC 6）

**L1 不做**：任何语义推理——只处理数字信号。

---

## 参考组件

| 组件 | 规格 |
|------|------|
| 全身控制 | TSID via Pinocchio |
| 轨迹优化 | Aligator / ProxDDP |
| 实时内核 | PREEMPT_RT |
| 驱动总线 | EtherCAT |
| 电机驱动 | ODrive Pro / VESC 6 |
| 计算平台 | NVIDIA Jetson Thor 275 TOPS，JetPack 7.0 |

---

*待写*
