Controller API Procedures that upload an ISO from a Linux Worker and create
or boot a VM on Proxmox.

Create ISO always runs first. This Project expects the ISO named
`unattended_{newMachine.fqn}.iso` (Windows guest) or
`unattended_{newOsNode.fqn}.iso` (Linux guest).

`BIOS or UEFI` (`biosOrUefi`) must match that ISO: `BIOS` creates a SeaBIOS VM;
`UEFI` creates an OVMF q35 VM with an EFI disk and TPM. Windows guests use
ostype `other` so the same recipe covers Windows 10, Windows 11, and
Windows Server. Default `UEFI`.

See the [Automate Operating System Installation Guide](https://attuneops.io/docs/topics/automated_os_installation.html).
