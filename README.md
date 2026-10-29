# NSU OS Labs

Solutions to the UNIX system programming course (Operating Systems, Novosibirsk State University, 2025/26).
Plain C on top of POSIX system calls.

| Task | Topic | Key calls |
|---|---|---|
| [1](Task1) | Process attributes and resource limits, command-line options | `getopt`, `getuid`, `getrlimit`, `ulimit`, `putenv` |
| [2](Task2) | Time zones | `time`, `tzset`, `localtime`, `setenv` |
| [3](Task3) | Real vs. effective user ID, file access | `getuid`, `setuid`, `fopen` |
| [4](Task4) | Linked list of input lines | dynamic memory |
| [5](Task5) | Line offset table, random access to a file | `lseek`, `read` |
| [6](Task6) | Same with a read timeout | `sigaction`, `lseek` |
| [7](Task7) | Same with a memory-mapped file | `mmap` |
| [9](Task9) | Creating a child process | `fork`, `waitpid` |
| [10](Task10) | Running a program and reporting its exit status | `fork`, `execvp`, `waitpid` |
| [17](Task17) | Line editor in non-canonical terminal mode | `tcsetattr`, `read`, `write` |
| [18](Task18) | `ls -l`-style file listing | `stat`, `localtime` |
| [21](Task21) | Signal handling | `signal` |
| [25](Task25) | Inter-process communication through a pipe | `pipe`, `fork`, `wait` |
| [30](Task30) | UNIX domain socket client/server | `socket`, `bind`, `listen`, `accept` |
| [31](Task31) | Multi-client server with I/O multiplexing | `poll` |
| [32](Task32) | Multi-client server, non-blocking I/O | `fcntl`, `signal` |

## Build

```sh
cc -Wall -o task TaskN/*.c   # client/server tasks: build client.c and server.c separately
```

Tested on Linux.
