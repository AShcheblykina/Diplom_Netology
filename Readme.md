# Дипломный проект по профессии «Инженер по тестированию»

## Тестирование мобильного приложения «Мобильный хоспис»

[Ссылка на задание](https://github.com/netology-code/qamid-diplom)

# Документация

- [План тестирования](https://github.com/AShcheblykina/Diplom_Netology/blob/main/Plan.md)
- [Чек-лист](https://github.com/AShcheblykina/Diplom_Netology/blob/main/%D0%A1heck%20list.xlsx)
- [Тест-кейсы](https://github.com/AShcheblykina/Diplom_Netology/blob/main/TestCase.xlsx)
- [Отчет о тестировании](https://github.com/AShcheblykina/Diplom_Netology/blob/main/Result.md)

# Запуск приложения и тестов

### 1. Склонировать репозиторий https://github.com/AShcheblykina/Diplom_Netology с помощью команды git clone

### 2. Открытие проекта

Откройте клонированный проект в Android Studio.

### 3. Подготовка устройства для тестирования

- Запустите эмулятор или подключите физическое устройство.
- Установите язык устройства на Русский.
- Убедитесь, что на устройстве установлены следующие данные для входа в приложение:
  - **Логин**: `login2`
  - **Пароль**: `password2`

### 4. Переход в директорию проекта

Перейдите в каталог проекта `fmh_android_15_03_24`

### 5. Запуск тестов

- Запустите тесты с помощью команды в терминале: ./gradlew connectedAndroidTest
- Примечание: если возникает ошибка "zsh: permission denied: ./gradlew" то необходимо предоставить права доступа к файлу, чтобы сделать его исполняемым. В этом случае воспользуйтесь следующей командой в терминале: chmod +x ./gradlew

- Дождитесь выполнения всех тестов.

### 6. Формирование отчёта AllureReport

#### Настройка Allure

Добавьте следующую строку в файл `allure.properties` в ресурсах `androidTest` вашего проекта: allure.results.useTestStorage=true

#### Добавление зависимостей

Добавьте следующую зависимость в файл `build.gradle` вашего приложения: androidTestUtil "androidx.test:orchestrator:1.4.2"

#### Извлечение результатов

Выгрузите каталог результатов тестирования с тестируемого устройства используя `Device File Explorer` в Android Studio: /sdcard/googletest/test_outputfiles/allure-results

#### Генерация отчёта

Переместите скачанные результаты на ваш компьютер и выполните команду в терминале на уровне выше каталога с результатами: allure serve

- Дождитесь генерации отчёта и просмотрите его в автоматически открывшемся окне браузера.
