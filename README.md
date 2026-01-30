# Boot Assets

[English](README.md) | [中文](README_zh.md)

Bootloader and firmware files for Qualcomm-based RubikPi3 development board.

## File Description

### Bootloader

| File | Description |
|------|-------------|
| `xbl.elf` | XBL (eXtensible Boot Loader) primary bootloader |
| `xbl_config.elf` | XBL configuration |
| `xbl_config_gunyah.elf` | XBL Gunyah hypervisor configuration |
| `xbl_config_kvm.elf` | XBL KVM hypervisor configuration |
| `XblRamdump.elf` | XBL RAM dump utility |

### UEFI / TrustZone

| File | Description |
|------|-------------|
| `uefi.elf` | UEFI firmware |
| `uefi_sec.mbn` | UEFI security module |
| `tz.mbn` | TrustZone secure firmware |
| `hypvm.mbn` | Hypervisor virtual machine monitor |

### System Firmware

| File | Description |
|------|-------------|
| `aop.mbn` | AOP (Always On Processor) firmware |
| `cpucp.elf` | CPU co-processor firmware |
| `devcfg.mbn` | Device configuration |
| `qupv3fw.elf` | QUPv3 peripheral firmware |
| `shrm.elf` | Shared Resource Manager firmware |
| `imagefv.elf` | Firmware volume image |

### Flashing Tools

| File | Description |
|------|-------------|
| `prog_firehose_ddr.elf` | Firehose programmer (DDR version) |
| `prog_firehose_lite.elf` | Firehose programmer (lite version) |
| `rawprogram*.xml` | Partition flashing configuration |
| `patch*.xml` | Partition patch configuration |
| `gpt_main*.bin` | GPT main partition table |
| `gpt_backup*.bin` | GPT backup partition table |

### RubikPi3 Configuration

| File | Description |
|------|-------------|
| `RubikPi3_CDT.bin` | CDT (Configuration Data Table) |
| `rubikpi_config.img` | RubikPi configuration image |
| `rubikpi_dtso.img` | Device Tree Overlay image |
| `splash.img` | Boot splash screen |

## Usage

Use with flashing tools like QFIL or QDL to flash firmware via Firehose protocol.

## Notes

- Flashing firmware carries risks, ensure you understand the process
- Backup original firmware before flashing
- These firmware files are only compatible with RubikPi3 development board
