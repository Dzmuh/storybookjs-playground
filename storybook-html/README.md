# Storybook for HTML

В этом проекте задействуем Storybook для создания пространства для разработки и прототипирования HTML.

## Быстрый старт нового проекта

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

## Настройка Storybook

Storybook позволяет достаточно гибко [настроить](https://storybook.js.org/docs/configurations/options-parameter/) себя под конкретный проект.

## Дополнения

Storybook имеет расширения. Рассмотрим ряд рекомендуемых.

### Docs

Расширение Docs позволяет расширить компоненты Storybook документацией.
Также расширение позволяет создавать и использовать файлы MDX для большего контроля над документацией.

Установка:

```bash
yarn add -D @storybook/addon-docs
```

Расширение имеет зависимости, поэтому выполним ещё:

```bash
yarn add -D react react-is babel-loader
```

Дополним файл `.storybook/main.js`:

```js
module.exports = {
    stories: ['../src/**/*.stories.(js|mdx)'],
    addons: ['@storybook/addon-docs'],
};
```

* [Storybook Docs Addon - Github](https://github.com/storybookjs/storybook/tree/master/addons/docs)

### Links

Создание ссылок между страницами Storybook.

* [Story Links Addon - Github](https://github.com/storybookjs/storybook/tree/master/addons/links)

## Работа с этим проектом

Инициализация проекта:

```bash
yarn install
```

Запускаем!

```bash
yarn storybook
```

## Ссылки

* [Storybook for HTML - Docs](https://storybook.js.org/docs/guides/guide-html/)
* [Exporting Storybook as a Static App - Docs](https://storybook.js.org/docs/basics/exporting-storybook/)
