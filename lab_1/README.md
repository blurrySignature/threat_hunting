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
<li>Выполнить команду system(“systeminfo”)</li>
<li>Выполнить команду system(“wmic cpu get name”)</li>
<li>Выполнить команду system2(“powershell”, args = “Get-EventLog -LogName System -Newest 30”, stdout = TRUE)</li>
</ol>
</section>
<section id="шаги" class="level2">
<h2 class="anchored" data-anchor-id="шаги">Шаги</h2>
<section id="шаг-1" class="level3">
<h3 class="anchored" data-anchor-id="шаг-1">Шаг 1</h3>
<p>Выполнение команды system(“systeminfo”) для вывода информации об операционной системе Windows</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb1"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a><span class="fu">system</span>(<span class="st">"systeminfo"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 0</code></pre>
</div>
</div>
</section>
<section id="шаг-2" class="level3">
<h3 class="anchored" data-anchor-id="шаг-2">Шаг 2</h3>
<p>Выполнение команды system(“wmic cpu get name”) для вывода информации о процессоре</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb3"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb3-1"><a href="#cb3-1" aria-hidden="true" tabindex="-1"></a><span class="fu">system</span>(<span class="st">"wmic cpu get name"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 0</code></pre>
</div>
</div>
</section>
<section id="шаг-3" class="level3">
<h3 class="anchored" data-anchor-id="шаг-3">Шаг 3</h3>
<p>Выполнение команды system2(“powershell”, args = “Get-EventLog -LogName System -Newest 30”, stdout = TRUE) для получения информации о последних логах системы</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb5"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb5-1"><a href="#cb5-1" aria-hidden="true" tabindex="-1"></a><span class="fu">system2</span>(<span class="st">"powershell"</span>, <span class="at">args =</span> <span class="st">"Get-EventLog -LogName System -Newest 30"</span>, <span class="at">stdout =</span> <span class="cn">TRUE</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code> [1] ""                                                                                                                        
 [2] "   Index Time          EntryType   Source                 InstanceID Message                                           " 
 [3] "   ----- ----          ---------   ------                 ---------- -------                                           " 
 [4] "   68808 мар 08 17:04  Information Microsoft-Windows...           16 The description for Event ID '16' in Source 'Mi..." 
 [5] "   68807 мар 08 17:04  Warning     DCOM                        10016 The description for Event ID '10016' in Source ..." 
 [6] "   68806 мар 08 17:02  Information Microsoft-Windows...          105 The description for Event ID '105' in Source 'M..." 
 [7] "   68805 мар 08 16:46  Warning     DCOM                        10016 The description for Event ID '10016' in Source ..." 
 [8] "   68804 мар 08 16:31  Information Service Control M...   1073748864 The start type of the Фоновая интеллектуальная ..." 
 [9] "   68803 мар 08 16:28  Information Service Control M...   1073748864 The start type of the Фоновая интеллектуальная ..." 
[10] "   68802 мар 08 16:27  Warning     DCOM                        10016 The description for Event ID '10016' in Source ..." 
[11] "   68801 мар 08 16:17  Warning     DCOM                        10016 The description for Event ID '10016' in Source ..." 
[12] "   68800 мар 08 16:12  Error       VBoxNetLwf             3221487628 The driver detected an internal driver error on..." 
[13] "   68799 мар 08 16:12  Information Service Control M...   1073748869 A service was installed in the system....         " 
[14] "   68798 мар 08 16:12  Information Microsoft-Windows...        20003 Driver Management has concluded the process to ..." 
[15] "   68797 мар 08 16:12  Information Service Control M...   1073748869 A service was installed in the system....         " 
[16] "   68796 мар 08 16:12  Error       Server                 3221227977 The server could not bind to the transport \\Dev..."
[17] "   68795 мар 08 16:12  Information Service Control M...   1073748869 A service was installed in the system....         " 
[18] "   68794 мар 08 16:12  Information Service Control M...   1073748869 A service was installed in the system....         " 
[19] "   68793 мар 08 16:12  Information Service Control M...   1073748869 A service was installed in the system....         " 
[20] "   68792 мар 08 16:12  Information Microsoft-Windows...           98 The description for Event ID '98' in Source 'Mi..." 
[21] "   68791 мар 08 15:13  Information Microsoft-Windows...          105 The description for Event ID '105' in Source 'M..." 
[22] "   68790 мар 08 14:56  Error       Server                 3221227977 The server could not bind to the transport \\Dev..."
[23] "   68789 мар 08 14:56  Information Microsoft-Windows...            1 The system has returned from a low power state...." 
[24] "   68788 мар 08 14:56  Information Microsoft-Windows...           16 The description for Event ID '16' in Source 'Mi..." 
[25] "   68787 мар 08 14:56  Information Microsoft-Windows...          566 The description for Event ID '566' in Source 'M..." 
[26] "   68786 мар 08 14:56  Information Microsoft-Windows...          566 The description for Event ID '566' in Source 'M..." 
[27] "   68785 мар 08 14:56  Information BTHUSB                 1074069522 Windows cannot store Bluetooth authentication c..." 
[28] "   68784 мар 08 14:56  Information Microsoft-Windows...          130 The description for Event ID '130' in Source 'M..." 
[29] "   68783 мар 08 14:56  Information Microsoft-Windows...          131 The description for Event ID '131' in Source 'M..." 
[30] "   68782 мар 08 14:56  Information Microsoft-Windows...            1 Possible detection of CVE: 2023-03-08T11:56:19...." 
[31] "   68781 мар 08 14:36  Information Microsoft-Windows...          107 The description for Event ID '107' in Source 'M..." 
[32] "   68780 мар 08 14:36  Information Microsoft-Windows...           42 The description for Event ID '42' in Source 'Mi..." 
[33] "   68779 мар 08 14:36  Information Microsoft-Windows...          566 The description for Event ID '566' in Source 'M..." 
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

</main>
<!-- /main column -->
<script id="quarto-html-after-body" type="application/javascript">
window.document.addEventListener("DOMContentLoaded", function (event) {
  const toggleBodyColorMode = (bsSheetEl) => {
    const mode = bsSheetEl.getAttribute("data-mode");
    const bodyEl = window.document.querySelector("body");
    if (mode === "dark") {
      bodyEl.classList.add("quarto-dark");
      bodyEl.classList.remove("quarto-light");
    } else {
      bodyEl.classList.add("quarto-light");
      bodyEl.classList.remove("quarto-dark");
    }
  }
  const toggleBodyColorPrimary = () => {
    const bsSheetEl = window.document.querySelector("link#quarto-bootstrap");
    if (bsSheetEl) {
      toggleBodyColorMode(bsSheetEl);
    }
  }
  toggleBodyColorPrimary();  
  const icon = "";
  const anchorJS = new window.AnchorJS();
  anchorJS.options = {
    placement: 'right',
    icon: icon
  };
  anchorJS.add('.anchored');
  const clipboard = new window.ClipboardJS('.code-copy-button', {
    target: function(trigger) {
      return trigger.previousElementSibling;
    }
  });
  clipboard.on('success', function(e) {
    // button target
    const button = e.trigger;
    // don't keep focus
    button.blur();
    // flash "checked"
    button.classList.add('code-copy-button-checked');
    var currentTitle = button.getAttribute("title");
    button.setAttribute("title", "Copied!");
    let tooltip;
    if (window.bootstrap) {
      button.setAttribute("data-bs-toggle", "tooltip");
      button.setAttribute("data-bs-placement", "left");
      button.setAttribute("data-bs-title", "Copied!");
      tooltip = new bootstrap.Tooltip(button, 
        { trigger: "manual", 
          customClass: "code-copy-button-tooltip",
          offset: [0, -8]});
      tooltip.show();    
    }
    setTimeout(function() {
      if (tooltip) {
        tooltip.hide();
        button.removeAttribute("data-bs-title");
        button.removeAttribute("data-bs-toggle");
        button.removeAttribute("data-bs-placement");
      }
      button.setAttribute("title", currentTitle);
      button.classList.remove('code-copy-button-checked');
    }, 1000);
    // clear code selection
    e.clearSelection();
  });
  function tippyHover(el, contentFn) {
    const config = {
      allowHTML: true,
      content: contentFn,
      maxWidth: 500,
      delay: 100,
      arrow: false,
      appendTo: function(el) {
          return el.parentElement;
      },
      interactive: true,
      interactiveBorder: 10,
      theme: 'quarto',
      placement: 'bottom-start'
    };
    window.tippy(el, config); 
  }
  const noterefs = window.document.querySelectorAll('a[role="doc-noteref"]');
  for (var i=0; i<noterefs.length; i++) {
    const ref = noterefs[i];
    tippyHover(ref, function() {
      // use id or data attribute instead here
      let href = ref.getAttribute('data-footnote-href') || ref.getAttribute('href');
      try { href = new URL(href).hash; } catch {}
      const id = href.replace(/^#\/?/, "");
      const note = window.document.getElementById(id);
      return note.innerHTML;
    });
  }
  const findCites = (el) => {
    const parentEl = el.parentElement;
    if (parentEl) {
      const cites = parentEl.dataset.cites;
      if (cites) {
        return {
          el,
          cites: cites.split(' ')
        };
      } else {
        return findCites(el.parentElement)
      }
    } else {
      return undefined;
    }
  };
  var bibliorefs = window.document.querySelectorAll('a[role="doc-biblioref"]');
  for (var i=0; i<bibliorefs.length; i++) {
    const ref = bibliorefs[i];
    const citeInfo = findCites(ref);
    if (citeInfo) {
      tippyHover(citeInfo.el, function() {
        var popup = window.document.createElement('div');
        citeInfo.cites.forEach(function(cite) {
          var citeDiv = window.document.createElement('div');
          citeDiv.classList.add('hanging-indent');
          citeDiv.classList.add('csl-entry');
          var biblioDiv = window.document.getElementById('ref-' + cite);
          if (biblioDiv) {
            citeDiv.innerHTML = biblioDiv.innerHTML;
          }
          popup.appendChild(citeDiv);
        });
        return popup.innerHTML;
      });
    }
  }
});
</script>
</div> <!-- /content -->



</body></html>
