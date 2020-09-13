[![Build Status](https://travis-ci.com/TinkoffCreditSystems/jira-helper.svg?branch=master)](https://travis-ci.com/TinkoffCreditSystems/jira-helper)

## “jira-helper” features

_version 2.6.0_

- [Chart Bar - showed count issues in columns for every swimlane on a board](./src/README.md#swimline-chart-bar)
- [showed a red-flag on the issue panel](./src/README.md#flag-on-issue-panel)
- [Tetris-planning for the Scrum backlog](./src/README.md#tetris-planning-for-scrum)
- [Printing stickers 76x76мм on a usual laser printer by the set many issues of JIRA](./src/README.md#printing-many-stickers)
- [WIP-limit for several columns](./src/README.md#wip-limits-for-several-columns)
- [WIP-limit for Swimlane](./src/README.md#wip-limits-for-swimlanes)
- [Personal WIP-limit](./src/README.md#wip-limit-for-person)
- [SLA-line for Control Chart with percentile](./src/README.md#sla-line-for-control-chart)
- [Overlay Measurement Ruler on the Control Chart](./src/README.md#control-chart-ruler)
- [The blurring of secret data](./src/README.md#the-blurring-of-secret-data)

## Ведение задач проекта

Все задачи заводятся на [github issues](https://github.com/TinkoffCreditSystems/jira-helper/issues)

Перед добавлением задачи убедитесь, что подобной задачи еще не добавляли.
Обязательно проверьте закрытые задачи, возможно к готовящейся версии такая задача уже добавлена.


### Для добавления нового функционала

[Создайте новую задачу](https://github.com/TinkoffCreditSystems/jira-helper/issues/new)

После описание задачи, добавьте только такие атрибуты:

- Labels: `feature`
- Project: `jira-helper`


### Если необходимо добавить исправление

_Когда функционал работает не так, как ожидаете._

[Создайте новую задачу](https://github.com/TinkoffCreditSystems/jira-helper/issues/new)

После описание задачи, добавьте только такие атрибуты:

- Labels: `invalid`, [`cloud jira`, `jira 7`, `jira 8`] – укажите в каких версиях JIRA воспроизводится проблема.
- Project: `jira-helper`


### Добавить описание проблемы (бага)

[Создайте новую задачу](https://github.com/TinkoffCreditSystems/jira-helper/issues/new)

После описание задачи, добавьте только такие аттрибуты:

- Labels: `bug`, [`cloud jira`, `jira 7`, `jira 8`] – укажите в каких версиях JIRA воспроизводится проблема.
- Project: `jira-helper`


### Labels общий список используемых labels

|   labels     |    Значение                                                               |
|--------------|:--------------------------------------------------------------------------|
| `feature`    | новый функционал                                                          |
| `invalid`    | функционал работает не так как ожидается                                  |
| `bug`        | проблема, ошибка - обязательно указывать label версии где воспроивзодится |
| `jira 7`     | воспроизводится в версии JIRA 7.x.x                                       |
| `jira 8`     | воспроизводится в версии JIRA 8.x.x                                       |
| `cliud jira` | воспроизводится в версии Cloud JIRA                                       |


## Установка расширения для разработки

Выполнить:

```
npm run bootstrap
npm run dev
```

В Chrome:

Открыть меню, выбрать "Дополнительные инструменты",
и в подменю выбрать ["Расширения"](chrome://extensions/)

На панели ["Расширения"](chrome://extensions/) включить "Режим разработчика"

После появления дополнительного меню, выбрать в нём
"Загрузить распакованное расширение"

Выбрать папку куда была произведена сборка `~/jira-helper/dist`.

После этого добавиться плагин в Chrome.


### Во время разработки

После изменения кода, webpack автоматически производит замену кода в папке `dist`.

Поэтому на панели ["Расширения"](chrome://extensions/) нужно нажать
на кнопку "Обновление" (в виде круглой стрелки).

И перезагрузить web-страницу, на которой идет проверка, нажав `F5`.

### Ведение ветки и commit-ов

Название ветки должно начинаться с номера задачи с которой она связана

Пример: `2-title-issue`, где префикс `2` – это номер задачи, обязателен.

В каждом `commit` обязательно добавляйте номер задачи с которым он связан

Пример: `[#15] rename *.feature to *.ru.feaute`

Названия веток и commit-ы пишем на `english` языке.

## Публикация расширения

Официальное расширение публикуется в ["Chrome WebStore"](https://chrome.google.com/webstore/detail/jira-helper/egmbomekcmpieccamghfgjgnlllgbgdl)

Публикация происходит после [сборки релиза на github](https://github.com/TinkoffCreditSystems/jira-helper/releases)

Версия релиза совпадает с версией приложения в [package.json](./package.json)

Этот же номер версии будет соответсвовать номеру пубикуемого в ["Chrome WebStore"](https://chrome.google.com/webstore/detail/jira-helper/egmbomekcmpieccamghfgjgnlllgbgdl)

_Может использоватся в Chrome [version >= 55](./src/manifest.json)_
