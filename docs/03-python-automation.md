# Python Automation / Автоматизация на Python

## English

Prefer standard-library abstractions: `pathlib` for paths, `shutil` for high-level file operations, `subprocess.run` for external programs and `logging` for diagnostics. Pass subprocess arguments as a list and avoid `shell=True` unless shell syntax is essential and inputs are fully controlled.

```python
from pathlib import Path
import subprocess

target = Path("workspace")
result = subprocess.run(
    ["git", "status", "--short"],
    cwd=target,
    check=True,
    capture_output=True,
    text=True,
)
print(result.stdout)
```

Design automation for idempotency: a repeated run should converge on the intended state. Add dry-run mode for material changes and log what changed.

## Русский

Используйте стандартные abstractions: `pathlib` для путей, `shutil` для файловых операций, `subprocess.run` для внешних программ и `logging` для диагностики. Передавайте аргументы subprocess списком и избегайте `shell=True`, если shell-синтаксис не обязателен и входы не контролируются полностью.

Проектируйте автоматизацию идемпотентной: повторный запуск должен приводить к тому же целевому состоянию. Для существенных изменений добавляйте dry-run и журнал результата.

Sources / Источники: [`subprocess`](https://docs.python.org/3/library/subprocess.html), [`pathlib`](https://docs.python.org/3/library/pathlib.html)
