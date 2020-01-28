# План тестирования
---

# Содержание
1 [Введение](#introduction)  
2 [Объект тестирования](#items)  
3 [Атрибуты качества](#quality)  
4 [Риски](#risk)  
5 [Аспекты тестирования](#features)  
6 [Подходы к тестированию](#approach)  
7 [Представление результатов](#pass)  
8 [Выводы](#conclusion)

<a name="introduction"/>

## Введение

Данный документ описывает план тестирования приложения ["Puzzle-of-Math"](https://github.com/IlyaKolbasov/Puzzle-of-Math). Документ предназначен для людей, выполняющих тестирование данного проекта (тестировщиков). Цель тестирования - проверка соответствия реального поведения программы проекта и ее ожидаемого поведения. Ожидаемые результаты формируются на основе [требований](https://github.com/IlyaKolbasov/Puzzle-of-Math/blob/master/Docs/Requirements.md).

<a name="items"/>

## Объект тестирования

В качестве объектов тестирования можно выделить программные модули, отвечающие за выполнение функциональных требований, а также отображения основных частей интерфейса пользователя:

* Главное меню;
* Выбор уровня;
* Игровое окно;
* Настройки;

<a name="quality"/>

## Атрибуты качества

1. Функциональность:
    - функциональная полнота: приложение должно выполнять все заявленные функции;
    - функциональная корректность: приложение должно выполнять все заявленные функции корректно;
    - функциональная целесообразность: отсутствуют не заявленные функции, которые бы мешали приложению выполнять первоначально поставленные задачи
2. Удобство использования:
    - эстетика пользовательского интерфейса: понятный и плавный интерфейс;
    - актуальность: обновление данных, например, добавление новых уровней;

<a name="risk"/>

## Риски

В данном случае к рискам можно отнести:
* некорректное отображение уровней;
* при запуске приложения в среде версии меньше указанной в требованиях приложение может работать некорректно.

<a name="features"/>

## Аспекты тестирования

В ходе тестирования планируется проверить реализацию основных функций приложения. Аспекты, подвергаемые тестированию: 
* выбор уровня;
* выполнение игрового задания;
* получение подсказки;
* изменение светлой/темной темы;
* отключение фоновой музыки;


### Выбор уровня
Этот вариант использования необходимо протестировать на:
* правильный выбор уровня.

### Выполнение игрового задания
Этот вариант использования необходимо протестировать на:
* правильное выполнение игрового задания.

### Получение подсказки
Этот вариант использования необходимо протестировать на:
* корректное получение подсказки.

### Изменение светлой/темной темы
Этот вариант использования необходимо протестировать на:
* корректное изменение темы на светлую;
* корректное изменение темы на темную.

### Отключение фоновой музыки
Этот вариант использования необходимо протестировать на:
* корректное отключение фоновой музыки.


## Нефункциональные требования:
* Useability интерфейс;
* Все функциональные элементы пользовательского интерфейса имеют названия, описывающие действие, которое произойдет при выборе элемента.

<a name="approach"/>

## Подходы к тестированию

При тестировании будет использован ручной подход.

<a name="pass"/>

## Представление результатов

Результаты представлены  в документе ["Результаты тестирования"](https://github.com/Beavis-Borow/TheBlackT/tree/master/Testing/TestsResults.md).

<a name="conclusion"/>

## Выводы

Данный тестовый план позволяет протестировать основной функционал приложения. Успешное прохождение всех тестов не гарантирует полной работоспособности на всех версиях платформ и архитектурах, однако позволяет полагать, что данное программное обеспечение работает корректно.