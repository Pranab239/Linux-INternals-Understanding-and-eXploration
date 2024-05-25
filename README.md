### README.md

# Linux Kernel Module and IOCTL Projects

## Overview

This project involves the development of various Linux kernel modules and IOCTL drivers to extend kernel functionality and interact with the /proc filesystem.

## Tasks

### Task 1: Kernel Modules
1. **helloworld.ko**: Prints "Hello World" when loaded and "Module Unloaded" when removed.
2. **lkm1.c**: Lists all processes in a running or runnable state.
3. **lkm2.c**: Takes a PID and prints its child processes' PIDs and states.
4. **lkm3.c**: Takes a PID and virtual address, prints the physical address if mapped.
5. **lkm4.c**: For a given PID, prints the size of allocated virtual and physical address spaces.

### Task 2: IOCTL Drivers
1. **ioctl_driver**: Provides physical address for a given virtual address and modifies memory content via IOCTL calls. Includes a user space application to test these functionalities.
2. **Dr. Doom's Task**: IOCTL driver to notify a central station of process exits by changing the parent process to receive a SIGCHLD signal.

### Task 3: procfs Entries
1. **hello_procfs.c**: Creates a /proc entry that displays "Hello World!" when read.
2. **get_pgfaults.c**: Creates a /proc entry to display the total count of page faults since system boot.

## Installation

1. Install necessary packages:
    ```sh
    sudo apt install linux-headers-$(uname -r) build-essential
    ```

2. Follow instructions in each directory's `Makefile` to build and load the kernel modules and IOCTL drivers.

## Directory Structure

```
<rollnumber>_assignment1/
├── 1/
│   ├── lkm1.c
│   ├── lkm2.c
│   ├── lkm3.c
│   ├── lkm4.c
│   ├── Makefile
│   └── Kbuild* (if used)
├── 2_I/
│   ├── spock.sh
│   └── ... (solution specific files/dirs)
├── 2_II/
│   ├── control_station.c
│   ├── soldier.c
│   ├── run_dr_doom.sh
│   ├── Makefile
│   └── ... (solution specific files/dirs)
└── 3/
    ├── hello_procfs.c
    ├── get_pgfaults.c
    ├── Makefile
    └── Kbuild* (if needed)
```

## References

- [Linux Kernel Module Programming Guide](https://sysprog21.github.io/lkmpg/)
- [Bootlin Linux Source Code](https://elixir.bootlin.com/linux/v6.1/source)
- [IOCTL Implementation Resources](https://github.com/pokitoz/ioctl_driver)

For any questions or support, please contact [pranab4752@gmail.com](mailto:pranab4752@gmail.com).
