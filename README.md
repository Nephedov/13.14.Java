# «Наследование и расширяемость систем. Проблемы наследования». «Исключительные ситуации и их обработка. Тестирование исключений».

## Решения
### Задание 1
* <a href="https://github.com/Nephedov/13.14.Java/blob/main/src/main/java/ru/netology/javaqa/Product.java">Product.java</a> - родительский класс описывающий "продукт".
* <a href="https://github.com/Nephedov/13.14.Java/blob/main/src/main/java/ru/netology/javaqa/Book.java">Book.java</a> - дочерний класс расширяющий "продукт" родительского класса.
* <a href="https://github.com/Nephedov/13.14.Java/blob/main/src/main/java/ru/netology/javaqa/Smartphone.java">Smartphone.java</a> - дочерний класс расширяющий "продукт" родительского класса.
* <a href="https://github.com/Nephedov/13.14.Java/blob/main/src/main/java/ru/netology/javaqa/ProductRepository.java">ProductRepository.java</a> - класс-репозиторий.
* <a href="https://github.com/Nephedov/13.14.Java/blob/main/src/main/java/ru/netology/javaqa/ProductManager.java">ProductManager.java</a> - класс-менеджер.
* <a href="https://github.com/Nephedov/13.14.Java/blob/main/src/test/java/ProductRepositoryTest.java">ProductRepositoryTest.java</a> - автотесты.

Ветка <a href="https://github.com/Nephedov/13.14.Java/tree/main">main</a> с проектом.
### Задание 2
* <a href="https://github.com/Nephedov/13.14.Java/blob/rich/src/main/java/ru/netology/javaqa/Product.java">Product.java</a> - с добавленным boolean matcher.
* <a href="https://github.com/Nephedov/13.14.Java/blob/rich/src/main/java/ru/netology/javaqa/Book.java">Book.java</a> - с переопределенным matcher родительского класса.
* <a href="https://github.com/Nephedov/13.14.Java/blob/rich/src/main/java/ru/netology/javaqa/Smartphone.java">Smartphone.java</a> - с переопределенным matcher родительского класса.
* <a href="https://github.com/Nephedov/13.14.Java/blob/rich/src/test/java/ProductRepositoryTest.java">ProductRepositoryTest.java</a> - автотесты.

Ветка <a href="https://github.com/Nephedov/13.14.Java/tree/rich">rich</a> с проектом.

### Задание 3, 4
* <a href="https://github.com/Nephedov/13.14.Java/blob/expection/src/main/java/ru/netology/javaqa/NotFoundException.java">NotFoundException.java</a> - генерирующий исключение при попытке удаления несуществующего "продукта".
* <a href="https://github.com/Nephedov/13.14.Java/blob/expection/src/main/java/ru/netology/javaqa/AlreadyExistsException.java">AlreadyExistsException.java</a> - генерирующий исключение при попытке добавления "продукта" с повторяющимся id.
* <a href="https://github.com/Nephedov/13.14.Java/blob/expection/src/test/java/ProductRepositoryTest.java">ProductRepositoryTest.java</a> - автотесты.

Ветка <a href="https://github.com/Nephedov/13.14.Java/tree/expection">expection</a> с проектом.
## Что было сделано
### Задание 1
* Создан Maven проект и настроен <a href="https://github.com/Nephedov/13.14.Java/blob/main/pom.xml">pom.xml</a> с плагинами и зависимостями:
  * JunitJupier.
  * Surefire.
  * Lombok.
  * Jacoco в режиме генерации отчетов и обрушения сборки по покрытию 100% по бранчам методов.
  * Настроен <a href="https://github.com/Nephedov/13.14.Java/blob/main/.github/workflows/maven.yml">maven.yml</a> для Gitub CI.
* Разрабон базовый класс <a href="https://github.com/Nephedov/13.14.Java/blob/main/src/main/java/ru/netology/javaqa/Product.java">Product.java</a> - описывающий объект "продукт".
* Разработано два унаследованных от <a href="https://github.com/Nephedov/13.14.Java/blob/main/src/main/java/ru/netology/javaqa/Product.java">Product.java</a> класса:
  <a href="https://github.com/Nephedov/13.14.Java/blob/main/src/main/java/ru/netology/javaqa/Book.java">Book.java</a>,
  <a href="https://github.com/Nephedov/13.14.Java/blob/main/src/main/java/ru/netology/javaqa/Smartphone.java">Smartphone.java</a>.
* Реализован класс-репозиторий <a href="https://github.com/Nephedov/13.14.Java/blob/main/src/main/java/ru/netology/javaqa/ProductRepository.java">ProductRepository.java</a> для сохранения, получения сохраненных, удаления экземпляра Product.
* Реализован класс-менеджер <a href="https://github.com/Nephedov/13.14.Java/blob/main/src/main/java/ru/netology/javaqa/ProductManager.java">ProductManager.java</a>,
  для добавления экземпляра Product в репозиторий и осуществления поиска по ним.
* Реализован класс с автотестами <a href="https://github.com/Nephedov/13.14.Java/blob/main/src/test/java/ProductRepositoryTest.java">ProductRepositoryTest.java</a>, проверяющий работу разработанных классов.
### Задание 2
* Создана ветка <a href="https://github.com/Nephedov/13.14.Java/tree/rich">rich</a> от ветки <a href="https://github.com/Nephedov/13.14.Java/tree/main">main</a> в которой:
  * Добавлен boolean matcher в <a href="https://github.com/Nephedov/13.14.Java/blob/rich/src/main/java/ru/netology/javaqa/Product.java">Product.java</a>, переопределяемый в дочерних классах.
  * Добавлены unit тесты в <a href="https://github.com/Nephedov/13.14.Java/blob/rich/src/test/java/ProductRepositoryTest.java">ProductRepositoryTest.java</a>.
### Задание 3, 4
* Создана ветка <a href="https://github.com/Nephedov/13.14.Java/tree/expection">expection</a> от ветки <a href="https://github.com/Nephedov/13.14.Java/tree/main">main</a> в которой:
  * Создан класс исключения <a href="https://github.com/Nephedov/13.14.Java/blob/expection/src/main/java/ru/netology/javaqa/NotFoundException.java">NotFoundException.java</a>,
    отнаследованный от RuntimeException - используемый в методе removeById() класса
    <a href="https://github.com/Nephedov/13.14.Java/blob/expection/src/main/java/ru/netology/javaqa/ProductRepository.java">ProductRepository.java</a>.
  * Создан класс исключения <a href="https://github.com/Nephedov/13.14.Java/blob/expection/src/main/java/ru/netology/javaqa/AlreadyExistsException.java">AlreadyExistsException.java</a>,
    отнаследованный от RuntimeException - используемый в методе saveProduct() класса
    <a href="https://github.com/Nephedov/13.14.Java/blob/expection/src/main/java/ru/netology/javaqa/ProductRepository.java">ProductRepository.java</a>.
  * Реализованы автотесты на проверку работы исключений - <a href="https://github.com/Nephedov/13.14.Java/blob/expection/src/test/java/ProductRepositoryTest.java">ProductRepositoryTest.java</a>.

# Описание Задания 1. Менеджер товаров (обязательное к выполнению)

Вам необходимо реализовать менеджер товаров, который умеет:

* добавлять товары в репозиторий,
* искать товары.

Что нужно сделать:
1. Разработайте базовый класс `Product`, содержащий `ID`, название, стоимость.
1. Разработайте два унаследованных от `Product` класса: `Book` с текстовыми полями «название» и «автор» и `Smartphone` с текстовыми полями «название» и «производитель»; общие поля вынесите в родителя.
1. Разработайте репозиторий, позволяющий сохранять `Product`, получать все сохранённые `Product` и удалять по `ID`. Для этого репозиторий будет хранить у себя поле с типом `Product[]` (массив товаров).
1. Разработайте менеджера, который умеет добавлять `Product` в репозиторий и осуществлять поиск по ним. Для этого вам нужно создать класс, конструктор которого будет принимать параметром репозиторий, а также с методом `publiс void add(Product product)` и методом поиска (см. ниже).

Менеджер при переборе всех продуктов, хранящихся в репозитории, должен для каждого продукта вызывать определённый в классе менеджера же метод `matches`, который проверяет, соответствует ли продукт поисковому запросу.

При проверке на соответствие запросу товара мы проверяем вхождение запроса в текст названия товара.

Напишите тесты на менеджер и репозиторий, добившись 100% покрытия по бранчам методов с логикой.


# Описание Задания 2*. Менеджер товаров: rich model (необязательная задача)

Достаточно часто объекты, моделирующие предметную область, называют моделями. Часто модели делают глупыми, то есть не содержащими никакой логики.

Но есть и другой подход, который позволяет делать умные или богатые модели (rich model), которые могут уже содержать определённую логику.

Что нужно сделать:
1. Создайте в том же, что и первое задание, репозитории новую ветку `rich` на базе ветки первого задания.
1. Реализуйте в классе `Product` метод `public boolean matches(String search)`, который определяет, подходит ли продукт поисковому запросу исходя из названия.
1. Переопределите этот метод в дочерних классах, чтобы они сначала вызывали родительский метод, и только если родительский метод вернул `false`, тогда проводили дополнительные проверки: `Book` — по автору, `Smartphone` — по производителю.
1. Замените в менеджере вызов метода `matches` из класса самого менеджера на вызов метода `matches` у самих продуктов: `if (product.matches(search)) {`.
1. Теперь вам нужны unit-тесты на методы ваших умных моделей, напишите их.
1. Удостоверьтесь, что ранее написанные тесты на менеджера из решения задачи 1 проходят.
1. Добейтесь 100% покрытия по бранчам методов с логикой.

# Описание Задания 3. NotFoundException (обязательное к выполнению)

Вы развиваете приложение с менеджером товаров, который мы рассматривали на лекции, и решили сделать так, чтобы при попытке удаления несуществующего объекта из репозитория генерировалось ваше исключение, а не `ArrayIndexOfBoundsException`.

Обратите внимание: это правильный подход, поскольку таким образом вы сообщаете через генерацию исключения, что это исключение, вписывающееся в вашу логику, а не ошибка программиста.

Что нужно сделать:
1. Возьмите проект с менеджером, репозиторием и товарами, мы его писали в рамках ДЗ про наследование.
1. Создайте класс исключения `NotFoundException`, отнаследовавшись от `RuntimeException`, и реализуйте как минимум конструктор с параметром-сообщением. Он будет просто вызывать суперконструктор предка, см. подсказку.
1. В методе удаления `removeById` сначала проверяйте, есть ли элемент. Для этого прямо из метода `removeById` вызывайте метод `findById`: если результат `null`, тогда выкидывайте исключение `NotFoundException`.
1. Напишите два автотеста на репозиторий: первый должен проверять успешность удаления существующего элемента, второй — генерации `NotFoundException` при попытке удаления несуществующего элемента.

Убедитесь, что ваши автотесты проходят. Напоминаем, что проект должен быть на базе Maven, с подключёнными зависимостями и необходимыми плагинами.

Мы рекомендуем вам указывать в сообщении исключения: при удалении по какому конкретно ID было сгенерировано ваше исключение.
Простейший способ, как это можно сделать: ```"Element with id: " + id + " not found"```.

# Описание Задания 4*. AlreadyExistsException (необязательная задача)

В том же самом проекте и в той же самой ветке добавьте следующую новую функциональность. В методе добавления нового товара в репозиторий должна осуществляться проверка на то, что в нём уже нет товара, у которого бы совпадал `ID` с `ID` добавляемого товара. Если же такой есть, то должно выкидываться ваше исключение — 
`AlreadyExistsException`. 

Напишите два автотеста на репозиторий: первый должен проверять успешность добавления элемента, второй — генерации `AlreadyExistsException` при попытке добавить элемент с повторяющимся `ID`.
