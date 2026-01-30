# Boot Assets

[English](README.md) | [中文](README_zh.md)

本仓库存放 Qualcomm 平台 RubikPi3 开发板的 bootloader 及相关固件文件，用于系统启动和刷机。

## 文件说明

### Bootloader

| 文件 | 说明 |
|------|------|
| `xbl.elf` | XBL (eXtensible Boot Loader) 主引导程序 |
| `xbl_config.elf` | XBL 配置文件 |
| `xbl_config_gunyah.elf` | XBL Gunyah 虚拟化配置 |
| `xbl_config_kvm.elf` | XBL KVM 虚拟化配置 |
| `XblRamdump.elf` | XBL 内存转储工具 |

### UEFI / TrustZone

| 文件 | 说明 |
|------|------|
| `uefi.elf` | UEFI 固件 |
| `uefi_sec.mbn` | UEFI 安全模块 |
| `tz.mbn` | TrustZone 安全固件 |
| `hypvm.mbn` | Hypervisor 虚拟机监控程序 |

### 系统固件

| 文件 | 说明 |
|------|------|
| `aop.mbn` | AOP (Always On Processor) 固件 |
| `cpucp.elf` | CPU 协处理器固件 |
| `devcfg.mbn` | 设备配置 |
| `qupv3fw.elf` | QUPv3 串口外设固件 |
| `shrm.elf` | 共享资源管理器固件 |
| `imagefv.elf` | 固件卷镜像 |

### 刷机相关

| 文件 | 说明 |
|------|------|
| `prog_firehose_ddr.elf` | Firehose 刷机程序 (DDR 版) |
| `prog_firehose_lite.elf` | Firehose 刷机程序 (精简版) |
| `rawprogram*.xml` | 分区刷写配置 |
| `patch*.xml` | 分区补丁配置 |
| `gpt_main*.bin` | GPT 主分区表 |
| `gpt_backup*.bin` | GPT 备份分区表 |

### RubikPi3 配置

| 文件 | 说明 |
|------|------|
| `RubikPi3_CDT.bin` | CDT (Configuration Data Table) |
| `rubikpi_config.img` | RubikPi 配置镜像 |
| `rubikpi_dtso.img` | 设备树 Overlay 镜像 |
| `splash.img` | 开机画面 |

## 使用方式

配合 QFIL 或 QDL 等刷机工具使用，通过 Firehose 协议将固件刷写到设备。

## 注意事项

- 刷机有风险，请确保了解操作流程
- 建议在刷机前备份原有固件
- 本仓库固件仅适用于 RubikPi3 开发板
