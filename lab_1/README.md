</head>

<body class="fullcontent">

<div id="quarto-content" class="page-columns page-rows-contents page-layout-article">

<main class="content" id="quarto-document-content">



<section id="системы-аутентификациии-и-защиты-от-несанкционированного-доступа" class="level1">
<h1>Системы аутентификациии и защиты от несанкционированного доступа</h1>
<p>Лабораторная работа №1</p>
<section id="цель-работы" class="level2">
<h2 class="anchored" data-anchor-id="цель-работы">Цель работы</h2>
<p>Вывести информацию о процессоре, операционной системе и о последних логах</p>
</section>
<section id="исходные-данные" class="level2">
<h2 class="anchored" data-anchor-id="исходные-данные">Исходные данные</h2>
<ol type="1">
<li>ОС Windows 11</li>
<li>RStudio Desktop</li>
<li>Интерпретатор языка R 4.2.2</li>
</ol>
</section>
<section id="план" class="level2">
<h2 class="anchored" data-anchor-id="план">План</h2>
<ol type="1">
<li>Выполнить команду “systeminfo”</li>
<li>Выполнить команду “wmic cpu get name”</li>
<li>Выполнить команду “Get-EventLog -LogName System -Newest 30”</li>
</ol>
</section>
<section id="шаги" class="level2">
<h2 class="anchored" data-anchor-id="шаги">Шаги</h2>
<section id="шаг-1" class="level3">
<h3 class="anchored" data-anchor-id="шаг-1">Шаг 1</h3>
<p>Выполнение команды “systeminfo” для вывода информации об операционной системе Windows</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb1"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a><span class="fu">system2</span>(<span class="st">"systeminfo"</span>, <span class="at">stdout =</span> <span class="cn">TRUE</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code> [1] ""                                                                                                               
 [2] "Host Name:                 LAPTOP-7UH81QUH"                                                                     
 [3] "OS Name:                   Майкрософт Windows 11 Домашняя для одного языка"                                     
 [4] "OS Version:                10.0.22000 N/A Build 22000"                                                          
 [5] "OS Manufacturer:           Microsoft Corporation"                                                               
 [6] "OS Configuration:          Standalone Workstation"                                                              
 [7] "OS Build Type:             Multiprocessor Free"                                                                 
 [8] "Registered Owner:          mrceed02@mail.ru"                                                                    
 [9] "Registered Organization:   N/A"                                                                                 
[10] "Product ID:                00342-41416-60096-AAOEM"                                                             
[11] "Original Install Date:     28.10.2021, 10:53:40"                                                                
[12] "System Boot Time:          01.03.2023, 17:31:03"                                                                
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
[25] "Total Physical Memory:     7&nbsp;104 MB"                                                                            
[26] "Available Physical Memory: 1&nbsp;293 MB"                                                                            
[27] "Virtual Memory: Max Size:  12&nbsp;671 MB"                                                                           
[28] "Virtual Memory: Available: 2&nbsp;175 MB"                                                                            
[29] "Virtual Memory: In Use:    10&nbsp;496 MB"                                                                           
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
[45] "                                 DHCP Server:     192.168.0.1"                                                  
[46] "                                 IP address(es)"                                                                
[47] "                                 [01]: 192.168.0.100"                                                           
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
[60] "                                 [02]: fe80::9961:96e6:dad8:d77f"                                               
[61] "Hyper-V Requirements:      A hypervisor has been detected. Features required for Hyper-V will not be displayed."</code></pre>
</div>
</div>
</section>
<section id="шаг-2" class="level3">
<h3 class="anchored" data-anchor-id="шаг-2">Шаг 2</h3>
<p>Выполнение команды “wmic cpu get name” для вывода информации о процессоре</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb3"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb3-1"><a href="#cb3-1" aria-hidden="true" tabindex="-1"></a><span class="fu">system</span>(<span class="st">"wmic cpu get name"</span>, <span class="at">intern =</span> <span class="cn">TRUE</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] "Name                                           \r"
[2] "AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx  \r"
[3] "\r"                                               </code></pre>
</div>
</div>
</section>
<section id="шаг-3" class="level3">
<h3 class="anchored" data-anchor-id="шаг-3">Шаг 3</h3>
<p>Выполнение команды “Get-EventLog -LogName System -Newest 30” для получения информации о последних логах системы</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb5"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb5-1"><a href="#cb5-1" aria-hidden="true" tabindex="-1"></a><span class="fu">system2</span>(<span class="st">"powershell"</span>, <span class="at">args =</span> <span class="st">"Get-EventLog -LogName System -Newest 30"</span>, <span class="at">stdout =</span> <span class="cn">TRUE</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code> [1] ""                                                                                                                        
 [2] "   Index Time          EntryType   Source                 InstanceID Message                                           " 
 [3] "   ----- ----          ---------   ------                 ---------- -------                                           " 
 [4] "   68810 мар 08 17:59  Information Microsoft-Windows...           16 The description for Event ID '16' in Source 'Mi..." 
 [5] "   68809 мар 08 17:37  Warning     DCOM                        10016 The description for Event ID '10016' in Source ..." 
 [6] "   68808 мар 08 17:04  Information Microsoft-Windows...           16 The description for Event ID '16' in Source 'Mi..." 
 [7] "   68807 мар 08 17:04  Warning     DCOM                        10016 The description for Event ID '10016' in Source ..." 
 [8] "   68806 мар 08 17:02  Information Microsoft-Windows...          105 The description for Event ID '105' in Source 'M..." 
 [9] "   68805 мар 08 16:46  Warning     DCOM                        10016 The description for Event ID '10016' in Source ..." 
[10] "   68804 мар 08 16:31  Information Service Control M...   1073748864 The start type of the Фоновая интеллектуальная ..." 
[11] "   68803 мар 08 16:28  Information Service Control M...   1073748864 The start type of the Фоновая интеллектуальная ..." 
[12] "   68802 мар 08 16:27  Warning     DCOM                        10016 The description for Event ID '10016' in Source ..." 
[13] "   68801 мар 08 16:17  Warning     DCOM                        10016 The description for Event ID '10016' in Source ..." 
[14] "   68800 мар 08 16:12  Error       VBoxNetLwf             3221487628 The driver detected an internal driver error on..." 
[15] "   68799 мар 08 16:12  Information Service Control M...   1073748869 A service was installed in the system....         " 
[16] "   68798 мар 08 16:12  Information Microsoft-Windows...        20003 Driver Management has concluded the process to ..." 
[17] "   68797 мар 08 16:12  Information Service Control M...   1073748869 A service was installed in the system....         " 
[18] "   68796 мар 08 16:12  Error       Server                 3221227977 The server could not bind to the transport \\Dev..."
[19] "   68795 мар 08 16:12  Information Service Control M...   1073748869 A service was installed in the system....         " 
[20] "   68794 мар 08 16:12  Information Service Control M...   1073748869 A service was installed in the system....         " 
[21] "   68793 мар 08 16:12  Information Service Control M...   1073748869 A service was installed in the system....         " 
[22] "   68792 мар 08 16:12  Information Microsoft-Windows...           98 The description for Event ID '98' in Source 'Mi..." 
[23] "   68791 мар 08 15:13  Information Microsoft-Windows...          105 The description for Event ID '105' in Source 'M..." 
[24] "   68790 мар 08 14:56  Error       Server                 3221227977 The server could not bind to the transport \\Dev..."
[25] "   68789 мар 08 14:56  Information Microsoft-Windows...            1 The system has returned from a low power state...." 
[26] "   68788 мар 08 14:56  Information Microsoft-Windows...           16 The description for Event ID '16' in Source 'Mi..." 
[27] "   68787 мар 08 14:56  Information Microsoft-Windows...          566 The description for Event ID '566' in Source 'M..." 
[28] "   68786 мар 08 14:56  Information Microsoft-Windows...          566 The description for Event ID '566' in Source 'M..." 
[29] "   68785 мар 08 14:56  Information BTHUSB                 1074069522 Windows cannot store Bluetooth authentication c..." 
[30] "   68784 мар 08 14:56  Information Microsoft-Windows...          130 The description for Event ID '130' in Source 'M..." 
[31] "   68783 мар 08 14:56  Information Microsoft-Windows...          131 The description for Event ID '131' in Source 'M..." 
[32] "   68782 мар 08 14:56  Information Microsoft-Windows...            1 Possible detection of CVE: 2023-03-08T11:56:19...." 
[33] "   68781 мар 08 14:36  Information Microsoft-Windows...          107 The description for Event ID '107' in Source 'M..." 
[34] ""                                                                                                                        
[35] ""                                                                                                                        </code></pre>
</div>
</div>
</section>
</section>
<section id="оценка-результата" class="level2">
<h2 class="anchored" data-anchor-id="оценка-результата">Оценка результата</h2>
<p>В результате лабораторной работы была получена информация о процессоре, об операционной системе и о последних логах</p>
</section>
<section id="вывод" class="level2">
<h2 class="anchored" data-anchor-id="вывод">Вывод</h2>
<p>В результате выполнения работы были получены навыки работы с командами Windows через среду разработки RStudio</p>
</section>
</section>
</body></html>
