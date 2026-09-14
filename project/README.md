Controller API Procedures that upload an ISO from a Linux Worker and create
or boot a VM on Proxmox.

Create ISO always runs first. This Project expects the ISO named
`unattended_{newMachine.fqn}.iso` (Windows guest) or
`unattended_{newOsNode.fqn}.iso` (Linux guest).

`BIOS or UEFI` (`biosOrUefi`) must match that ISO. `Operating System Name`
(`operatingSystemName`) must match the ISO edition:

- `Windows 10`, `Windows Server 2016`, `Windows Server 2019` → ostype `win10`
- `Windows 11`, `Windows Server 2022` → ostype `win11`, plus TPM 2.0 on UEFI

UEFI uses OVMF on q35 with Secure Boot off so a rebuilt autounattend ISO can
start. Every guest uses SATA disks and an e1000 NIC so VirtIO drivers are not
required on the ISO. Default firmware `UEFI`, default edition `Windows 10`.

See the [Automate Operating System Installation Guide](https://attuneops.io/docs/topics/automated_os_installation.html).
