# Storybook for HTML

В этом проекте задействуем Storybook для создания пространства для разработки и прототипирования HTML.

## Быстрый старт

Инициализация проекта в автоматическом режиме:

```bash
npx -p @storybook/cli sb init --type html
```

Запускаем!

```bash
npm run storybook
```

## Экспорт Storybook в статичное приложение

Добавляем или расширяем в `package.json` следующую запись:

```json
{
    "scripts": {
        "build-storybook": "build-storybook -c .storybook -o .out"
    }
}
```

Выполним её:

```bash
npm run build-storybook
```

В результате будем иметь статичный вариант нашей работы.

## Ссылки

* [Storybook for HTML - Docs](https://storybook.js.org/docs/guides/guide-html/)
* [Exporting Storybook as a Static App - Docs](https://storybook.js.org/docs/basics/exporting-storybook/)
