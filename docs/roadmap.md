# Engineering Roadmap

Long-term roadmap for moving from embedded foundations to embodied intelligence.

从嵌入式基础走向具身智能的长期工程路线图。

## Stage 01: Embedded Systems

| Area | Target | Maturity Goal |
| --- | --- | --- |
| MCU firmware | STM32, ESP32, nRF52/nRF53 foundations | Repeatable board bring-up and firmware structure |
| Device link | Command framing, serialization, host tools | Reusable device communication patterns |
| OTA | Bootloader, image validation, rollback strategy | Safe update path for real devices |
| Low power | Sleep modes, wake sources, measurement | Power-aware firmware design |

阶段目标：建立可靠的 MCU 工程基础，为后续 RTOS、协议栈和机器人控制板提供底层能力。

Recommended first deliverables:

| Deliverable | Repository | Done When |
| --- | --- | --- |
| Device link specification | `xgen-link` | Frame format, command ID policy, payload rules, and host examples are documented |
| OTA design baseline | `xgen-ota` | Boot flow, image validation, rollback model, and target assumptions are documented |
| Firmware style baseline | `xgen-docs` | Board bring-up, logging, error handling, and test conventions are documented |

## Stage 02: RTOS Platforms

| Area | Target | Maturity Goal |
| --- | --- | --- |
| Zephyr platform | Board support, drivers, configuration | Reusable robot MCU platform |
| FreeRTOS patterns | Tasks, queues, timers, synchronization | Clear concurrency model |
| Driver abstraction | GPIO, I2C, SPI, UART, ADC, PWM | Portable peripheral access |
| Power management | Device states, runtime PM, sleep policy | Production-ready firmware behavior |

阶段目标：把单板固件能力提升为可复用、可配置、可测试的 RTOS 平台能力。

Recommended first deliverables:

| Deliverable | Repository | Done When |
| --- | --- | --- |
| Zephyr platform skeleton | `xgen-zephyr-platform` | Board layout, driver boundary, sample app, and build instructions exist |
| Driver abstraction notes | `xgen-docs` | GPIO, I2C, SPI, UART, ADC, and PWM conventions are captured |
| Robot control board target | `xgen-balancebot` | MCU responsibilities and host communication boundary are defined |

## Stage 03: Embedded Linux

| Area | Target | Maturity Goal |
| --- | --- | --- |
| Kernel drivers | Char devices, platform drivers, interrupts | Practical Linux driver capability |
| Device tree | Board description, overlays, bindings | Hardware integration literacy |
| System services | Boot, networking, logging, diagnostics | Maintainable embedded Linux runtime |
| Performance | Latency, memory, tracing, profiling | Observable system behavior |

阶段目标：建立 Linux 侧的驱动、系统集成和诊断能力，为上层 ROS2 和机器人平台提供稳定运行环境。

Recommended first deliverables:

| Deliverable | Repository | Done When |
| --- | --- | --- |
| Driver learning track | `xgen-linux-lab` | Char device, platform driver, interrupt, and device tree examples are organized |
| System diagnostics notes | `xgen-docs` | Boot logs, tracing, networking, and service diagnostics are documented |
| Host bridge assumptions | `xgen-balancebot` | Linux host role and MCU link contract are clear |

## Stage 04: ROS2

| Area | Target | Maturity Goal |
| --- | --- | --- |
| ROS2 basics | Nodes, topics, services, actions | Clean robot software building blocks |
| Simulation | Gazebo, RViz, URDF, sensor models | Repeatable robot experiments |
| Navigation | Localization, mapping, path planning | Robot autonomy foundation |
| Tooling | Launch files, bags, diagnostics | Efficient development workflow |

阶段目标：把设备控制、传感器数据和机器人行为连接到 ROS2 软件体系中。

Recommended first deliverables:

| Deliverable | Repository | Done When |
| --- | --- | --- |
| ROS2 lab skeleton | `xgen-ros2-lab` | Node, launch, message, and simulation examples exist |
| Robot interface model | `xgen-balancebot` | Topics, services, and link bridge responsibilities are defined |
| Simulation baseline | `xgen-ros2-lab` | RViz/Gazebo workflow can be followed from documentation |

## Stage 05: Robotics

| Area | Target | Maturity Goal |
| --- | --- | --- |
| BalanceBot-X | Modular robot MCU control platform | Integrated firmware-control-ROS2 system |
| Motor control | PWM, encoder, PID, safety limits | Stable motion control |
| Sensor fusion | IMU, odometry, filtering | Reliable state estimation |
| System integration | MCU, Linux host, ROS2 bridge | End-to-end robot architecture |

阶段目标：构建真实机器人平台，把底层控制、系统软件和中间件联成完整工程闭环。

Recommended first deliverables:

| Deliverable | Repository | Done When |
| --- | --- | --- |
| BalanceBot-X V1 architecture | `xgen-balancebot` | Firmware, control loop, sensor fusion, platform services, host, and ROS2 boundaries are documented |
| Control loop baseline | `xgen-balancebot` | Motor, encoder, IMU, PID, safety, and fallback assumptions are defined |
| Integration checklist | `xgen-docs` | Firmware-to-ROS2 bring-up sequence is reusable |

## Stage 06: Embodied AI

| Area | Target | Maturity Goal |
| --- | --- | --- |
| Vision | Camera pipeline, object detection, tracking | Perception-ready robot platform |
| Edge AI | Jetson or edge accelerator experiments | Local AI inference capability |
| Agents | Task planning, tool use, robot command bridge | AI-assisted robot behavior |
| Learning loops | Dataset capture, evaluation, iteration | Measurable intelligence experiments |

阶段目标：在真实机器上连接感知、规划和执行，让 AI 能力进入可验证的物理系统。

Recommended first deliverables:

| Deliverable | Repository | Done When |
| --- | --- | --- |
| Vision demo definition | `xgen-docs` | Camera, model, latency, and robot command boundary are defined |
| Edge runtime target | Future AI repository | Compute target and inference constraints are selected |
| Evaluation loop | `xgen-docs` | Dataset capture, metrics, and replay process are documented |
