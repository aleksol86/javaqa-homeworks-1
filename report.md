# Отчёт о тестировании 
## Краткое описание
18.02.2020 - 18.02.2020 было проведено функциональное тестирование инструкции по установке OpenJDK11, запуску приложения KeyValidator и его работе согласно руководству использования.

На тестирование затрачено: 1 час

В результате тестирования выявлены следующие дефекты:
* [Баг 1 При запуске приложения с валидным ключом 80b427f8-92cd-3aae-ba04-3927fbe17c6 появляется сообщение FAIL](https://github.com/aleksol86/javaqa-homeworks-1/issues/3)
* [Баг 2 При запуске приложения с валидным ключом 387eedc6-12e9-3b32-9881-63b6b5e85317 появляется сообщение FAIL](https://github.com/aleksol86/javaqa-homeworks-1/issues/4)
* [Баг 3 При запуске приложения с невалидным ключом 2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1 появляется сообщение ОК](https://github.com/aleksol86/javaqa-homeworks-1/issues/5)
## Описание процесса тестирования
 В процессе тестирования использовались следующие артефакты:
* Инструкция по установке OpenJDK11
* Руководство использования KeyValidator

В качестве тестовых данных использовались данные
[Инструкция по установке OpenJDK11](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/openjdk11-manual.md#инструкция-по-установке-openjdk11),
[Ключи для проверки приложения KeyValidator](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md#ключи-для-проверки).

* Тестирование инструкции по установке OpenJDK11 и работоспособности в ОС
  * Установить OpenJDK11 по шагам в инструкции 
  * Выполнить команду cmd, нажав Win+R  
  * В командной строке набрать java -version
  * Ожидаемый результат: установка выполнена успешно 

* Тестирование запуска приложения KeyValidator и его совместимости с Java 11:
  * Скачать KeyValidator по ссылке, нажав Download  https://github.com/netology-code/javaqa-homeworks/blob/master/intro/artifacts/KeyValidator.class
  * Переместить в папку javaqa-homeworks 1 
  * Открыть Git Bash и перейти в директорию javaqa-homeworks 1
  * Ввести в строке:
  
    `java KeyValidator 00000000-0000-0000-0000-000000000000 00000000-0000-0000-0000-000000000001`

    где 00000000-0000-0000-0000-000000000000, 00000000-0000-0000-0000-000000000001 - передаваемые для валидации ключи 

  * Нажать Enter
  * Ожидаемый результат: приложение запускается 


Тестирование производилось в следующем окружении:
* Windows 7 SP1 x64
* Java 11
* Git c оболочкой Bash 