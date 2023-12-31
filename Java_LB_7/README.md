# Звіт

## Опис Електронної Комерції (E-Commerce) Бек-Енд

### Огляд проекту

Цей проект є бек-енд реалізацією базової системи для платформи електронної комерції, зосередженою на керуванні інвентарем, кошиками користувачів та обробці замовлень. Використовуючи Java Collections, система дозволяє додавати користувачів та товари, керувати їх кошиками та створювати та обробляти замовлення.

### Компоненти системи

1. **Товар (Product):**
   - Поля: ідентифікатор, назва, ціна, кількість на складі.
   - Конструктори та методи доступу до полів.
   - Метод `toString` для адекватного відображення інформації про товар.

2. **Користувач (User):**
   - Поля: ідентифікатор, ім'я користувача, кошик (карта товарів та їх кількості).
   - Конструктори, методи доступу та модифікації кошика.

3. **Замовлення (Order):**
   - Поля: ідентифікатор, ідентифікатор користувача, деталі замовлення (карта товарів), загальна ціна.
   - Конструктори, методи доступу, а також метод для обчислення загальної вартості замовлення.

4. **Платформа Електронної Комерції (ECommercePlatform):**
   - Поля: користувачі, товари, замовлення (усі як мапи).
   - Методи для додавання нових користувачів і товарів, створення замовлень, перегляду списків доступних товарів, користувачів, замовлень та оновлення запасів.

5. **Рекомендації для Користувача:**
   - Метод, що пропонує товари користувачам на основі їхнього кошика або історії покупок.

6. **ECommerceDemo:**
   - Використовується для старту платформи, додавання учасників та товарів, імітації взаємодії користувачів із кошиком, а також створення та обробки замовлень.

### Висновки

Цей звіт надає повний огляд проекту Електронної Комерції (E-Commerce) Бек-Енд, включаючи опис компонентів системи, їх функціональність та взаємодію між ними. Проект використовує Java Collections для ефективного управління даними та забезпечення базового функціоналу електронної комерції.