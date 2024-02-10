# Tooling List

[Netflix Linux Performance Analysis](https://netflixtechblog.com/linux-performance-analysis-in-60-000-milliseconds-accc10403c55)

## Standard Linux Performance Tools

- `uptime` - load average
- `dmesg | tail` - kernel messages
- `vmstat 1` - virtual memory statistics
- `mpstat -P ALL 1` - CPU usage
- `pidstat 1` - CPU usage by process
- `iostat -xz 1` - I/O statistics
- `free -m` - memory usage
- `sar -n DEV 1` - network statistics
- `sar -n TCP,ETCP 1` - network statistics
- `top` - process activity
