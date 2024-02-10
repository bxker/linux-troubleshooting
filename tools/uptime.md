# Uptime

Using the `uptime` command in Linux will show you the current time, how long the system has been running, how many users are currently logged on, and the system load averages for the past 1, 5, and 15 minutes.

## Examples

### Example 1 - Basic Usage

In the terminal, run the `uptime` command and observe the output.

Input:

```sh

uptime

```

Output:

```sh

 14:06:30 up 4 min,  0 users,  load average: 0.06, 0.11, 0.04
 # current time
    # up or down
      # time since last boot
        # number of users logged in
            # system load averages for the past 1, 5, and 15 minutes

```

### Example 2 - Uptime redirectors

In the terminal, run the `uptime` command and redirect the output to a file.

Input:

```sh

uptime > uptime.txt

# Optionally append the output to a file
# uptime >> uptime.txt

```

File saved to the current directory with the output of the `uptime` command.

View the files contents:

```sh

cat uptime.txt

```

Output:

```sh

 14:06:30 up 4 min,  0 users,  load average: 0.06, 0.11, 0.04

```

### Example 3 - Combine with date, hostname, whoami, and ip a

In the terminal, run the `uptime` command and combine it with other commands to display the current date, hostname, logged in user, and network information.

Input:

```sh

echo "Current date and time: $(date)" && echo "Hostname: $(hostname)" && echo "Logged in user: $(whoami)" && echo "Network information: $(ip a)" && echo "System uptime: $(uptime)"

# Optionally redirect the output to a file
# echo "Current date and time: $(date)" && echo "Hostname: $(hostname)" && echo "Logged in user: $(whoami)" && echo "Network information: $(ip a)" && echo "System uptime: $(uptime)" > system_info.txt

```

Output:

```sh

Current date and time: Fri 26 Mar 2021 02:06:30 PM UTC
Hostname: ubuntu
Logged in user: user
Network information: 1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
inet

...

valid_lft forever preferred_lft forever
System uptime:  14:06:30 up 4 min,  0 users,  load average: 0.06, 0.11, 0.04
    
```

### Example 4 - Uptime with options (-p, --pretty | -V, --version | -s, --since)

In the terminal, run the `uptime` command with the `-p` option to display the uptime in a more human-readable format.

Input:

```sh

uptime -p
uptime -V
uptime -s

```

Output:

```sh

up 4 minutes
uptime from procps-ng 3.3.12
2021-03-26 14:06:30

```

### Example 5 - Uptime combine with `watch`

In the terminal, run the `uptime` command with the `watch` command to update the output every 2 seconds.

Input:

```sh

watch -n 2 uptime

```

Output:

```sh

Every 2.0s: uptime

 14:06:30 up 4 min,  0 users,  load average: 0.06, 0.11, 0.04

```

### Example 6 - Uptime with `awk`

In the terminal, run the `uptime` command and use `awk` to print the system load averages for the past 1, 5, and 15 minutes.

Input:

```sh

uptime | awk -F'load average: ' '{print $2}'

```

Output:

```sh

0.06, 0.11, 0.04

```

### Example 7 - Uptime with `grep`

In the terminal, run the `uptime` command and use `grep` to filter the output for the system load averages for the past 1, 5, and 15 minutes.

Input:

```sh

uptime | grep -o 'load average.*'

```

Output:

```sh

load average: 0.06, 0.11, 0.04

```
