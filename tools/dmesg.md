# DMESG

Using the `dmesg` command in Linux will display the kernel ring buffer. This can be useful for troubleshooting hardware issues or for viewing system boot messages.

## Examples

### Example 1 - Basic Usage

In the terminal, run the `dmesg` command and observe the output.

Input:

```sh

dmesg

```

Output:

```sh

[    0.000000] Linux version 5.4.0-42-generic (buildd@lcy01-amd64-020) (gcc version 9.3.0 (Ubuntu 9.3.0-10ubuntu2)) #46-Ubuntu SMP Fri Jul 10 00:24:02 UTC 2020 (Ubuntu 5.4.0-42.46-generic 5.4.44)
[    0.000000] Command line: BOOT_IMAGE=/boot/vmlinuz-5.4.0-42-generic root=UUID=3e3b3e3b-3e3b-3e3b-3e3b-3e3b3e3b3e3b ro quiet splash vt.handoff=7
[    0.000000] KERNEL supported cpus:
[    0.000000]   Intel GenuineIntel
[    0.000000]   AMD AuthenticAMD
[    0.000000]   Hygon HygonGenuine
[    0.000000]   Centaur CentaurHauls
[    0.000000]   zhaoxin   Shanghai  
[    0.000000] x86/fpu: x87 FPU will use FXSAVE
[    0.000000] BIOS-provided physical RAM map:
[    0.000000] BIOS-e820: [mem 0x0000000000000000-0x000000000009fbff] usable
[    0.000000] BIOS-e820: [mem 0x000000000009fc00-0x000000000009ffff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000000f0000-0x00000000000fffff] reserved
[    0.000000] BIOS-e820: [mem 0x0000000000100000-0x00000000bffdffff] usable
[    0.000000] BIOS-e820: [mem 0x00000000bffdf000-0x00000000bfffffff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000fc000000-0x

```