# SSH and Remote Work / SSH и удалённая работа

## English

Verify the host key on first connection through a trusted channel. Prefer modern key-based authentication, protect private keys with appropriate permissions and a passphrase, and use an agent where suitable. Never copy private keys into repositories or chat.

Use `~/.ssh/config` to name hosts and centralize user, hostname, port and identity selection. Keep `StrictHostKeyChecking` enabled; bypassing it trades convenience for exposure to machine-in-the-middle attacks. Limit forwarding and remote privileges to actual need.

## Русский

При первом соединении проверяйте fingerprint хоста через доверенный канал. Предпочитайте современную key-based authentication, защищайте private key правами и passphrase и при необходимости используйте agent. Никогда не копируйте private keys в репозитории или чат.

Используйте `~/.ssh/config` для имён хостов и централизованной настройки user, hostname, port и identity. Не отключайте `StrictHostKeyChecking`: удобство не компенсирует риск MITM.

Source / Источник: [OpenSSH manuals](https://www.openssh.com/manual.html)
