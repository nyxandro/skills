<div align="center">

# nyxandro skills

**Скиллы для ИИ-агентов в Claude Code, Codex, OpenCode и Cursor. Любой из них ставится плагином Claude Code из одного каталога.**

[![Validate catalog](https://github.com/nyxandro/skills/actions/workflows/validate.yml/badge.svg)](https://github.com/nyxandro/skills/actions/workflows/validate.yml)
[![License](https://img.shields.io/github/license/nyxandro/skills)](LICENSE)
[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-SKILL.md-6f42c1)](https://agentskills.io/specification)
[![Claude Code marketplace](https://img.shields.io/badge/Claude%20Code-marketplace-d97757)](#установка)

[English](README.md) · **Русский**

</div>

Каталог плагинов Claude Code с моими скиллами. Каждый скилл живёт в своём репозитории, со своими
версиями, выпусками и списком изменений. Этот репозиторий только перечисляет их, чтобы Claude Code
мог поставить любой из одного места. Те же скиллы работают в Codex, OpenCode, Cursor и других
агентах, которые понимают Agent Skills.

## Установка

| Агент | Команда |
|---|---|
| Claude Code 2.1.275 и новее | `/plugin install <скилл> --marketplace nyxandro/skills` |
| Claude Code постарше | `/plugin marketplace add nyxandro/skills`, потом `/plugin install <скилл>@nyxandro` |
| Codex, OpenCode, Cursor и другие | `npx skills add nyxandro/<скилл>-skill` |

Вместо `<скилл>` подставьте имя из таблицы ниже, например
`/plugin install prod-recon --marketplace nyxandro/skills`. Каждый установленный скилл добавляет
своё описание в каждую сессию, поэтому ставьте только те, которыми пользуетесь.

<details>
<summary>Обновления</summary>

<br>

Версии в каталоге не закреплены, поэтому каждый коммит в репозиторий скилла приходит
пользователям плагина как обновление. Выполните в терминале
`claude plugin marketplace update nyxandro`, потом `claude plugin update <скилл>@nyxandro`, или
включите автообновление каталога в `/plugin` → Marketplaces.

</details>

## Скиллы

**Планирование и качество**

| Скилл | Что делает | Версия |
|---|---|---|
| [feature-blueprint](https://github.com/nyxandro/feature-blueprint-skill) | Пишет спецификацию фичи и план реализации до кода, с исследованием за каждым решением и вопросами только о том, что меняет продукт | ![release](https://img.shields.io/github/v/release/nyxandro/feature-blueprint-skill?label=) |
| [property-testing](https://github.com/nyxandro/property-testing-skill) | Тесты на свойства с fast-check и Hypothesis, с честными генераторами и доказательством, что тест умеет падать | ![release](https://img.shields.io/github/v/release/nyxandro/property-testing-skill?label=) |
| [sparring](https://github.com/nyxandro/sparring-skill) | Второе мнение от Claude или Codex о плане, архитектуре или коде, со спором в несколько ходов | ![release](https://img.shields.io/github/v/release/nyxandro/sparring-skill?label=) |
| [skill-picker](https://github.com/nyxandro/skill-picker-skill) | Подбирает, проверяет и ставит скиллы, нужные стеку проекта, и показывает, что покрыто | ![release](https://img.shields.io/github/v/release/nyxandro/skill-picker-skill?label=) |

**Работа с проектом**

| Скилл | Что делает | Версия |
|---|---|---|
| [prod-recon](https://github.com/nyxandro/prod-recon-skill) | Проверка прода или стейджа только на чтение. Находит сервер, читает логи и базу, отчитывается и ничего не чинит | ![release](https://img.shields.io/github/v/release/nyxandro/prod-recon-skill?label=) |
| [issue-register](https://github.com/nyxandro/issue-register-skill) | Держит список открытых проблем в согласии с кодом, в одном файле и только с тем, что осталось | ![release](https://img.shields.io/github/v/release/nyxandro/issue-register-skill?label=) |
| [session-handoff](https://github.com/nyxandro/session-handoff-skill) | Передаёт незаконченную работу в новую сессию одним документом, сверенным с репозиторием | ![release](https://img.shields.io/github/v/release/nyxandro/session-handoff-skill?label=) |
| [goal-rules](https://github.com/nyxandro/goal-rules-skill) | Даёт агенту довести длинную задачу `/goal` до конца без вас, с записанными решениями и стоп-листом | ![release](https://img.shields.io/github/v/release/nyxandro/goal-rules-skill?label=) |
| [owner-decisions](https://github.com/nyxandro/owner-decisions-skill) | Отвечает на вопрос-развилку так, как вы уже отвечали на похожий. Хранит ваши решения по всем проектам в приватной базе и спрашивает только новое | ![release](https://img.shields.io/github/v/release/nyxandro/owner-decisions-skill?label=) |
| [materials-intake](https://github.com/nyxandro/materials-intake-skill) | Принимает входящие материалы проекта. Раскладывает новое в `inbox/`, не пускает секреты в git и ведёт одну опись того, что лежит и что в этом сказано, с решениями, противоречиями и открытыми вопросами | ![release](https://img.shields.io/github/v/release/nyxandro/materials-intake-skill?label=) |

**Предметные**

| Скилл | Что делает | Версия |
|---|---|---|
| [telegram-bot-development](https://github.com/nyxandro/telegram-bot-development-skill) | Telegram-боты и Mini Apps на живом Bot API, со сверкой с документацией и установленной библиотекой перед каждым вызовом | ![release](https://img.shields.io/github/v/release/nyxandro/telegram-bot-development-skill?label=) |
| [t-invest](https://github.com/nyxandro/t-invest-skill) | Доступ к вашему брокерскому счёту Т-Инвестиций. Портфель, доходность, аналитика и сделки по вашей команде | ![release](https://img.shields.io/github/v/release/nyxandro/t-invest-skill?label=) |

В README каждого скилла сказано, что ему нужно и как им пользоваться.

<details>
<summary>Как устроен каталог</summary>

<br>

- В `.claude-plugin/marketplace.json` по одной записи на скилл, каждая ведёт в репозиторий скилла.
  Claude Code читает этот файл, когда вы добавляете каталог.
- На каждый пуш GitHub запускает `claude plugin validate --strict` по каталогу, поэтому сломанная
  запись не может тихо сломать установку у всех.
- Версии, выпуски и списки изменений живут в репозиториях скиллов, а не здесь.

```text
.claude-plugin/marketplace.json   каталог, по одной записи на скилл
.github/workflows/validate.yml    проверка каталога на каждый пуш
README.md, README.ru.md           эта страница на английском и на русском
```

</details>

## Лицензия

[MIT](LICENSE), для файлов этого репозитория. На сами скиллы она не распространяется, смотрите
репозиторий каждого скилла.
