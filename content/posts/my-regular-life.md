+++
title = "My Regular life"
lastmod = 2020-11-21T03:20:39-08:00
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

- <span class="section-num">1</span> [wasting my clothes <code>[0/3]</code>](#wasting-my-clothes)

</div>
<!--endtoc-->

tags
: [life hacker]({{< relref "life-hack" >}})


## <span class="section-num">1</span> wasting my clothes <code>[0/3]</code> {#wasting-my-clothes}

<!--list-separator-->

1. <span class="org-todo todo TODO">TODO</span>  Put clothes washer

    <p><span class="timestamp-wrapper"><span class="timestamp-kwd">SCHEDULED:</span> <span class="timestamp">&lt;2020-09-20 Sun 20:00 +1w&gt;</span></span></p>

        TRIGGER: next-sibling scheduled!("++1h")

        WILD_NOTIFIER_NOTIFY_BEFORE: 2

<!--list-separator-->

2. <span class="org-todo todo TODO">TODO</span>  Put clothes in dryer

        TRIGGER: next-sibling scheduled!("++1h")

        BLOCKER: previous-sibling

        WILD_NOTIFIER_NOTIFY_BEFORE: 2

<!--list-separator-->

3. <span class="org-todo todo TODO">TODO</span>  Put clothes away

        TRIGGER: next-sibling scheduled!("++1M")

        WILD_NOTIFIER_NOTIFY_BEFORE: 2

    ```emacs-lisp
    (require 'alert)

    ;; This is the most basic form usage
    (alert "This is an alert")

    ```
