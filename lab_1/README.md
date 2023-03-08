# Системы аутентификациии и защиты от несанкционированного доступа

Лабораторная работа №1

## Цель работы

Вывести информацию о процессоре, операционной системе и о последних логах

## Исходные данные

1.  ОС Windows 11
2.  RStudio Desktop
3.  Интерпретатор языка R 4.2.2

## План

1.  Выполнить команду system("systeminfo")
2.  Выполнить команду system("wmic cpu get name")
3.  Выполнить команду system2("powershell", args = "Get-EventLog -LogName System -Newest 30", stdout = TRUE)


## Шаги

### Шаг 1
Выполнение команды system("systeminfo") для вывода информации об операционной системе Windows

    ```{r}
    system("systeminfo")
    ```

### Шаг 2
Выполнение команды system("wmic cpu get name") для вывода информации о процессоре

    ```{r}
    system("wmic cpu get name")
    ```

### Шаг 3
Выполнение команды system2("powershell", args = "Get-EventLog -LogName System -Newest 30", stdout = TRUE) для получения информации о последних логах системы

    ```{r}
    system2("powershell", args = "Get-EventLog -LogName System -Newest 30", stdout = TRUE)

    ```

## Оценка результата

В результате лабораторной работы была получена информация о процессоре, об операционной системе и о последних логах

## Вывод

В результате выполнения работы были получены навыки работы с командами Windows с помощью языка R