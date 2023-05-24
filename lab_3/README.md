# Развертывание системы мониторинга ELK Stack

## Цель работы

1.  Освоить базовые подходы централизованного сбора и накопления информации

2.  Освоить современные инструменты развертывания контейнирозованных приложений

3.  Закрепить знания о современных сетевых протоколах прикладного уровня

## Ход выполнения практической работы

### Шаг 1. Развернуть систему мониторинга на базе ElasticSearch

1.  Увеличиваем размер виртуальной памяти системы

![image](https://github.com/Pave1Nesterov/threat_hunting/assets/95019919/0eeb3f40-2fab-4a85-ab2b-f2da16c1c678)

2.  Далее следуем инструкции по ссылке:

https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html

Создаём файл docker-compose.yml, а так же конфигурационные файлы для каждого модуля:

```         
filebeat.yml
packetbeat.yml
```
![image](https://github.com/Pave1Nesterov/threat_hunting/assets/95019919/69181f0d-6bdb-408e-9d61-00938ba20d76)

3.  После формирования файлов с конфигурациями, запускаем образы

![image](https://github.com/Pave1Nesterov/threat_hunting/assets/95019919/b55f84b1-73cc-4abd-ae96-b107f99b45bf)

4.  Переходим на `localhost:5061` и авторизируемся

![image](https://github.com/Pave1Nesterov/threat_hunting/assets/95019919/bd88c051-af51-4582-84f0-f7227ecb570b)

Шаг 2. Работа с ElasticSearch

1.  filebeat

![image](https://github.com/Pave1Nesterov/threat_hunting/assets/95019919/31376a95-bd3f-4487-b826-0fc48a14cb3e)

2.  packetbeat

![image](https://github.com/Pave1Nesterov/threat_hunting/assets/95019919/574f043a-42fd-48ad-8d3a-ef4b3641d5b9)

## Оценка результата

Была развёрнута система ElasticSearch и настроена система сбора трафика и лог-файлов.

## Вывод

В результате работы была освоена система контейнеризации приложений Docker, работа с Docker-compose и освоена система централизованного сбора и накопления информации ElasticSearch.
