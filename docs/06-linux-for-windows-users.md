# Linux for Windows Users — A Practical Second Environment

Linux is useful even when Windows remains the primary desktop. Run Bash, Python, Git, data validation and scheduled analysis in a separate **learning sandbox** before using authorized remote environments.

## Choose your environment

| Option | Use | Caveat |
|---|---|---|
| Windows Subsystem for Linux (WSL2) | Bash + Linux tools on Windows | Not identical to every Linux server |
| Virtual machine | Full OS, services, process and filesystem practice | Requires disk/RAM |
| Remote Linux over SSH | Learn remote automation | Use only authorized hosts and protected credentials |
| Container | Reproducible application environment | Not a full Linux administration lab |

## Windows → Linux concepts

| Windows habit | Linux command | Why it matters |
|---|---|---|
| Explore files | `pwd`, `ls -lah`, `find` | Confirm location and hidden files |
| Search text | `grep`, `cut`, `sort`, `uniq` | Inspect synthetic data/logs |
| Processes | `ps`, `top`, `pgrep` | Diagnose a job that did not finish |
| Permissions | `ls -l`, `chmod`, `chown` | Least privilege, not `chmod 777` |
| Disk usage | `df -h`, `du -sh` | Detect full volumes |
| Help | `man`, `--help` | Verify command semantics |
| Schedules | `cron`, systemd timer | Plan repeatable tasks with logs |

## Hands-on mini lab

```bash
mkdir -p "$HOME/demo-reporting"/{input,output,logs}
printf 'period,items\nWeek-1,4\nWeek-2,6\n' > "$HOME/demo-reporting/input/demo.csv"
wc -l "$HOME/demo-reporting/input/demo.csv"
grep -n 'Week-2' "$HOME/demo-reporting/input/demo.csv"
python3 --version
```

`>` overwrites files; `>>` appends. Never experiment with `sudo` or destructive cleanup on an unfamiliar system.

## Troubleshooting order

Check host/user → current folder → command availability → permissions → disk → exit status → logs. Fix the actual error before trying elevation. Separate `last attempted run` from `last successful run`.

**RU:** Linux как вторая среда после Windows: WSL, VM, SSH, безопасная работа с файлами, процессами, правами и логами. Все упражнения — в отдельной тестовой среде.

References: [Microsoft WSL](https://learn.microsoft.com/windows/wsl/), [GNU Coreutils](https://www.gnu.org/software/coreutils/manual/), [Linux Journey](https://github.com/labex-labs/linuxjourney).
