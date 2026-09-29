# XMAKB3M0P1B13 Unlocked BIOS

小米笔记本 Air13.3 2019款 BIOS 高级菜单解锁版。

本版本基于原版 InsydeH2O BIOS，主要解除厂商对高级设置菜单的隐藏限制，使 BIOS 中原本不可见的配置项目可以直接访问。

> ⚠️ 修改 BIOS 设置存在风险，请在了解选项作用并具备 BIOS 恢复能力的情况下使用。

---

## 解锁内容

解锁后主要增加 **Advanced 高级设置菜单**，可以访问更多 CPU、芯片组、电源和设备相关配置。

### CPU Configuration

可查看和调整更多处理器相关选项，例如：

```text
CPU Power Management
Intel SpeedStep
Intel Turbo Boost
CPU C-States
Hyper-Threading
Config TDP
CPU Power Limit
Thermal Configuration
```

部分 Intel 通用处理器调试项目也会显示。

---

## Power Management

增加更多电源管理相关设置，例如：

```text
CPU Power Management
C-State Configuration
Package C-State
Turbo Power Limit
Config TDP
Platform Power Management
ACPI Configuration
```

可用于研究性能、功耗和待机策略。

---

## System Agent Configuration

可以访问原本隐藏的 System Agent 设置，包括：

```text
System Agent Configuration
Memory Configuration
Graphics Configuration
VT-d
Graphics / GT Settings
Memory Related Settings
```

部分项目属于 Intel 通用平台设置，实际是否生效取决于处理器和主板硬件。

---

## PCH Configuration

解锁 Intel PCH 芯片组相关设置，例如：

```text
PCH Configuration
PCI Express Configuration
SATA Configuration
USB Configuration
HD Audio Configuration
Serial IO Configuration
GPIO Configuration
```

可以查看更多主板底层硬件配置。

---

## PCI Express Configuration

解锁更多 PCIe Root Port 设置。

常见选项包括：

```text
PCIe Root Port Enable / Disable
PCIe Link Speed
ASPM
L1 Substates
Hot Plug
CLKREQ
PCIe Power Management
PCIe Storage Configuration
RST Remapping
```

可用于 PCIe 设备和接口调试。

---

## Storage Configuration

增加更多存储相关设置，例如：

```text
SATA Configuration
PCIe Storage Configuration
NVMe Related Settings
Intel RST Configuration
PCIe Storage Remapping
```

---

## USB Configuration

可以访问更多 USB 控制器相关设置，例如：

```text
USB Configuration
USB Port Enable / Disable
USB Legacy Support
USB Power Management
xHCI Configuration
```

---

## Serial IO Configuration

解锁 Intel Serial IO 相关设置：

```text
I2C
SPI
UART
```

可以查看或调整不同控制器的启用状态和部分工作参数。

---

## GPIO Configuration

增加 GPIO 相关高级配置页面。

该部分属于主板底层硬件设置，可能与：

```text
设备复位
电源控制
I2C / SPI
PCIe
USB
摄像头
触摸板
无线设备
```

等硬件相关。

不建议在不了解具体 GPIO 用途的情况下修改。

---

## Audio Configuration

解锁更多音频相关设置，例如：

```text
HD Audio Configuration
HD Audio Advanced Settings
DSP Configuration
Audio Controller Settings
```

---

## Intel ME / Security

可以访问部分 Intel Management Engine 和安全相关设置，例如：

```text
Intel ME Configuration
Firmware Update Configuration
PTT Configuration
ME Debug Configuration
Trusted Computing
```

部分项目可能仍然受到 ME 固件或平台策略限制。

---

## Overclocking / Performance

固件中包含 Intel 通用性能和超频设置页面，例如：

```text
Processor
Memory
GT
Uncore
Voltage
PLL
Platform Voltage
```

部分项目在解锁后可以显示。

需要注意：

> 菜单能够显示，不代表当前 CPU 一定支持对应功能。

锁倍频移动处理器可能会忽略部分超频参数。

---

## Thermal Configuration

可访问更多散热和温度相关设置，例如：

```text
Thermal Configuration
CPU Thermal Management
DPTF
Thermal Trip
Power / Thermal Policy
```

实际风扇控制仍可能由 EC 独立管理。

---

## Debug / Platform Settings

解锁版还可以看到更多用于平台开发和调试的项目，例如：

```text
Debug Configuration
Platform Configuration
Policy Configuration
Firmware Configuration
Hardware Monitor
```

这些通常是 Insyde / Intel 平台开发阶段保留下来的高级项目。

---

## 注意事项

解锁高级菜单并不会改变硬件本身的能力。

部分设置来自 Intel / Insyde 通用 BIOS 模板，因此可能存在：

```text
菜单存在但硬件不存在
菜单可以修改但设置不会生效
修改后 BIOS 自动恢复默认值
某些选项只适用于其他平台版本
```

建议只修改明确了解用途的项目。

尤其谨慎修改：

```text
CPU Voltage
Memory Voltage
PLL
GPIO
PCIe Lane
HSIO
Intel ME
Platform Voltage
Clock
Reset Signal
```

错误配置可能导致无法启动。

---

## Recovery

强烈建议在刷写或修改 BIOS 前：

```text
备份完整 SPI Flash
准备 SPI 编程器
保留原始 BIOS Dump
记录默认设置
```

如果错误设置导致无法进入 BIOS，可以通过恢复默认 NVRAM、清除 CMOS 或使用 SPI 编程器恢复原始固件。

---

