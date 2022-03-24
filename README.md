@ СТАРТОВЫЙ ШАБЛОН с использованинм Parcel2

<!-- vim-markdown-toc GFM -->

- [ИСПОЛЬЗОВАНИЕ](#ИСПОЛЬЗОВАНИЕ)
  - [Клонируем репозиторий:](#Клонируем-репозиторий)
  - [Удаляем:](#Удаляем)
  - [Инициализируем:](#Инициализируем)
  - [Устанавливаем:](#Устанавливаем)
  - [Создаем html структуру в файле index.html](#Создаем-html-структуру-в-файле-indexhtml)
  - [Запускаем сборку:](#Запускаем-сборку)
  - [Запускаем проект:](#Запускаем-проект)
- [СТРУКТУРА](#СТРУКТУРА)
  - [Config](#config)
  - [Base](#base)
  - [Objects](#objects)
  - [Globals](#globals)
  - [Components](#components)
  - [Utilities](#utilities)

<!-- vim-markdown-toc -->

# ИСПОЛЬЗОВАНИЕ

## Клонируем репозиторий:

git clone https://github.com/

## Удаляем:

rm -rf .git

## Инициализируем:

git init

npm init -y

## Устанавливаем:

npm install --legacy-peer-deps

## Создаем html структуру в файле index.html

!!! При использовании БЭМ методологии, генерируем файловую структуру БЭМ из html папку src/scss/globals/blocs

npm run bemtree

## Запускаем сборку:

npm start

## Запускаем проект:

npm run build

Вот и все! 🎉

# СТРУКТУРА

Шаблонная структура SCSS основанна на ITCSS:

src/scss:
config
| \_variables.scss
| \_functions.scss
| \_mixins.scss
base
| \_resets.scss
| \_typography.scss
| \_forms.scss
objects
| \_buttons.scss
globals
| \_header.scss
| \_footer.scss
| \_layout.scss
components
utilities

Проект настроен на работу с SCSS, в сучае раоты с CSS или SASS требуется создать соответствующие папки с файлами и подключить их в файле index.html

<head>
	<link rel="stylesheet" href="./css/style.css">
</head>

## Config

Для определения всех переменных Sass, миксинов и функций используемых на протяжении всего проекта. Можно использовать один файл для переменных, брекпоинтов (breakpoints), цветов, интервалов и разбивать файл переменных на несколько файлов только для больших проектов.

## Base

Предполагает написание стилей на самих элементах, а не на классах. Включает в себя любые ресеты (например, \* { box-sizing: border-box; }) и базовые стили для типографии и элементов формы, некоторые из которых впоследствии могут быть переопределены на уровне компонентов.

## Objects

Для любых небольших, многократно используемыех элементов пользовательского интерфейса, которые могут присутствовать в нескольких компонентах. Напимер button.scss, присутствующий практически в каждом проекте есть кнопки!

## Globals

Для глобальных компонентов, которые будут использоваться на каждой странице, такие как header и footer, а так же общих классов лэйаутов - например, используемых во многих местах.

## Components

Для больших фрагментов пользовательского интерфейса, таких как hero секции, карточки, медиа объекты и многое другое.

## Utilities

Для вспомогательных классов, которые могут быть применены к любому элементу. Например, для установки вертикальных отступов на всех элементах, которые относятся к этому классу.

#
