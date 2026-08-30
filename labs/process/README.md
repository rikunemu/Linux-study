# Lab: プロセス管理

```bash
sleep 300 &
job_pid=$!
printf 'PID=%s\n' "$job_pid"
ps -p "$job_pid" -o pid,ppid,stat,ni,cmd
jobs
kill "$job_pid"
wait "$job_pid" 2>/dev/null
```

## 課題

- `$!`には何が入るか
- `ps`のPID、PPID、STAT、NIを説明する
- SIGTERMとSIGKILLの違いを調べる

終了対象のPIDが自分で起動した`sleep`であることを確認してから`kill`します。
