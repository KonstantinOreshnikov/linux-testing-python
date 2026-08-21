# Containers and CI / Контейнеры и CI

## English

Build from trusted, minimal base images; exclude irrelevant files with `.dockerignore`; install only required packages; run as a non-root user when possible; rebuild regularly and test images in CI. Multi-stage builds separate build tools from the runtime image.

CI should reproduce local checks from a clean environment. Grant workflow tokens the minimum permissions, pin third-party actions to reviewed versions or commit SHAs, do not print secrets and prefer short-lived OIDC credentials for cloud deployments where supported.

## Русский

Используйте доверенные минимальные base images, исключайте лишнее через `.dockerignore`, устанавливайте только необходимые пакеты, по возможности запускайте процесс не от root, регулярно пересобирайте и проверяйте images в CI. Multi-stage build отделяет инструменты сборки от runtime image.

CI должен воспроизводить локальные проверки в чистом окружении. Выдавайте workflow token минимальные permissions, закрепляйте сторонние actions на проверенной версии или commit SHA, не печатайте secrets и при поддержке используйте короткоживущую OIDC-аутентификацию.

Sources / Источники: [Docker build best practices](https://docs.docker.com/build/building/best-practices/), [GitHub Actions secure use](https://docs.github.com/en/actions/reference/security/secure-use)
