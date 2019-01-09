# Экзамен по JavaScript

## Настройка IDE

WebStorm включает в себя всё необходимое для работы.

Для VSCode рекомендуется установить следующие плагины:

- [TSLint](https://marketplace.visualstudio.com/items?itemName=eg2.tslint)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [EditorConfig](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)

## Начало работы

Склонируйте репозиторий и установите зависимости:

```bash
git clone https://github.com/urfu-2018/typescript-task-exam/
cd typescript-task-exam
npm install
```

## Доступные команды

Запускаются так: `npm run <command>`

| Команда  | Действие                        |
| -------- | ------------------------------- |
| start:js | Запуск index.js                 |
| start:ts | Запуск index.ts                 |
| format   | Запуск утилиты форматирования   |
| lint     | Запуск статического анализатора |

## Настройка отладчика

Для настройки отладчика в VSCode создайте файл `.vscode/launch.json` и вставьте следующее содержимое:

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Start index.js",
      "program": "${workspaceFolder}/src/index.js",
      "cwd": "${workspaceRoot}"
    },
    {
      "type": "node",
      "request": "launch",
      "name": "Start index.ts",
      "args": ["${workspaceFolder}/src/index.ts"],
      "runtimeArgs": ["--nolazy", "-r", "ts-node/register"],
      "cwd": "${workspaceRoot}",
      "sourceMaps": true
    }
  ]
}
```

Станут доступны две конфигурации - первая для отладки кода на JS, вторая для TS.

<hr>

Желаем всем успешно сдать!

![Stan Pines](https://raw.githubusercontent.com/evgenymarkov/public-images/master/stan-pines.png)
