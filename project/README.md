Controller API Procedures that upload an ISO from a Linux Worker and create
or boot a VM on Proxmox.

Create ISO always runs first. This Project expects the ISO named
`unattended_{newMachine.fqn}.iso` (Windows guest) or
`unattended_{newOsNode.fqn}.iso` (Linux guest).

See the [Automate Operating System Installation Guide](https://attuneops.io/docs/topics/automated_os_installation.html).
