# Smarty-Releases

Публичный репозиторий только для готовых релизов Android-приложения **Smarty**.

Исходный код хранится отдельно в приватном репозитории `navitanton-source/Smarty`.

## Release contents

Каждый пользовательский релиз должен публиковать:

- `Smarty.apk` — подписанный установочный APK;
- `Smarty.apk.sha256` — SHA-256 для проверки целостности;
- тег `v<versionName>`;
- краткие release notes.

Smarty использует latest GitHub Release этого репозитория как канал обновлений. Токены GitHub в APK не встраиваются: репозиторий публичный и доступен для чтения без авторизации.

## Infrastructure separation

This is a public **binary distribution only** repository, not a source-code CI
project. No billing-read personal access token is required or stored here.
When creating a new **source** repository with hybrid GitHub Actions, follow
the private owner's `ci-infrastructure/docs/NEW_PROJECT_ONBOARDING.md`
instead and configure the pre-existing billing-read token only through the
new source repo's Actions Repository secrets. Never place it in public releases.
