+++
title = "GuangTao's Xah Fly Keys config"
lastmod = 2020-09-23T03:30:31-07:00
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

- <span class="section-num">1</span> [use package with xah-fly-keys](#use-package-with-xah-fly-keys)
- <span class="section-num">2</span> [define-key xah-fly-keys-map(Insert mode)](#define-key-xah-fly-keys-map--insert-mode)
- <span class="section-num">3</span> [define-key xah-fly-keys-map(Command mode)](#define-key-xah-fly-keys-map--command-mode)
- <span class="section-num">4</span> [specific keys in different mode map](#specific-keys-in-different-mode-map)
    - <span class="section-num">4.1</span> [load all of specific keys](#load-all-of-specific-keys)
    - <span class="section-num">4.2</span> [Only Linux keys](#only-linux-keys)
    - <span class="section-num">4.3</span> [.-dot](#dot-dot)
    - <span class="section-num">4.4</span> [,-comma](#comma)
    - <span class="section-num">4.5</span> [/-slash](#slash)
    - <span class="section-num">4.6</span> [;-semicolon](#semicolon)
    - <span class="section-num">4.7</span> ['-apostrophe](#apostrophe)
    - <span class="section-num">4.8</span> [=-e](#e)
    - <span class="section-num">4.9</span> [p-keymap](#p-keymap)
    - <span class="section-num">4.10</span> [P-key](#p-key)
    - <span class="section-num">4.11</span> [&#x2013;minus](#and-x2013-minus)
    - <span class="section-num">4.12</span> [Color](#color)
- <span class="section-num">5</span> [define-key xah-fly-leader-key-map](#define-key-xah-fly-leader-key-map)
- <span class="section-num">6</span> [search-keys (leader-key to "s")](#search-keys--leader-key-to-s)
- <span class="section-num">7</span> [org-keys (leader-key to "o")](#org-keys--leader-key-to-o)
- <span class="section-num">8</span> [magit-keys (leader-key to "m")](#magit-keys--leader-key-to-m)

</div>
<!--endtoc-->

-   [Emacs: Xah Fly Keys Customization](http://ergoemacs.org/misc/xah-fly-keys%5Fcustomization.html)
-   [Emacs: Xah Fly Keys Tutorial](http://ergoemacs.org/misc/xah-fly-keys%5Ftutorial.html)


## <span class="section-num">1</span> use package with xah-fly-keys {#use-package-with-xah-fly-keys}

```emacs-lisp
(use-package! xah-fly-keys
  :config
  (xah-fly-keys 1)
  (add-hook 'xah-fly-command-mode-activate-hook
            (lambda ()
              (setq xah-fly-insert-state-q nil)))
  )
```


## <span class="section-num">2</span> define-key xah-fly-keys-map(Insert mode) {#define-key-xah-fly-keys-map--insert-mode}

```emacs-lisp
(defun xah-fly-insert-mode-init ()
  (xah-fly--define-keys
   xah-fly-key-map
   '(
     ("SPC" . nil)
     ("DEL" . nil)

     ("a" . nil)
     ("b" . nil)
     ("c" . nil)
     ("d" . nil)
     ("e" . nil)
     ("f" . nil)
     ("g" . nil)
     ("h" . nil)
     ("i" . nil)
     ("j" . nil)
     ("k" . nil)
     ("l" . nil)
     ("m" . nil)
     ("n" . nil)
     ("o" . nil)
     ("p" . nil)
     ("q" . nil)
     ("r" . nil)
     ("s" . nil)
     ("t" . nil)
     ("u" . nil)
     ("v" . nil)
     ("w" . nil)
     ("x" . nil)
     ("y" . nil)
     ("z" . nil)

     ("1" . nil)
     ("2" . nil)
     ("3" . nil)
     ("4" . nil)
     ("5" . nil)
     ("6" . nil)
     ("7" . nil)
     ("9" . nil)
     ("0" . nil)


     ("/" . nil)
     ("-" . nil)
     ("." . nil)
     ("," . nil)
     (";" . nil)
     ("'" . nil)
     ("[" . nil)
     ("]" . nil)
     ("\\" . nil)
     ("'" . nil)


     ("C-n" . next-line)
     ("C-s" . swiper-isearch)
     ("C-c i" . counsel-imenu)
     ("C-v" . scrollkeeper-contents-up)
     ("C-x c" . xah-fly-command-mode-activate)
     ("<f3>" . gtrun/hydra-org-starter/body)
     ("<f4>" . xah-fly-command-mode-activate)
     ("<f5>" . awesome-tab-ace-jump)
     ;; more
     ))
  )
```


## <span class="section-num">3</span> define-key xah-fly-keys-map(Command mode) {#define-key-xah-fly-keys-map--command-mode}

-   [xah-fly-keys/xah-fly-keys.el at master · xahlee/xah-fly-keys](https://github.com/xahlee/xah-fly-keys/blob/master/xah-fly-keys.el#L3392)
    -   [p-keymap](#p-keymap)

<!--listend-->

```emacs-lisp
(defun xah-fly-command-mode-init ()
  (interactive)
  (xah-fly--define-keys
   xah-fly-key-map
   '(
     ("SPC" . xah-fly-leader-key-map)

     ("a" . counsel-M-x)
     ("b" . backward-word)
     ("c" . xah-copy-line-or-region)
     ("d" . xah-beginning-of-line-or-block)
     ("e" . xah-end-of-line-or-block)
     ("f" . xah-fly-insert-mode-activate)

     ("g" . backward-word)
     ("h" . forward-word)

     ("i" . previous-line)
     ("j" . forward-char)
     ("k" . next-line)
     ("l" . backward-char)
     ("m" . isearch-backward)
     ("n" . isearch-forward)

     ("o" . xah-delete-current-text-block)
     ("p" . xah-fly-p-keymap)
     ("q" . quit-window)
     ("r" . xah-delete-backward-char-or-bracket-text)
     ("t" . set-mark-command)
     ("u" . undo-fu-only-redo)
     ("v" . xah-paste-or-paste-previous)
     ("w" . xah-next-window-or-frame)
     ("x" . xah-cut-line-or-region)
     ("y" . undo-fu-only-undo)
     ("z" . xah-goto-matching-bracket)



     ("[" . xah-backward-punct)
     ("]" . xah-forward-punct)
     (";" . Info-goto-emacs-command-node)

     ("1" . xah-extend-selection)
     ("2" . xah-select-line)
     ("3" . delete-other-windows)
     ("4" . split-window-below)
     ("5" . delete-char)
     ("6" . xah-select-block)
     ("7" . xah-select-line)
     ("8" . xah-extend-selection)
     ("9" . xah-select-text-in-quote)
     ("0" . xah-pop-local-mark-ring)


     ("C-a" . beginning-of-visual-line)

     ("M-'" . maple-iedit-match-all)

     ("<f3>" . gtrun/hydra-org-starter/body)
     ("<f4>" . xah-fly-command-mode-activate)
     ("<f4>" . xah-fly-command-mode-activate)
     ))
;; FIXEME: end line with under headlines
```


## <span class="section-num">4</span> specific keys in different mode map {#specific-keys-in-different-mode-map}


### <span class="section-num">4.1</span> load all of specific keys {#load-all-of-specific-keys}

```emacs-lisp
(define-key xah-fly-key-map (kbd ".") 'gtrun-xah-fly-keys-dot)
(define-key xah-fly-key-map (kbd "s-p") 'gtrun-xah-fly-keys-P)
(define-key xah-fly-key-map (kbd "-") 'gtrun-xah-fly-keys-minus)
(define-key xah-fly-key-map (kbd "/") 'gtrun-xah-fly-keys-slash)
(define-key xah-fly-key-map (kbd ",") 'gtrun-xah-fly-keys-comma)
```


### <span class="section-num">4.2</span> Only Linux keys {#only-linux-keys}

```emacs-lisp
(when (eq system-type 'gnu/linux)
  (define-key xah-fly-key-map (kbd "r") 'eaf-open)
  (define-key xah-fly-key-map (kbd "w") 'snails)
  )
;; end line to xah-fly-command-mode-init
)

(when (display-graphic-p)
 (define-key key-translation-map (kbd "ESC") (kbd "C-x c"))
)
```


### <span class="section-num">4.3</span> .-dot {#dot-dot}

```emacs-lisp
(defun gtrun-xah-fly-keys-dot ()
  "key `.'"
  (interactive)
  (cond
   ((eq major-mode 'org-mode) (call-interactively 'org-edit-src-code))
   ((eq major-mode 'org-tanglesync-mode) (call-interactively 'org-edit-src-code))
   ((eq major-mode 'elfeed-search-mode) (call-interactively 'scrollkeeper-contents-up))
   (t nil)))
```


### <span class="section-num">4.4</span> ,-comma {#comma}

```emacs-lisp
(defun gtrun-xah-fly-keys-comma ()
  "key `,'"
  (interactive)
  (cond
   ;; ((eq major-mode 'dired-mode) (call-interactively 'd))
   ((eq major-mode 'w3m-mode) (call-interactively 'scrollkeeper-contents-down))
   ((eq major-mode 'elfeed-show-mode) (call-interactively 'scrollkeeper-contents-down))
   ((eq major-mode 'elfeed-search-mode) (call-interactively 'scrollkeeper-contents-down))
   (t nil)))
```


### <span class="section-num">4.5</span> /-slash {#slash}

```emacs-lisp
(defun gtrun-xah-fly-keys-slash ()
  "key `/'"
  (interactive)
  (cond
   ;; ((eq major-mode 'dired-mode) (call-interactively 'd))
   ((eq major-mode 'dired-mode) (call-interactively 'vinegar/dired-diff))
   ((eq major-mode 'w3m-mode) (call-interactively 'w3m-bookmark-add-current-url))
   ((eq major-mode 'org-agenda-mode) (call-interactively 'org-agenda-filter-by-tag))
   ((eq major-mode 'elfeed-search-mode) (call-interactively 'elfeed-update))
   ((eq major-mode 'ess-julia-mode) (call-interactively 'julia-mode))
   (t nil)))
```


### <span class="section-num">4.6</span> ;-semicolon {#semicolon}

```emacs-lisp
(defun gtrun-xah-fly-keys-semicolon ()
  "key `;'"
  (interactive)
  (cond
   ;; ((eq major-mode 'dired-mode) (call-interactively 'd))

   (t nil)))
```


### <span class="section-num">4.7</span> '-apostrophe {#apostrophe}

```emacs-lisp
(defun gtrun-xah-fly-keys-apostrophe ()
  "key `''"
  (interactive)
  (cond
   ;; ((eq major-mode 'dired-mode) (call-interactively 'd))

   (t nil)))
```


### <span class="section-num">4.8</span> =-e {#e}

```emacs-lisp
(defun gtrun-xah-equality-fly-keys ()
  "key `='"
  (interactive)
  (cond
   ;; ((eq major-mode 'dired-mode) (call-interactively 'd))
   (t nil)))

```


### <span class="section-num">4.9</span> p-keymap {#p-keymap}

<span class="timestamp-wrapper"><span class="timestamp">[2020-09-23 Wed 03:14] </span></span> <- [define-key xah-fly-keys-map(Command mode)](#define-key-xah-fly-keys-map--command-mode)

```emacs-lisp
(xah-fly--define-keys
 (define-prefix-command 'xah-fly-p-keymap)
 '(
   ("," . xah-open-in-external-app)
   ("." . find-file)
   ("c" . bookmark-bmenu-list)
   ("e" . ibuffer)
   ("u" . xah-open-file-at-cursor)
   ("h" . recentf-open-files)
   ("i" . xah-copy-file-path)
   ("l" . bookmark-set)
   ("n" . xah-new-empty-buffer)
   ("o" . xah-show-in-desktop)
   ("p" . xah-open-last-closed)
   ("f" . xah-open-recently-closed)
   ("y" . xah-list-recently-closed)
   ("r" . xah-open-file-fast)
   ("s" . write-file)
   ))
```


### <span class="section-num">4.10</span> P-key {#p-key}

```emacs-lisp
(defun gtrun-xah-fly-keys-P ()
  "key `P'"
  (interactive)
  (cond
   ;; ((eq major-mode 'dired-mode) (call-interactively 'd))
   ((eq major-mode 'dired-mode) (call-interactively 'xah-show-in-desktop))
   (t nil)))
```


### <span class="section-num">4.11</span> &#x2013;minus {#and-x2013-minus}

```emacs-lisp
(defun gtrun-xah-minus-fly-keys ()
  "key `-'"
  (interactive)
  (cond
   ;; ((eq major-mode 'dired-mode) (call-interactively 'd))
   ((eq major-mode 'dired-mode) (call-interactively 'vinegar/up-directory))
   (t nil)))
```


### <span class="section-num">4.12</span> Color {#color}

```emacs-lisp
;; (defun my-highlight-line-on () (global-hl-line-mode 1))
;; (defun my-highlight-line-off () (global-hl-line-mode 0))

;; (add-hook! 'xah-fly-command-mode-activate-hook 'my-highlight-line-on)
;; (add-hook! 'xah-fly-insert-mode-activate-hook  'my-highlight-line-off)

;; (defun my-xfk-command-color () (set-background-color "DeepSkyBlue"))
;; (defun my-xfk-insert-color () (set-background-color "IndianRed"))

;; (add-hook! 'xah-fly-command-mode-activate-hook 'my-xfk-command-color)
;; (add-hook! 'xah-fly-insert-mode-activate-hook  'my-xfk-insert-color)
```


## <span class="section-num">5</span> define-key xah-fly-leader-key-map {#define-key-xah-fly-leader-key-map}

-   [magit-keys (leader-key to "m")](#magit-keys--leader-key-to-m)
-   [org-keys (leader-key to "o")](#org-keys--leader-key-to-o)
-   [search-keys (leader-key to "s")](#search-keys--leader-key-to-s)

<!--listend-->

```emacs-lisp
  (xah-fly--define-keys
   (define-prefix-command 'xah-fly-leader-key-map)
   '(
     ("m" . magit-keys)
     ("o" . org-keys)
     ("s" . search-keys)
     ;;timer
     ("ti" . insert-current-date-time-inactive)
     ("ta" . insert-current-date-time-active)
     ("tc" . insert-current-date-time)
     ;;find file
     ("fr" . counsel-recentf)
     ("fp" . doom/find-file-in-private-config)
     ("<tab>" . spacemacs/alternate-buffer)
     ("ff" . counsel-file-jump)
     ("RET" . helm-bookmarks)
     ;; treemacs
     ("tt" . +treemacs/toggle)
     ("tf" . +treemacs/find-file)
     ;; helm
     ("bb" . switch-to-buffer)
     ("bs" . bookmark-set)
     ("bm" . bookmark-bmenu-list)
     ("bt" . bm-toggle)
     ;; dired
     ("dw" . dired-other-window)
     ("df" . dired-other-frame)
))

```


## <span class="section-num">6</span> search-keys (leader-key to "s") {#search-keys--leader-key-to-s}

<span class="timestamp-wrapper"><span class="timestamp">[2020-09-23 Wed 03:25] </span></span> <- [define-key xah-fly-leader-key-map](#define-key-xah-fly-leader-key-map)

```emacs-lisp
  (xah-fly--define-keys
   ;; create a keymap my-keymap
   (define-prefix-command 'search-keys)
   '(
     ("a" . counsel-ag)
     ("r" . counsel-rg)
     ("y" . xah-search-current-word)
     ("m" . maple-iedit-match-next)
     ;;
     ))
```


## <span class="section-num">7</span> org-keys (leader-key to "o") {#org-keys--leader-key-to-o}

<span class="timestamp-wrapper"><span class="timestamp">[2020-09-23 Wed 03:24] </span></span> <- [define-key xah-fly-leader-key-map](#define-key-xah-fly-leader-key-map)

```emacs-lisp
  (xah-fly--define-keys
   ;; create a keymap org-keymap
   (define-prefix-command 'org-keys)
   '(
     ("i" . org-clock-in)
     ("o" . org-clock-out)
     ("a" . org-agenda)
     ))
```


## <span class="section-num">8</span> magit-keys (leader-key to "m") {#magit-keys--leader-key-to-m}

<span class="timestamp-wrapper"><span class="timestamp">[2020-09-23 Wed 03:22] </span></span> <- [define-key xah-fly-leader-key-map](#define-key-xah-fly-leader-key-map)

```emacs-lisp
  (xah-fly--define-keys
   ;; create a keymap org-keymap
   (define-prefix-command 'magit-keys)
   '(
     ("s" . magit)
     ))
```
