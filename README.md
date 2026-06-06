# X-Gen-Lab Roadmap

Long-term engineering roadmap and lab planning for X-Gen-Lab.

X-Gen-Lab 的长期工程路线图与实验室规划仓库。

## Purpose

This repository defines how X-Gen-Lab grows from embedded foundations to robotics and embodied intelligence. It is not a quarterly delivery tracker. It is a durable planning map for choosing projects, sequencing technical work, and keeping the lab's public repositories aligned.

本仓库用于定义 X-Gen-Lab 如何从嵌入式基础逐步演进到机器人与具身智能方向。它不是季度交付表，而是一份长期稳定的工程规划地图，用来指导项目选择、技术推进顺序和公开仓库之间的协同关系。

## Roadmap Model

```text
Embedded Systems -> RTOS -> Embedded Linux -> ROS2 -> Robotics -> Embodied AI
```

Each stage builds reusable capabilities for the next stage:

| Stage | Focus | Outcome |
| --- | --- | --- |
| Embedded Systems | MCU firmware, board bring-up, protocols, OTA | Reliable device foundations |
| RTOS | Zephyr, FreeRTOS, drivers, IPC, scheduling | Production-ready firmware architecture |
| Embedded Linux | Drivers, device tree, kernel modules, services | System-level integration |
| ROS2 | Nodes, messages, simulation, navigation, tooling | Robot software middleware |
| Robotics | Control, sensing, localization, robot platforms | Integrated robot systems |
| Embodied AI | Vision, edge AI, agents, perception | Intelligence connected to physical machines |

每个阶段都会沉淀下一阶段需要复用的能力：

| 阶段 | 重点 | 产出 |
| --- | --- | --- |
| 嵌入式系统 | MCU 固件、板级启动、协议、OTA | 可靠的设备基础 |
| RTOS | Zephyr、FreeRTOS、驱动、IPC、调度 | 面向产品的固件架构 |
| 嵌入式 Linux | 驱动、设备树、内核模块、系统服务 | 系统级集成能力 |
| ROS2 | 节点、消息、仿真、导航、工具链 | 机器人软件中间件 |
| 机器人 | 控制、感知、定位、机器人平台 | 集成机器人系统 |
| 具身智能 | 视觉、边缘 AI、智能体、感知 | 连接物理机器的智能能力 |

## How To Read This Repository

- [docs/roadmap.md](docs/roadmap.md): long-term roadmap by engineering stage.
- [docs/projects.md](docs/projects.md): repository-to-stage mapping and project roles.
- [docs/milestones.md](docs/milestones.md): near-term milestone board for active planning.
- [docs/planning-model.md](docs/planning-model.md): status rules, maturity gates, and execution rhythm.

## Priority Tracking

Project priority is tracked with four lightweight states:

| Status | Meaning |
| --- | --- |
| Active | Current planning or implementation focus |
| Planned | Intended project, not yet the main workstream |
| Backlog | Useful idea that needs more validation |
| Deferred | Explicitly postponed to keep the current focus narrow |

优先级使用四个轻量状态跟踪：

| 状态 | 含义 |
| --- | --- |
| Active | 当前规划或实现重点 |
| Planned | 已确定方向，但还不是主要工作流 |
| Backlog | 有价值但仍需要验证的想法 |
| Deferred | 为了保持当前聚焦而明确推迟 |

## Execution Strategy

The roadmap is implemented from reusable foundations toward visible robot outcomes:

```text
xgen-roadmap -> xgen-docs -> xgen-link / xgen-ota -> xgen-zephyr-platform -> xgen-balancebot -> xgen-ros2-lab -> AI experiments
```

The best implementation path is to make each repository useful on its own before using it as a dependency in the next stage.

最佳实现路径是先让每个仓库自身可用，再把它作为下一阶段项目的依赖能力。

## Planning Principles

- Build real systems, not isolated demos.
- Document engineering decisions as the system evolves.
- Prefer reusable architecture over one-off experiments.
- Connect low-level control with high-level intelligence.

## License

MIT License. See [LICENSE](LICENSE).
