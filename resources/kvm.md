---
layout: page
title: KVM
permalink: /resources/kvm/
---


# Useful Tips

KVM can sometimes be tricky when used on a headless server. To fix it so you can use curses, you need to edit the following things in the vm.

- Modify /etc/default/grub

```
GRUB_CMDLINE_LINUX_DEFAUL="fbcon=map:99 text"

GRUB_TERMINAL=console

```

Run update-grub

- Blacklist vga16fb

```
echo 'install vga16fb /bin/true' >/etc/modprobe.d/graphics-disabled.conf
```

# Troubleshooting

For networking, it is useful to use a tap device. Make sure the /etc/qemu-ifup script has switch set to the bridge device. It normally tries to act smart and guess it based on your ip routes. This unfortunately is not helpful if you want a private network.

# Useful Commands

- **Connect to qemu.**

```
$ virsh connect qemu:///system
```

- **Check VM info.**

```
$ virsh dominfo GUESTNAME
```

- **List VMs.**

```
$ virsh list
```

- **Display VM CPU & Memory Usage.**

```
$ virt-top
```

- **START** \| **STOP** \| **REBOOT** \| **SUSPEND** \| **RESUME VM**.

```
$ virsh START|STOP|REBOOT|SUSPEND|RESUME GUESTNAME
```

- **Connect to VM Console.**

```
$ virsh console GUESTNAME
```

- **Clone a VM.**

```
$ virt-clone --connect=qemu:///system -o SRCGUEST -n NEWHOST -f /path/to/image/newhost.qcow2 
```
