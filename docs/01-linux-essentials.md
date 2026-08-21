# Linux Essentials / Основы Linux

## English

Understand where you are before changing anything: `pwd`, `ls -la`, `find` and `stat` establish context. Linux permissions combine owner, group and other with read, write and execute bits. Change permissions to the minimum required; `chmod 777` is not troubleshooting.

Processes have identifiers, environment and exit status. Inspect with `ps`, `pgrep` and system-specific service tools. Logs are evidence: filter them without overwriting the original. A pipeline connects standard output to standard input; each stage should be understandable and independently testable.

## Русский

Перед изменениями определите контекст: `pwd`, `ls -la`, `find` и `stat`. Права Linux объединяют owner, group и other с битами read, write и execute. Выдавайте минимально необходимые права; `chmod 777` — не диагностика.

Процесс имеет PID, окружение и exit status. Проверяйте процессы через `ps`, `pgrep` и сервисные инструменты системы. Логи — evidence: фильтруйте их без перезаписи оригинала. Pipeline соединяет stdout одной команды со stdin другой.

Source / Источник: [GNU Coreutils manual](https://www.gnu.org/software/coreutils/manual/)
