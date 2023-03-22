Лабораторная работа № 1
================

# Системы аутентификациии и защиты от несанкционированного доступа

Лабораторная работа №1

## Цель работы

Вывести информацию о процессоре, операционной системе и о последних
логах

## Исходные данные

1.  ОС Windows 11
2.  RStudio Desktop
3.  Интерпретатор языка R 4.2.2

## План

1.  Выполнить команду “systeminfo”
2.  Выполнить команду “wmic cpu get name”
3.  Выполнить команду “Get-EventLog -LogName System -Newest 30”

## Шаги

### Шаг 1

Выполнение команды “systeminfo” для вывода информации об операционной
системе Windows

``` r
system2("systeminfo", stdout = TRUE)
```

     [1] ""                                                                                                               
     [2] "Host Name:                 LAPTOP-7UH81QUH"                                                                     
     [3] "OS Name:                   Microsoft Windows 11 Home Single Language"                                           
     [4] "OS Version:                10.0.22000 N/A Build 22000"                                                          
     [5] "OS Manufacturer:           Microsoft Corporation"                                                               
     [6] "OS Configuration:          Standalone Workstation"                                                              
     [7] "OS Build Type:             Multiprocessor Free"                                                                 
     [8] "Registered Owner:          mrceed02@mail.ru"                                                                    
     [9] "Registered Organization:   N/A"                                                                                 
    [10] "Product ID:                00342-41416-60096-AAOEM"                                                             
    [11] "Original Install Date:     28.10.2021, 10:53:40"                                                                
    [12] "System Boot Time:          21.03.2023, 20:43:26"                                                                
    [13] "System Manufacturer:       HUAWEI"                                                                              
    [14] "System Model:              NBLK-WAX9X"                                                                          
    [15] "System Type:               x64-based PC"                                                                        
    [16] "Processor(s):              1 Processor(s) Installed."                                                           
    [17] "                           [01]: AMD64 Family 23 Model 24 Stepping 1 AuthenticAMD ~2100 Mhz"                    
    [18] "BIOS Version:              HUAWEI 1.18, 30.03.2022"                                                             
    [19] "Windows Directory:         C:\\WINDOWS"                                                                         
    [20] "System Directory:          C:\\WINDOWS\\system32"                                                               
    [21] "Boot Device:               \\Device\\HarddiskVolume1"                                                           
    [22] "System Locale:             ru;Russian"                                                                          
    [23] "Input Locale:              ru;Russian"                                                                          
    [24] "Time Zone:                 (UTC+03:00) Moscow, St. Petersburg"                                                  
    [25] "Total Physical Memory:     7 104 MB"                                                                            
    [26] "Available Physical Memory: 486 MB"                                                                              
    [27] "Virtual Memory: Max Size:  12 746 MB"                                                                           
    [28] "Virtual Memory: Available: 2 025 MB"                                                                            
    [29] "Virtual Memory: In Use:    10 721 MB"                                                                           
    [30] "Page File Location(s):     C:\\pagefile.sys"                                                                    
    [31] "Domain:                    WORKGROUP"                                                                           
    [32] "Logon Server:              \\\\LAPTOP-7UH81QUH"                                                                 
    [33] "Hotfix(s):                 7 Hotfix(s) Installed."                                                              
    [34] "                           [01]: KB5022505"                                                                     
    [35] "                           [02]: KB5004567"                                                                     
    [36] "                           [03]: KB5008295"                                                                     
    [37] "                           [04]: KB5012170"                                                                     
    [38] "                           [05]: KB5014869"                                                                     
    [39] "                           [06]: KB5019961"                                                                     
    [40] "                           [07]: KB5022925"                                                                     
    [41] "Network Card(s):           4 NIC(s) Installed."                                                                 
    [42] "                           [01]: Realtek 8822CE Wireless LAN 802.11ac PCI-E NIC"                                
    [43] "                                 Connection Name: Беспроводная сеть"                                            
    [44] "                                 DHCP Enabled:    Yes"                                                          
    [45] "                                 DHCP Server:     192.168.25.244"                                               
    [46] "                                 IP address(es)"                                                                
    [47] "                                 [01]: 192.168.25.172"                                                          
    [48] "                                 [02]: fe80::4890:216f:1e06:bd4c"                                               
    [49] "                           [02]: TAP-Windows Adapter V9"                                                        
    [50] "                                 Connection Name: Ethernet 2"                                                   
    [51] "                                 Status:          Media disconnected"                                           
    [52] "                           [03]: Bluetooth Device (Personal Area Network)"                                      
    [53] "                                 Connection Name: Сетевое подключение Bluetooth"                                
    [54] "                                 Status:          Media disconnected"                                           
    [55] "                           [04]: VirtualBox Host-Only Ethernet Adapter"                                         
    [56] "                                 Connection Name: Ethernet 3"                                                   
    [57] "                                 DHCP Enabled:    No"                                                           
    [58] "                                 IP address(es)"                                                                
    [59] "                                 [01]: 192.168.56.1"                                                            
    [60] "                                 [02]: fe80::ba3f:338d:3318:fccc"                                               
    [61] "Hyper-V Requirements:      A hypervisor has been detected. Features required for Hyper-V will not be displayed."

### Шаг 2

Выполнение команды “wmic cpu get name” для вывода информации о
процессоре

``` r
system("wmic cpu get name", intern = TRUE)
```

    [1] "Name                                           \r"
    [2] "AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx  \r"
    [3] "\r"                                               

### Шаг 3

Выполнение команды “Get-EventLog -LogName System -Newest 30” для
получения информации о последних логах системы

``` r
system2("powershell", args = "Get-EventLog -LogName System -Newest 30", stdout = TRUE)
```

     [1] ""                                                                                                                        
     [2] "   Index Time          EntryType   Source                 InstanceID Message                                           " 
     [3] "   ----- ----          ---------   ------                 ---------- -------                                           " 
     [4] "   71255 мар 22 09:55  Warning     DCOM                        10016 The description for Event ID '10016' in Source ..." 
     [5] "   71254 мар 22 09:55  Warning     DCOM                        10016 The description for Event ID '10016' in Source ..." 
     [6] "   71253 мар 22 09:49  Error       disk                   3221487627 The driver detected a controller error on \\Devi..."
     [7] "   71252 мар 22 09:48  Information Microsoft-Windows...           16 The description for Event ID '16' in Source 'Mi..." 
     [8] "   71251 мар 22 09:48  Information Microsoft-Windows...           16 The description for Event ID '16' in Source 'Mi..." 
     [9] "   71250 мар 22 09:48  Information Microsoft-Windows...           16 The description for Event ID '16' in Source 'Mi..." 
    [10] "   71249 мар 22 09:48  Information Microsoft-Windows...           16 The description for Event ID '16' in Source 'Mi..." 
    [11] "   71248 мар 22 09:42  Information Microsoft-Windows...           16 The description for Event ID '16' in Source 'Mi..." 
    [12] "   71247 мар 22 09:41  Warning     DCOM                        10016 The description for Event ID '10016' in Source ..." 
    [13] "   71246 мар 22 09:37  Error       Microsoft-Windows...           20 Installation Failure: Windows failed to install..." 
    [14] "   71245 мар 22 09:37  Information Service Control M...   1073748864 The start type of the Установщик модулей Window..." 
    [15] "   71244 мар 22 09:36  Error       Server                 3221227977 The server could not bind to the transport \\Dev..."
    [16] "   71243 мар 22 09:33  Error       Server                 3221227977 The server could not bind to the transport \\Dev..."
    [17] "   71242 мар 22 09:32  Error       Server                 3221227977 The server could not bind to the transport \\Dev..."
    [18] "   71241 мар 22 09:32  Error       Server                 3221227977 The server could not bind to the transport \\Dev..."
    [19] "   71240 мар 22 09:31  Error       Server                 3221227977 The server could not bind to the transport \\Dev..."
    [20] "   71239 мар 22 09:30  Error       Server                 3221227977 The server could not bind to the transport \\Dev..."
    [21] "   71238 мар 22 09:29  Warning     DCOM                        10016 The description for Event ID '10016' in Source ..." 
    [22] "   71237 мар 22 09:29  Information Microsoft-Windows...           98 The description for Event ID '98' in Source 'Mi..." 
    [23] "   71236 мар 22 09:28  Information Service Control M...   1073748864 The start type of the Установщик модулей Window..." 
    [24] "   71235 мар 22 09:26  Information Microsoft-Windows...            6 File System Filter 'WIMMount' (10.0, 2023-01-05..." 
    [25] "   71234 мар 22 09:25  Information Microsoft-Windows...           43 Installation Started: Windows has started insta..." 
    [26] "   71233 мар 22 09:23  Information Service Control M...   1073748864 The start type of the Фоновая интеллектуальная ..." 
    [27] "   71232 мар 22 09:20  Information Service Control M...   1073748864 The start type of the Фоновая интеллектуальная ..." 
    [28] "   71231 мар 22 09:19  Information volsnap                1074135073 The oldest shadow copy of volume C: was deleted..." 
    [29] "   71230 мар 22 09:16  Information Microsoft-Windows...           16 The description for Event ID '16' in Source 'Mi..." 
    [30] "   71229 мар 22 09:15  Error       Server                 3221227977 The server could not bind to the transport \\Dev..."
    [31] "   71228 мар 22 09:15  Information Service Control M...   1073748864 The start type of the Установщик модулей Window..." 
    [32] "   71227 мар 22 09:10  Information Microsoft-Windows...           44 Windows Update started downloading an update.     " 
    [33] "   71226 мар 22 09:10  Information Service Control M...   1073748864 The start type of the Установщик модулей Window..." 
    [34] ""                                                                                                                        
    [35] ""                                                                                                                        

## Оценка результата

В результате лабораторной работы была получена информация о процессоре,
об операционной системе и о последних логах

## Вывод

В результате выполнения работы были получены навыки работы с командами
Windows через среду разработки RStudio
