# IT Club Irkutsk

Метарепозиторий (репозиторий `itclub-irk/itclub-meta`) с общими материалами и проектами
IT-клуба (Иркутск):

## Состав

Сами проекты — **независимые git-репозитории** и живут в `repos/`
(в корень не включаются, см. `.gitignore`):

| Репозиторий | Что это |
| --- | --- |
| [`itclub-irk.github.io`](https://github.com/itclub-irk/itclub-irk.github.io) | Сайт клуба [itclub-irk.ru](https://itclub-irk.ru) — Hugo (тема PaperMod) |
| [`itclub_chat_bot`](https://github.com/itclub-irk/itclub_chat_bot) | Telegram-чат-бот клуба — Clojure (http-kit, mount, malli) |
| [`community`](https://github.com/itclub-irk/community) | Проект правил сообщества (rules.md) + QR-код |
| [`microfest`](https://github.com/itclub-irk/microfest) | Фестиваль «Полезная микроэлектроника» / конкурс «Микрофест» (rules.md) |

## Работа с проектами

Каждую папку в `repos/` клонируют и коммитят отдельно. Схематично:

```shell
cd repos/<project>
git checkout -b feature/...
# правки, коммиты
git push -u origin <branch>
# PR в основной ветке через GitHub
```

Подробности по сборке и запуску бота — `make dev` / `make build` в `repos/itclub_chat_bot`;
для сайта — `hugo server` в `repos/itclub-irk.github.io`.

## Ссылки

- Сайт: <https://itclub-irk.ru>
- Telegram-чат клуба: QR в `_other/itclub_irkutsk_qr.png`
