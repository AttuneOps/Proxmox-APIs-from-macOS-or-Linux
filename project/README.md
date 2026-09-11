Controller API Procedures that upload an ISO from a Linux Worker and create
or boot a VM on Proxmox.

Create ISO always runs first. This Project expects the ISO at
`unattended_{newLinuxMachine.fqn}.iso` or `unattended_{newWindowsMachine.fqn}.iso`
(or `unattended_{newMachine.fqn}.iso` / `unattended_{newOsNode.fqn}.iso` on older steps).

See the [Automate Operating System Installation Guide](https://attuneops.io/docs/topics/automated_os_installation.html).
