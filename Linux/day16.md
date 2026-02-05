# Managing Processes and Optimizing Performance

## Understanding Process Priority and Nice Values
Process priority determines the importance of a process relative to others in the system. In Linux, the `nice` value is used to influence process scheduling by assigning a priority level.

### Key Points:
- **Nice Values**:
  - Range: `-20` (highest priority) to `19` (lowest priority).
  - Default value: `0`.
  - Negative nice values require root privileges.
- **Command to Check Priority**:
  - Use `top` or `htop` to view running processes and their priorities.
- **Changing Nice Values**:
  - Use `nice` to start a process with a specific nice value.
  - Use `renice` to change the nice value of an existing process.

---

## Finding Process IDs
Each running process in Linux is assigned a unique Process ID (PID).

### Commands:
- **List all processes**: `ps -e`
- **Find specific process**: `pgrep <process_name>`
- **Detailed information**: `ps -aux | grep <process_name>`

---

## Sending Signals to Processes
Linux allows sending signals to control or terminate processes.

### Common Signals:
- `SIGTERM` (15): Graceful termination.
- `SIGKILL` (9): Forceful termination.
- `SIGHUP` (1): Reload configuration.

### Commands:
- Send signal: `kill -<signal_number> <PID>`
- Example: `kill -9 1234` (forcefully terminates process with PID 1234).

---

## Practical Example: Adjusting Priority of Long-Running Processes
1. **Start a Process with Nice Value**:
   ```bash
   nice -n 10 sleep 1000
   ```
   - This starts a `sleep` process with a nice value of `10`.

2. **Change Priority of Existing Process**:
   ```bash
   renice -5 -p <PID>
   ```
   - Adjusts the nice value of the process with the given PID to `-5`.

3. **Monitor Changes**:
   ```bash
   top
   ```
   - Observe the updated priority in the `PR` and `NI` columns.

---

## Overview of Process States
Processes in Linux can exist in different states.

### Common States:
- **R**: Running or runnable.
- **S**: Sleeping (waiting for an event).
- **D**: Uninterruptible sleep (waiting for I/O).
- **Z**: Zombie (terminated but not cleaned up).
- **T**: Stopped or traced.

### View Process States:
- Use `ps -e -o pid,stat,cmd` to see process states and commands.

---

## Different Job Types and States
Jobs represent processes managed by the shell.

### Commands:
- **List jobs**: `jobs`
- **Foreground job**: `fg <job_id>`
- **Background job**: `bg <job_id>`
- **Stop job**: `kill -TSTP <PID>`

---

## Visualizing the Process Tree
Understanding parent-child relationships among processes helps analyze system behavior.

### Command:
- `pstree`
  - Displays processes in a tree structure.
- Example:
  ```bash
  pstree -p
  ```
  - Shows processes along with their PIDs.

---
