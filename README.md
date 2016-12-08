# deepsleep
deepsleep is a simple script that reduces power consumption of most Linux systems.

# verbs/usage
deepsleep has three options:
`sleep` - puts the system into a state of sleep and exit
`wake` - puts the system into a normal state and exit
`interactive` - put the system into a state of sleep and wait for the user to wake the system; ideal for short naps or testing
`status` - prints the status of the system (exit code also returns the current state: 3 for sleeping, 4 for awake)

# method
`deepsleep` sleeps all cores on the system except for core 0 and stops all hard disks. This allows the system to continue functioning in a sleepy state (i.e. respond to SSH requests). `deepsleep` can also be configured to perform certain commands before sleep and after waking (see functions `beforesleep` and `afterawaken`) such as unmounting filesystems to prevent disk arbitration which could cause drive spin-up.

# to-do
- [ ] comment code for readability
- [ ] add usage message on invalid option
