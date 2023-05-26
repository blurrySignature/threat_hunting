# Развертывание Threat intelligence Platform OpenCTI

## Цель работы

1.  Освоить базовые подходы процессов Threat Intelligence

2.  Освоить современные инструменты развертывания контейнеризованных
    приложений

3.  Получить навыки поиска информации об угрозах ИБ

## Исходные данные

1.  ОС Kali Linux
2.  RStudio Desktop
3.  Docker
4.  ElasticSearch

## Ход выполнения практической работы

Для разворачивания системы threat intelligence OpenCTI была использована
система контейнеризации приложений Docker.

### Шаг 1 - Предварительная конфигурация

### 1. Для работы ElasticSearch требуется увеличить размер виртуальной памяти системы:

``` bash
    sudo sysctl -w vm.max_map_count=1048575
```

### 2. Создание файла конфигурации

Был создан файл окружения .env со следующими параметрами:

```
    OPENCTI_ADMIN_EMAIL=admin@opencti.io
    OPENCTI_ADMIN_PASSWORD=admin
    OPENCTI_ADMIN_TOKEN=cedd95c3-744d-43ef-a300-2bc54a99baad
    OPENCTI_BASE_URL=http://localhost:8080
    MINIO_ROOT_USER=opencti
    MINIO_ROOT_PASSWORD=admin
    RABBITMQ_DEFAULT_USER=opencti
    RABBITMQ_DEFAULT_PASS=admin
    CONNECTOR_EXPORT_FILE_STIX_ID=dd817c8b-abae-460a-9ebc-97b1551e70e6
    CONNECTOR_EXPORT_FILE_CSV_ID=7ba187fb-fde8-4063-92b5-c3da34060dd7
    CONNECTOR_EXPORT_FILE_TXT_ID=ca715d9c-bd64-4351-91db-33a8d728a58b
    CONNECTOR_IMPORT_FILE_STIX_ID=72327164-0b35-482b-b5d6-a5a3f76b845f
    CONNECTOR_IMPORT_DOCUMENT_ID=c3970f8a-ce4b-4497-a381-20b7256f56f0
    SMTP_HOSTNAME=localhost
    ELASTIC_MEMORY_SIZE=4G
```

### 3. Создаём Docker-compose.yml и запускаем его

``` bash
docker-compose up 
```



### Шаг 2. Использование системы threat intelligence OpenCTI

#### 1. После перехода на веб-ресурс OpenCTI пользователя встречает поле авторизации



#### 2. После входа появляется веб-интерфейс:



#### 3. Импортируем содержимое файла hosts.txt как индикаторы, используя API Opencti

``` python
import pycti
from stix2 import TLP_GREEN
from datetime import datetime
date = datetime.today().strftime("%Y-%m-%dT%H:%M:%SZ")

api_url = 'http://localhost:8080'
api_token = 'd19af35b-1374-4131-bf92-2afcefdaa204'
client = pycti.OpenCTIApiClient(api_url, api_token)

TLP_GREEN_CTI = client.marking_definition.read(id=TLP_GREEN["id"])
with open('hosts.txt', 'r') as f:
    domains = f.read().splitlines()
k = 1
for domain in domains:
    indicator = client.indicator.create(
    name="Malicious domain {}".format(k),
    description="Micola hosts",
    pattern_type="stix",
    label="micola hosts",
    pattern="[domain-name:value = '{}']".format(domain),
    x_opencti_main_observable_type="IPv4-Addr",
    valid_from=date,
    update=True,
    score=75,
    markingDefinitions=[TLP_GREEN_CTI["id"]],
    )
    print("Создан индикатор:", indicator["id"])
    k += 1
```

#### 4. Импортируем сетевой трафик (файл dns.log, полученный в PR2) в OpenCTI



#### 5. Добавляем dns.log в рабочую область, переходим в раздел анализа и фильтруем трафик для просмотра нежелательного



## Оценка результата

С помощью платформы OpenCTI удалось проанализировать трафик на предмет
перехода по нежелательным доменам.

## Выводы

Таким образом, были изучены возможности работы с платформой threat
intelligence OpenCTI.