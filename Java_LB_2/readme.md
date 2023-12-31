Звіт по лабораторній роботі з Java: "Система управління бібліотекою"

Опис програми:
Ця Java-програма реалізує систему управління бібліотекою з використанням класів та інтерфейсів для моделювання різних типів елементів та патронів. Основні компоненти програми включають:

1. Абстрактний клас Елемент
Атрибути:
title (рядок)
uniqueID (рядок, унікальний для кожного елемента)
isBorrowed (логічний, за замовчуванням false)
Методи:
Конструктори, геттери, сетери
abstract void borrowItem(): позначає елемент як запозичений.
abstract void returnItem(): позначає елемент як не запозичений.

2. Клас Book (реалізує Елемент)
Атрибути:
author (рядок)
Методи:
borrowItem(): реалізує абстрактний метод з Елемент.
returnItem(): реалізує абстрактний метод із Елемент.

3. Клас DVD (реалізує Елемент)
Атрибути:
duration (ціле число, хвилини)
Методи:
borrowItem(): реалізує абстрактний метод з Елемент.
returnItem(): реалізує абстрактний метод із Елемент.

4. Клас I'm dog Patron
Атрибути:
name (рядок)
ID (рядок, унікальний для кожного патрона)
borrowedItems (Список<Елемент>)
Методи:
Конструктори, геттери, сетери
borrow(Елемент): додає предмет до списку запозичених патроном.
return(Елемент): видаляє предмет зі списку запозичених патроном.

5. Інтерфейс IManageable
Методи:
add(Елемент): додає елемент.
remove(Елемент): видаляє елемент.
listAvailable(): перераховує всі доступні елементи.
listBorrowed(): перераховує всі запозичені елементи.

6. Клас Бібліотека (реалізує IManageable)
Атрибути:
items (List<Елемент>, для збереження всіх елементів)
patrons (List<Patron>, для зберігання всіх зареєстрованих патронів)
Методи:
registerPatron(Patron): реєструє нового патрона.
lendItem(Patron, Елемент): позичає предмет патрону.
returnItem(Patron, Елемент): повертає позичений предмет.
add(Елемент): додає елемент до бібліотеки.
remove(Елемент): видаляє елемент із бібліотеки.
listAvailable(): перераховує всі доступні елементи в бібліотеці.
listBorrowed(): перераховує всі запозичені елементи з бібліотеки.
Тестові випадки (LibraryTest):
Клас LibraryTest містить низку тестових випадків JUnit для перевірки функціональності системи керування бібліотекою. Кожен тестовий випадок адресує конкретний аспект системи та підтверджує його правильність.

testRegisterPatron(): Тестує реєстрацію нового патрона в бібліотеці та перевіряє його присутність у списку патронів.

testLendItem(): Виконує позичання предмета патрону, перевіряючи, чи змінюється стан бібліотечного елемента та списку запозичених речей патрона.

testReturnItem(): Тестує повернення позиченого предмета, впевнюючись, що елемент вилучається зі списку запозичених речей патрона.

testAddItemToLibrary(): Перевіряє можливість додавання нового елемента до бібліотеки та його наявність у списку елементів бібліотеки.

testRemoveItemFromLibrary(): Тестує видалення елемента з бібліотеки та перевіряє його відсутність у списку елементів бібліотеки.

Ці тести охоплюють різні сценарії використання та забезпечують адекватність роботи різних частин системи управління бібліотекою.

Додаткові нотатки:
Код відповідає принципам об'єктно-орієнтованого програмування, використовуючи інкапсуляцію та абстракцію для створення моделі бібліотеки та її компонентів.
Програма має потенціал для розширення та додавання нових функцій з врахуванням потреб користувачів та можливих вдосконалень.