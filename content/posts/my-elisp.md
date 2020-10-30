+++
title = "My Elisp"
lastmod = 2020-10-28T13:19:57-07:00
draft = false
creator = "Emacs 28.0.50 (Org mode 9.4 + ox-hugo)"
author = "GTrunSec"
+++

<style>
  .ox-hugo-toc ul {
    list-style: none;
  }
</style>
<div class="ox-hugo-toc toc">
<div></div>

<div class="heading">Table of Contents</div>

- <span class="section-num">1</span> [Elisp documents](#elisp-documents)
    - <span class="section-num">1.1</span> [GitHub - p3r7/awesome-elisp: A curated list of emacs-lisp development resources](#github-p3r7-awesome-elisp-a-curated-list-of-emacs-lisp-development-resources)
- <span class="section-num">2</span> [Buffer](#buffer)
    - <span class="section-num">2.1</span> [如何给指定文件添加模式 - Emacs-general - Emacs China](#如何给指定文件添加模式-emacs-general-emacs-china)
- <span class="section-num">3</span> [Command Interpretere](#command-interpretere)
    - <span class="section-num">3.1</span> [Comint: Writing your own Command Interpreter - Mastering Emacs](#comint-writing-your-own-command-interpreter-mastering-emacs)
- <span class="section-num">4</span> [org-mode](#org-mode)
    - <span class="section-num">4.1</span> [parsing](#parsing)
        - <span class="section-num">4.1.1</span> [Elisp: Parse Org Mode](#elisp-parse-org-mode)
    - <span class="section-num">4.2</span> [search](#search)
        - <span class="section-num">4.2.1</span> [Kungsgeten/ivy-todo: Manage org-mode TODOs with ivy](#kungsgeten-ivy-todo-manage-org-mode-todos-with-ivy)
- <span class="section-num">5</span> [learning elisp from users](#learning-elisp-from-users)
    - <span class="section-num">5.1</span> [ideasman42 · GitLab](#ideasman42-gitlab)
- <span class="section-num">6</span> [timing](#timing)
    - <span class="section-num">6.1</span> [aspiers/etrace: Emacs Lisp Latency Tracing for the Chromium Catapult Trace Event Format](#aspiers-etrace-emacs-lisp-latency-tracing-for-the-chromium-catapult-trace-event-format)

</div>
<!--endtoc-->



## <span class="section-num">1</span> Elisp documents {#elisp-documents}


### <span class="section-num">1.1</span> [GitHub - p3r7/awesome-elisp: A curated list of emacs-lisp development resources](https://github.com/p3r7/awesome-elisp) {#github-p3r7-awesome-elisp-a-curated-list-of-emacs-lisp-development-resources}


## <span class="section-num">2</span> Buffer {#buffer}


### <span class="section-num">2.1</span> [如何给指定文件添加模式 - Emacs-general - Emacs China](https://emacs-china.org/t/topic/14553/17) {#如何给指定文件添加模式-emacs-general-emacs-china}

```emacs-lisp
(add-hook 'org-mode-hook (lambda ()
  ;;……
  (cond
   ;;如果文件最后8个字符是data.org
     ((equal (substring buffer-file-name -8) "data.org")
       (progn ;;这是只对data.org文件生效的快捷键
          (local-set-key (kbd "C") 'next-line)
       ))
     (t ;对不是data.org的org文件生效的快捷键
          (local-set-key (kbd "C") 'hydra-org-mode/body)
     ))
))
```


## <span class="section-num">3</span> Command Interpretere {#command-interpretere}


### <span class="section-num">3.1</span> [Comint: Writing your own Command Interpreter - Mastering Emacs](https://www.masteringemacs.org/article/comint-writing-command-interpreter) {#comint-writing-your-own-command-interpreter-mastering-emacs}


## <span class="section-num">4</span> org-mode {#org-mode}


### <span class="section-num">4.1</span> parsing {#parsing}


#### <span class="section-num">4.1.1</span> [Elisp: Parse Org Mode](http://ergoemacs.org/emacs/elisp%5Fparse%5Forg%5Fmode.html) {#elisp-parse-org-mode}


### <span class="section-num">4.2</span> search {#search}


#### <span class="section-num">4.2.1</span> [Kungsgeten/ivy-todo: Manage org-mode TODOs with ivy](https://github.com/Kungsgeten/ivy-todo) {#kungsgeten-ivy-todo-manage-org-mode-todos-with-ivy}


## <span class="section-num">5</span> learning elisp from users {#learning-elisp-from-users}


### <span class="section-num">5.1</span> [ideasman42 · GitLab](https://gitlab.com/ideasman42) {#ideasman42-gitlab}


## <span class="section-num">6</span> timing {#timing}


### <span class="section-num">6.1</span> [aspiers/etrace: Emacs Lisp Latency Tracing for the Chromium Catapult Trace Event Format](https://github.com/aspiers/etrace) {#aspiers-etrace-emacs-lisp-latency-tracing-for-the-chromium-catapult-trace-event-format}
