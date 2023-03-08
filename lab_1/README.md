<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en"><head>

<meta charset="utf-8">
<meta name="generator" content="quarto-1.2.269">

<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">


<title>lab_1</title>
<style>
code{white-space: pre-wrap;}
span.smallcaps{font-variant: small-caps;}
div.columns{display: flex; gap: min(4vw, 1.5em);}
div.column{flex: auto; overflow-x: auto;}
div.hanging-indent{margin-left: 1.5em; text-indent: -1.5em;}
ul.task-list{list-style: none;}
ul.task-list li input[type="checkbox"] {
  width: 0.8em;
  margin: 0 0.8em 0.2em -1.6em;
  vertical-align: middle;
}
pre > code.sourceCode { white-space: pre; position: relative; }
pre > code.sourceCode > span { display: inline-block; line-height: 1.25; }
pre > code.sourceCode > span:empty { height: 1.2em; }
.sourceCode { overflow: visible; }
code.sourceCode > span { color: inherit; text-decoration: inherit; }
div.sourceCode { margin: 1em 0; }
pre.sourceCode { margin: 0; }
@media screen {
div.sourceCode { overflow: auto; }
}
@media print {
pre > code.sourceCode { white-space: pre-wrap; }
pre > code.sourceCode > span { text-indent: -5em; padding-left: 5em; }
}
pre.numberSource code
  { counter-reset: source-line 0; }
pre.numberSource code > span
  { position: relative; left: -4em; counter-increment: source-line; }
pre.numberSource code > span > a:first-child::before
  { content: counter(source-line);
    position: relative; left: -1em; text-align: right; vertical-align: baseline;
    border: none; display: inline-block;
    -webkit-touch-callout: none; -webkit-user-select: none;
    -khtml-user-select: none; -moz-user-select: none;
    -ms-user-select: none; user-select: none;
    padding: 0 4px; width: 4em;
    color: #aaaaaa;
  }
pre.numberSource { margin-left: 3em; border-left: 1px solid #aaaaaa;  padding-left: 4px; }
div.sourceCode
  {   }
@media screen {
pre > code.sourceCode > span > a:first-child::before { text-decoration: underline; }
}
code span.al { color: #ff0000; font-weight: bold; } /* Alert */
code span.an { color: #60a0b0; font-weight: bold; font-style: italic; } /* Annotation */
code span.at { color: #7d9029; } /* Attribute */
code span.bn { color: #40a070; } /* BaseN */
code span.bu { color: #008000; } /* BuiltIn */
code span.cf { color: #007020; font-weight: bold; } /* ControlFlow */
code span.ch { color: #4070a0; } /* Char */
code span.cn { color: #880000; } /* Constant */
code span.co { color: #60a0b0; font-style: italic; } /* Comment */
code span.cv { color: #60a0b0; font-weight: bold; font-style: italic; } /* CommentVar */
code span.do { color: #ba2121; font-style: italic; } /* Documentation */
code span.dt { color: #902000; } /* DataType */
code span.dv { color: #40a070; } /* DecVal */
code span.er { color: #ff0000; font-weight: bold; } /* Error */
code span.ex { } /* Extension */
code span.fl { color: #40a070; } /* Float */
code span.fu { color: #06287e; } /* Function */
code span.im { color: #008000; font-weight: bold; } /* Import */
code span.in { color: #60a0b0; font-weight: bold; font-style: italic; } /* Information */
code span.kw { color: #007020; font-weight: bold; } /* Keyword */
code span.op { color: #666666; } /* Operator */
code span.ot { color: #007020; } /* Other */
code span.pp { color: #bc7a00; } /* Preprocessor */
code span.sc { color: #4070a0; } /* SpecialChar */
code span.ss { color: #bb6688; } /* SpecialString */
code span.st { color: #4070a0; } /* String */
code span.va { color: #19177c; } /* Variable */
code span.vs { color: #4070a0; } /* VerbatimString */
code span.wa { color: #60a0b0; font-weight: bold; font-style: italic; } /* Warning */
</style>


<script src="lab_1_files/libs/clipboard/clipboard.min.js"></script>
<script src="lab_1_files/libs/quarto-html/quarto.js"></script>
<script src="lab_1_files/libs/quarto-html/popper.min.js"></script>
<script src="lab_1_files/libs/quarto-html/tippy.umd.min.js"></script>
<script src="lab_1_files/libs/quarto-html/anchor.min.js"></script>
<link href="lab_1_files/libs/quarto-html/tippy.css" rel="stylesheet">
<link href="lab_1_files/libs/quarto-html/quarto-syntax-highlighting.css" rel="stylesheet" id="quarto-text-highlighting-styles">
<script src="lab_1_files/libs/bootstrap/bootstrap.min.js"></script>
<link href="lab_1_files/libs/bootstrap/bootstrap-icons.css" rel="stylesheet">
<link href="lab_1_files/libs/bootstrap/bootstrap.min.css" rel="stylesheet" id="quarto-bootstrap" data-mode="light">


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