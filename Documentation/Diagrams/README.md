# UML Диаграммы
1. [Диаграмма прецедентов](#1)<br>
1.1 [Актёры](#1.1)<br>
1.2 [Варианты использования](#1.2)<br>
1.2.1 [Регистрация](#1.2.1)<br>
1.2.2 [Вход в систему](#1.2.2)<br>
1.2.3 [Просмотр товаров](#1.2.3)<br>
1.2.4 [Просмотр детальной информации о продукте](#1.2.4)<br>
1.2.5 [Создание заказа](#1.2.5)<br>
2. [Диаграммы активности](#2)<br>
2.1 [Регистрация](#2.1)<br>
2.2 [Вход в систему](#2.2)<br>
2.3 [Просмотр всех товаров](#2.3)<br>
2.4 [Просмотр детальной информации о товаре](#2.4)<br>
2.5 [Добавление товара в корзину](#2.5)<br>
2.6 [Создание заказа](#2.6)<br>
3. [Диаграмма последовательности](#3)<br>
4. [Диаграммы состояний](#4)<br>
4.1 [Регистрация нового пользователя](#4.1)<br>
4.2 [Вход в систему](#4.2)<br>
4.3 [Добавление товара в корзину](#4.3)<br>
4.4 [Просмотр детальной информации о товаре](#4.4)<br>
4.5 [Оформление заказа](#4.5)<br>
5. [Диаграмма классов](#5)<br>
6. [Диаграмма компонентов и развертывания](#6)<br>

### 1. Диаграмма прецедентов<a name="1"></a>
Диаграмма прецедентов представляет собой следующую диаграмму:
![Use Case](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/useCase/useCase.jpg)
#### 1.1 Актёры<a name="1.1"></a>
Актёр | Описание
--- | ---
Покупатель|Человек, использующий приложение для просмотра товаров, оформление заказа невозможно до входа в систему.
Зарегистрированный пользователь|Человек, использующий приложение для покупки определенных товаров.

#### 1.2 Варианты использования<a name="1.2"></a>
Примечание: при указании повторения дествия, происходит повторение действия варианта использования, в котором оно возникло.
##### 1.2.1 Регистрация<a name="1.2.1"></a>
**Описание.** Вариант использования "Регистрация" позволяет новому пользователю создать свою учетную запись в системе.
Поток событий:
1. Пользователь нажимает клавишу "Регистрация" на панели инструментов.
2. Приложение переходит на страницу регистрации.
3. Пользователь вводит "Email", "Пароль".
4. Пользователь подтвержает пароль. Если пароли не совпадают, происходит уведомление пользователя об этом и повторение действия 4.
5. Приложение проверяет валидность и уникальность данных. При неверных данных приложение показывает сообщение об ошибке, далее пользователь повторяет дейстия 3, 4.
6. Пользователь нажимает клавишу "Создать мою учетную запись".
7. Приложение добавляет нового пользователя в систему.
8. Конец.
##### 1.2.2 Вход в систему<a name="1.2.2"></a>
**Описание.** Вариант использования "Вход в систему" позволяет пользователю авторизироваться в приложении.
Поток событий:
1. Пользователь нажимает клавишу "Войти" на панели инструментов.
2. Приложение переходит на страницу входа в систему.
3. Пользователь вводит "Email", "Пароль".
4. Приложение проверяет соответствие введенных данных с базой данных. При неверных данных приложение выводит сообщение об ошибке, пользователь повторяет действие 3. 
5. Пользователь нажимает клавишу "Войти".
6. Приложение авторизирует пользователя, при этом заменяя клавишу "Войти" на "Выйти".
7. Конец.
##### 1.2.3 Просмотр товаров<a name="1.2.3"></a>
**Описание.** Вариант использования "Просмотр товаров" позволяет пользователю просматривать все товары, а также выполнять поиск и сортировку с данными товарами.
Поток событий:
1. Пользователь нажимает клавишу "Товары" на панели инструментов.
2. Приложение переходит на станицу просмотра всех товаров.
3. Пользователь вводит данные в поле "поиск". При данном действии выполняется альтернативный поток А1.
4. Пользователь нажимает клавишу со значком сортировки. При данном дейтвии выполняется альтернативный поток А2.
5. Конец.

Альтернативный поток А1:
1. Пользователь вводит данные в поле "поиск".
2. Приложение выполняет поиск по совпадениям введных данных со списком товаров.
3. Приложение отображает результаты поиска на экране.
4. Конец.

Альтенативный поток А2:
1. Пользователь нажимает клавшишу со значком сортировки.
2. Приложение выполняет сортировку товаров в соответствии с выбраными порядком.
3. Приложение отображает результаты сортировки на экране.
4. Конец.
##### 1.2.4 Просмотр детальной информации о товаре<a name="1.2.4"></a>
**Описание.** Вариант использования "Просмотр детальной информации о товаре" позволяет пользователю просматривать подробную информация о товаре, а также добавлять его в корзину.
Поток событий:
1. Пользователь нажимает на определенный товар.
2. Приложение переходит на страницу просмотра детальной информации выбранного товара.
3. Пользователь просматривает информацию.
4. Пользователь нажимает клавишу "Добавить в корзину". При данном действии выполняется альтернативный поток B1.
5. Конец.
Альтернативный поток В1:
1. Пользователь нажимает клавишу "Добавить в корзину".
2. Пользователь выбирает количество товара.
3. Приложение добавляет текущий товар с выбранным количеством в корзину.
4. Конец.
##### 1.2.5 Создание заказа<a name="1.2.5"></a> 
**Описание.** Вариант использования "Создание заказа" позволяет пользователю оформить заказ по выбранному товару в корзине.
Поток событий:
1. Пользователь нажимает клавишу со значком корзины на панели инструментов.
2. Приложение переходит в корзину.
3. Пользователь выбирает нужный ему товар из корзины, изменяет количество, если необходимо.
4. Пользователь заполняет формы "Личные данные","Адрес доставки" и "Способ оплаты".
5. Приложение проверяет валидность данных. При неверных данных происходит повторение действия 4. 
6. Пользователь нажимает клавишу "Оформить заказ у этого продавца".
7. Приложение создает заказ с выбранными продуктами и введенными данными.
8. Конец.
### 2. Диаграммы активности<a name="2"></a>
##### 2.1 Регистрация<a name="2.1"></a> 
При заполнении форм данных происходит их валидация. При неверных данных выводится сообщение об ошибке с требованием повторить действие, иначе происходит регистрация нового пользователя и переход на главную страницу.

![Registration activity](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/Activity/SignUp.jpg)
##### 2.2 Вход в систему<a name="2.2"></a> 
При заполнении форм данных происходит их валидация. При неверных данных выводится сообщение об ошибке с требованием повторить действие, иначе происходит авторизация и переход на главную страницу.

![Login activity](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/Activity/LogIn.jpg)
##### 2.3 Просмотр всех товаров<a name="2.3"></a> 
Пользователь просматривает товары. Пользователь имеет возможность использовать поиск и сортировку при нажатии соответствующих клавиш и ввода данных для поиска. При нажатии на товар происходит переход на страницу его детальной информации.

![Product List activity](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/Activity/ProductList.jpg)
##### 2.4 Просмотр детальной информации о товаре<a name="2.4"></a>
При нажатии на необходимый товар происходит переход на страницу с детальной информацией о нем.

![Product List activity](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/Activity/DetailedInfo.jpg)
##### 2.5 Добавление товара в корзину<a name="2.5"></a>
При нажатии на кнопку "Добавить в корзину" происходит добавление товара с выбранным количеством в корзину. Пользователь имеет возможность редактировать количество.

![Detailed Product Info](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/Activity/AddingToCart.jpg)
##### 2.6 Создание заказа<a name="2.6"></a>
При нажатии на значок корзины на панели инструментов происходит переход в корзину. Пользователь выбирает нужный товар и нажимает оформить заказ. Пользователь заполняет все необходимые для заказа данные. Если данные не проходят валидацию, выводится сообщание об ошибке, иначе при нажатии "Оформить заказ у этого продавца" создается заказ.

![Place Order activity](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/Activity/Ordering.jpg)

### 3. Диаграмма последовательности<a name="3"></a>
Диаграмма последовательности основных вариантов использования представлена ниже:

![Sequence Diagram](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/Sequence/Sequence.jpg)

### 4. Диаграммы состояний<a name="4"></a>
##### 4.1 Регистрация нового пользователя<a name="4.1"></a> 

![Registration Diagram](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/State/Registration.jpg)
##### 4.2 Вход в систему<a name="4.2"></a> 

![LogIn Diagram](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/State/LogIn.jpg)
##### 4.3 Добавление товара в корзину<a name="4.3"></a> 

![AddingToCart Diagram](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/State/AddingT%D0%9ECart.jpg)
##### 4.4 Просмотр детальной информации о товаре<a name="4.4"></a> 

![DetailedInfo Diagram](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/State/DetailedInfo.jpg)
##### 4.5 Оформление заказа<a name="4.5"></a> 

![Ordering Diagram](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/State/Ordering.jpg)

### 5. Диаграмма классов<a name="5"></a>
На этой диаграмме представлены основные классы, которые будут реализованы в системе, а также отношения между ними.

![Class Diagram](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/Class/Class.jpg)

### 6. Диаграмма компонентов и развертывания<a name="6"></a>
Диаграмма компонентов совмещена с диаграммой развертывания и представлена ниже.

![Deployment Diagram](https://github.com/Beavis-Borow/TheBlackT/blob/master/Documentation/Diagrams/Deployment/Deployment.jpg)