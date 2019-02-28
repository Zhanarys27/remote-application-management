## remote-control

## remote-control

# Название команды: Lot_of_Dream

# Название проекта: Приложение для управления ПК с помощью смартфона

## Идея проекта: создание программы для управления компьютером с помощью телефона по Bluetooth. Мобильное приложение, которое устанавливается на телефон или планшет, оснащенный Bluetooth адаптером и работающий под управлением операционной системы Android. Для осуществления управления компьютером будет использована технология Bluetooth, позволяет обеспечить обмен информации между различными устройствами. Bluetooth позволяет этим устройствам сообщаться, когда они находятся в радиусе до 10 м друг от друга. В ходе выполнения курсового проекта предполагается реализовать следующий функционал:
1. Использование смартфона для управления аудиоплеером.
2. Использование смартфона в качестве компьютерной мыши. 
3. Использования смартфона для показа презентаций.
В результате чего данную программу можно будет активно использовать в домашних условиях, не находясь при этом непосредственно перед компьютером. Так же при необходимости программа может найти применение и в рабочие моменты. Например, управление презентацией или демонстрацией слайдов.

## Тип проекта: мобильное приложение (Android).

## Технологии: язык С & Java, Android Bluetooth API, Windows socket.

## Доска: https://trello.com/b/wvrVZLZ3/remotecontrol

### Требования к функционалу:
Главное требование заключается в следующем: пользователь устанавливает клиентскую часть приложения на свой телефон, а серверную на ПК. Далее посредством соединения Bluetooth пользователь может контролировать множество процессов на своем ПК. Данное требование и отличает разрабатываемый программный продукт от традиционных клиентских приложений.

### Выбор технологий:
Так как программа состоит из клиентской и серверной части, и каждый из модулей разрабатывается под разные операционные системы, то необходимо было выбрать средства для работы с Bluetooth под обе операционные системы. Важным условием является то, что и клиент, и сервер должны использовать один и тот же протокол. В качестве протокола передачи данных был выбран протокол RFCOMM. Он является одним из самых простых и удобен для реализации соединения по схеме “клиент-сервер”.
Серверная часть программы разрабатывается для операционной системы Windows. Поэтому для работы с Bluetooth был выбран API Windows socket, который использует протокол RFCOMM и позволил настроить сервер на принятие данных от клиента. Сам же клиент разрабатывался под операционную систему Android, так что здесь выбор пал на API Android Bluetooth, который , также как и WinSock, использует протокол RFCOMM и позволяет пользоваться телефоном в качестве клиента для передачи данных серверу.




