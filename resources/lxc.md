---
layout: page
title: LXC
permalink: /resources/lxc/
---

## Notes:

- I use the name c1 in the following commands. Replace c1 with the container you wish to use.
- To view actual stats of a container you can see:

```
/sys/fs/cgroup/memory/lxc/c1
```

*replace memory with a cgroup*

# Installing

- Install from the ubuntu package manager
```
$ sudo apt-get install lxc uidmap cgroup-lite
```

- Check if system is configured properly
```
$ sudo lxc-checkconfig
```

# Commands

- **Create a Container**

```
# lxc-create -n c1 -t ubuntu
```

This creates container c1 from the template ubuntu(replace as you see fit with an available template/usr/share/lxc/templates)

- **Start a Container**

```
# lxc-start -n c1 -d
```

This starts container c1 as a daemon(-d)

- **List Containers**

```
# lxc-ls --fancy
```

- **Access Console**

```
# lxc-console -n c1
```

To exit use ctrl-a q

- **Access Root Filesystem(similar to chroot)**

```
# lxc-attach -n c1
```

- **View All Details of Container**

```
# lxc-info -n c1
```

- **Stop a Container**

```
# lxc-stop -n c1
```

- **Clone a Container**

```
# lxc-clone c1 c2
```

Make sure to stop the machine before cloning

- **Snapshot Container**

```
# lxc-snapshot -n c1
```

- **View Snapshots of a Container**

```
# lxc-snapshot -n c1 -L
```

- **Restore From a Snapshot**

```
# lxc-snapshot -n c1 -r snap2 c2
```

If it is backed by a directory, you have to restore to a new container name

- **Delete Container**

```
# lxc-destroy -n c1
```

