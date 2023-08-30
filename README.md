# Тестовое задание на позицию стажера-QA в avito-tech
---
## Задание 1. Где найти файлы для первого задания
1 вариант - По ссылке на [Гугл Документы](https://docs.google.com/spreadsheets/d/1D_ELZoN1oAvxbG0DB3rTlAGNXXftFWyf2SuIbmyOhvk/edit#gid=129372290)
2 вариант - в корне проекта в папке task1 лежит Excel-файл Test-plan.xlsx

## Задание 2. Руководство по запуску автотеста

### Предварительные условия для рабочего пространства:
1. Установлен Git
2. Установлен Gradle (можно проверить командой gradle --version)
3 Установлен JDK (Java Development Kit) (проверить командой java -version)
3. Настройки и скриншоты указаны для среды разработки IntelliJ Idea (возможно вы будете использовать свою среду разработки)

### Клонирование проекта из GitHub
1. В IDEA выбрать ```File -> New -> Project from Version Control...```;
2. В появившемся окне вставить URL репозитория;

![](https://raw.githubusercontent.com/AndreiAvdko/avito_test_task/main/images/screen1.png)

3. Выбрать File -> Settings, в окне поиска ввести gradle, в открывшемся пункте настроек выставить значения как на скриншоте;
![](/images/screen2.png)
### Запуск тестов
1. В окне проекта, открыть папку ```avito_test_task\src\test\java\ru.avito\```, двойным кликом открыть класс ```AddAdvertisementInFavourites```;
3. В открывшемся окне ```AddAdvertisementInFavourites.java```, кликнуть на двойную зелёную стрелку;
4. В появившемся модальном окне выбрать пункт ```Run 'AddAdvertisementInFavourites.java'```;

![](https://raw.githubusercontent.com/AndreiAvdko/avito_test_task/main/images/screen2.png)

5. В случае успеха, в нижней части окна появится сообщение ```BUILD SUCCESSFUL``` в правой части и зелёные галочки результатов выполнения теста в левой.
### Просмотр Allure-отчёта
1.  В правой части интерфейса IntelliJ Idea нажать на вкладку Gradle
2. Во вкладках найти раздел avito_test_task > verification > allureServe

![](https://raw.githubusercontent.com/AndreiAvdko/avito_test_task/main/images/screen3.png)

3. Нажать на него двойным щелчком
4. В браузере откроется Allure-отчёт в котором на вкладке Suites можно ознакомиться с ходом прохождения теста
5. Выберите в списке тест, справа откроется вкладка с шагами прохождения теста в секции Test body
6. Кликая по шагам можно ознакомиться со скриншотами, сделанными на каждом шаге

![](https://raw.githubusercontent.com/AndreiAvdko/avito_test_task/main/images/screen4.png)