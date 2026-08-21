# Shell Safety / Безопасный shell

## English

Use `set -euo pipefail` deliberately in Bash scripts, while understanding its edge cases. Quote expansions (`"$path"`), validate required variables and use `--` before untrusted positional paths when supported. Preview targets before deletion and avoid broad globs.

```bash
#!/usr/bin/env bash
set -euo pipefail

input=${1:?usage: script INPUT}
[[ -f "$input" ]] || { printf 'not a file: %s\n' "$input" >&2; exit 2; }
wc -l -- "$input"
```

Use functions, `readonly`, meaningful exit codes and `trap` for cleanup. Run ShellCheck in development. Never put credentials directly in scripts or command history.

## Русский

Используйте `set -euo pipefail` осознанно, учитывая его особенности. Заключайте expansions в кавычки (`"$path"`), проверяйте обязательные переменные и применяйте `--` перед внешними путями, если команда это поддерживает. Перед удалением выводите точный список целей и избегайте широких glob.

Используйте функции, `readonly`, понятные exit codes и `trap` для cleanup. Не помещайте credentials в скрипты и историю команд.

Source / Источник: [GNU Bash — Shell Scripts](https://www.gnu.org/software/bash/manual/html_node/Shell-Scripts.html)
