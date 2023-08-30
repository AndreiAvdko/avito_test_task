# Тестовое задание на позицию стажера-QA в avito-tech
---
## Задание 1. Где найти файлы для первого задания
1. вариант - По ссылке на [Гугл Документы](https://docs.google.com/spreadsheets/d/1D_ELZoN1oAvxbG0DB3rTlAGNXXftFWyf2SuIbmyOhvk/edit#gid=129372290)
2. вариант - в корне проекта в папке task1 лежит Excel-файл Test-plan.xlsx

## Задание 2. Руководство по запуску автотеста

### Предварительные условия для рабочего пространства:
1. Установлен Git
2. Установлен Gradle (можно проверить командой gradle --version)
3. Установлен JDK (Java Development Kit) (проверить командой java -version)
4. Настройки и скриншоты указаны для среды разработки IntelliJ Idea (возможно вы будете использовать свою среду разработки)

### Клонирование проекта из GitHub
1. В IDEA выбрать ```File -> New -> Project from Version Control...```;
2. В появившемся окне вставить URL репозитория (https://github.com/AndreiAvdko/avito_test_task.git);

![](/images/screen1.png)

3. Выбрать File -> Settings, в настройках Gradle выставить значения как на скриншоте, путь должен соответствовать локальному пути до Gradle;

![](/images/screen2.png)

### Запуск тестов
1. В окне проекта, открыть папку ```avito_test_task\src\test\java\ru.avito\```, двойным кликом открыть класс ```AddAdvertisementInFavourites```;
3. В открывшемся окне ```AddAdvertisementInFavourites.java```, кликнуть на двойную зелёную стрелку;
4. В появившемся модальном окне выбрать пункт ```Run 'AddAdvertisementInFavourites.java'```;

![](/images/screen3.png)

5. В случае успеха, в нижней части окна появится сообщение ```BUILD SUCCESSFUL``` в правой части и зелёные галочки результатов выполнения теста в левой.

### Просмотр Allure-отчёта
1.  В правой части интерфейса IntelliJ Idea нажать на вкладку Gradle
2. Во вкладках найти раздел avito_test_task > verification > allureServe

![](/images/screen4.png)

3. Нажать на него двойным щелчком
4. В браузере откроется Allure-отчёт в котором на вкладке Suites можно ознакомиться с ходом прохождения теста
5. Выберите в списке тест, справа откроется вкладка с шагами прохождения теста в секции Test body
6. Кликая по шагам можно ознакомиться со скриншотами, сделанными на каждом шаге

![](images/screen5.png)

### Post scriptum (Вопрос по прохождению теста)
В рамках выполнения задания попробовал запустить тест с помощью "Github CI". Вот [ссылка на проект](https://github.com/AndreiAvdko/avito_git_ci_test_task/),
где настроено выполнение теста в контейнере Selenoid с помощью Gihub actions (Таб Actions). Однако при выполнении теста столкнулся с проблемой, решение которой пока так и не нашёл - он падает при выполнении, при этом локально всё отрабатывает корректно.
Также периодически тест выполняется нормально, без падений.
Ссылки на Allure-отчеты:
1. [Успешный](https://andreiavdko.github.io/avito_git_ci_test_task/26/#suites/c32586214ad1807100b8da5818070a84/ef64b5407e3cefc8/)
2. [C упавшим тестом](https://andreiavdko.github.io/avito_git_ci_test_task/21/#suites/c32586214ad1807100b8da5818070a84/dfb51c858a4d2754/)

В Allure-отчёте на сделанных скриншотах обнаружил вот это:

![](images/screen7.png)

Если вы знаете в чём может быть проблема и как её исправить, то буду очень благодарен, если вы отправите его по адресу andrei_avdeenko@outlook.com

### Post post scriptum (Обнаруженный дефект)
Во время выполнения тестового задания столкнулся со следующим дефектом ([Ссылка на видео](https://drive.google.com/file/d/1UECd204a7CyQxnAtdcbNeZvjduS9f171/view?usp=sharing))
Шаги для воспроизведения:
1. Открыть любое объявление
2. Нажать <Подписаться на продавца>
3. Закрыть открывшееся окно авторизации
4. Надпись изменится на "Вы подписаны на продавца"
5. При повторном нажатии на кнопку появится предупреждение "По техническим причинам мы не можем подписать вас на продавца"

На [видео](https://drive.google.com/file/d/1UECd204a7CyQxnAtdcbNeZvjduS9f171/view?usp=sharing) всё представлено более наглядно =)