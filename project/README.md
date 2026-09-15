Controller API Procedures that upload an ISO from a Linux Worker and create
or boot a VM on Proxmox.

Create ISO always runs first. This Project expects the ISO named
`unattended_{newMachine.fqn}.iso` (Windows guest) or
`unattended_{newOsNode.fqn}.iso` (Linux guest).

`BIOS or UEFI` (`biosOrUefi`) must match that ISO: `BIOS` creates a SeaBIOS VM;
`UEFI` creates an OVMF VM (q35, EFI disk, and a TPM 2.0 device on Windows).
Default `UEFI`.

See the [Automate Operating System Installation Guide](https://attuneops.io/docs/topics/automated_os_installation.html).
