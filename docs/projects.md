# Project Map

Repository roles and their relationship to the roadmap stages.

仓库角色以及它们与长期路线图阶段的关系。

## Core Repositories

| Repository | Role | Primary Stage | Status |
| --- | --- | --- | --- |
| `xgen-roadmap` | Long-term engineering roadmap and lab planning | Organization | Active |
| `xgen-link` | Embedded device link and communication framework | Embedded Systems | Planned |
| `xgen-ota` | Production-oriented OTA framework | Embedded Systems | Planned |
| `xgen-docs` | Knowledge base for embedded, RTOS, Linux, ROS2, robotics, and AI | Organization | Planned |
| `xgen-zephyr-platform` | Zephyr-based robot MCU platform | RTOS | Planned |
| `xgen-linux-lab` | Embedded Linux driver and system learning lab | Embedded Linux | Planned |
| `xgen-balancebot` | BalanceBot-X modular robot MCU platform | Robotics | Planned |
| `xgen-ros2-lab` | ROS2 robotics experiments and architecture examples | ROS2 | Planned |

## Recommended Build Order

| Order | Repository | Why First |
| --- | --- | --- |
| 1 | `xgen-roadmap` | Keeps planning language, status rules, and project boundaries stable |
| 2 | `xgen-docs` | Gives every later repository a shared place for notes and decisions |
| 3 | `xgen-link` | Defines the device-to-host contract used by firmware, Linux, and robot software |
| 4 | `xgen-ota` | Establishes safe update assumptions before firmware platforms become complex |
| 5 | `xgen-zephyr-platform` | Turns embedded foundations into a reusable robot MCU platform |
| 6 | `xgen-linux-lab` | Builds host-side system knowledge needed for integration and diagnostics |
| 7 | `xgen-balancebot` | Integrates firmware, control, host communication, and ROS2 boundaries for the BalanceBot-X platform |
| 8 | `xgen-ros2-lab` | Expands robot behavior, simulation, and middleware patterns after hardware boundaries are clear |

推荐顺序：先稳定规划和知识库，再做设备链路、OTA、RTOS 平台，最后推进机器人集成和 ROS2 实验。

## Repository Responsibilities

### `xgen-roadmap`

Defines the long-term direction, project sequencing, and public planning language for X-Gen-Lab.

定义 X-Gen-Lab 的长期方向、项目推进顺序和公开规划语言。

### `xgen-docs`

Collects reusable knowledge, design notes, lab notes, and learning paths across all engineering stages.

沉淀跨阶段的知识库、设计笔记、实验记录和学习路径。

### `xgen-balancebot`

Acts as the flagship BalanceBot-X integration target that connects firmware, control, power, sensing, communication, Linux, ROS2, and AI extensions.

作为旗舰集成目标，连接固件、控制、Linux、ROS2 和 AI 扩展能力。

### `xgen-zephyr-platform`

Provides a reusable Zephyr-based MCU platform for robot control boards and production-oriented firmware work.

提供可复用的 Zephyr MCU 平台，用于机器人控制板和面向产品的固件工程。

### `xgen-linux-lab`

Builds practical embedded Linux capability through drivers, kernel modules, device tree, and system diagnostics.

通过驱动、内核模块、设备树和系统诊断建立嵌入式 Linux 实战能力。

### `xgen-ros2-lab`

Hosts ROS2 experiments, robot software patterns, simulation examples, and architecture prototypes.

承载 ROS2 实验、机器人软件模式、仿真示例和架构原型。

### `xgen-link`

Defines reusable embedded device link patterns for device, host, and robot integration.

定义可复用的嵌入式设备连接与通信模式，用于设备、主机和机器人集成。

### `xgen-ota`

Develops safe update mechanisms, bootloader integration patterns, image validation, and rollback strategies.

发展安全升级机制、Bootloader 集成模式、镜像校验和回滚策略。

## Dependency Direction

```text
xgen-roadmap
        |
xgen-docs
        |
xgen-link + xgen-ota
        |
xgen-zephyr-platform
        |
xgen-linux-lab
        |
xgen-balancebot
        |
xgen-ros2-lab
        |
Embodied AI experiments
```

`xgen-docs` supports all stages. `xgen-roadmap` coordinates the planning model and priority language.

`xgen-docs` 支撑所有阶段；`xgen-roadmap` 负责统一规划模型和优先级语言。

## Repository Readiness Checklist

Each repository should reach this baseline before it is treated as an active dependency:

| Item | Requirement |
| --- | --- |
| Purpose | README explains the repository's role in the roadmap |
| Boundary | Scope, non-scope, and upstream/downstream dependencies are clear |
| First usable artifact | A spec, sample, skeleton, or demo can be used by another repository |
| Validation | Build, test, render, or review command is documented |
| Decision record | Important architecture choices are captured in docs or ADRs |

每个仓库在成为其他项目的依赖前，都应该先达到这个最低可用标准。
