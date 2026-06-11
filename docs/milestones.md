# Milestones

Near-term milestone board for X-Gen-Lab planning.

X-Gen-Lab 近期规划里程碑。

## Foundation Track

| Milestone | Outcome | Status |
| --- | --- | --- |
| Publish organization profile | Clear public identity and project map | Active |
| Complete roadmap repository | Durable planning source for lab direction | Active |
| Define planning model | Status rules, maturity gates, and execution rhythm | Active |
| Create knowledge-base structure | Shared docs home for notes and decisions | Planned |

基础方向目标：先建立公开身份、路线图和知识沉淀结构，让后续项目有统一入口。

## Platform Track

| Milestone | Outcome | Status |
| --- | --- | --- |
| Define xgen-link framework scope | Framing, IDs, payload conventions, host tools | Planned |
| Define OTA framework scope | Bootloader model, update flow, rollback behavior | Planned |
| Define Zephyr platform scope | Board, driver, configuration, and test boundaries | Planned |

平台方向目标：形成可复用的 MCU、协议和升级能力，为机器人项目提供底座。

## Robotics Track

| Milestone | Outcome | Status |
| --- | --- | --- |
| Define BalanceBot-X V1 architecture | Firmware, control loop, sensors, host integration, platform boundaries | Planned |
| Create ROS2 lab skeleton | Nodes, launch files, simulation examples | Planned |
| Connect platform work to robot target | MCU platform and xgen-link work mapped to BalanceBot-X | Planned |

机器人方向目标：以 BalanceBot-X 为主线，把底层平台、通信、安全和 ROS2 能力连接到真实系统。

## AI Track

| Milestone | Outcome | Status |
| --- | --- | --- |
| Define vision robot demo | Camera, perception, and robot command boundary | Backlog |
| Define edge AI runtime target | Jetson or equivalent local inference platform | Backlog |
| Define embodied AI experiment loop | Dataset capture, evaluation, and iteration process | Backlog |

AI 方向目标：先保持为探索项，在机器人平台稳定后逐步进入可验证实验。

## Status Rules

| Status | Use When |
| --- | --- |
| Active | Work is currently being planned or implemented |
| Planned | Work is accepted but not yet the main focus |
| Backlog | Work is promising but needs more validation |
| Deferred | Work is intentionally postponed to protect current focus |

状态规则用于避免把所有想法都标成同等优先级。

## Near-Term Execution Order

| Step | Focus | Expected Result |
| --- | --- | --- |
| 1 | Finish `xgen-roadmap` baseline | Public planning source is complete enough to guide other repositories |
| 2 | Create `xgen-docs` skeleton | Shared knowledge base exists before technical repositories multiply |
| 3 | Specify `xgen-link` | Device link contract is available for firmware, host, and robot integration |
| 4 | Specify `xgen-ota` | Firmware update assumptions are clear before platform implementation |
| 5 | Start `xgen-zephyr-platform` | Reusable MCU platform begins with known link and OTA boundaries |
| 6 | Start `xgen-balancebot` BalanceBot-X architecture | Robot integration target has stable platform dependencies |

近期最优路径：先把规划、文档、链路和 OTA 这些基础能力做稳，再进入 Zephyr 平台和 BalanceBot-X 集成。
