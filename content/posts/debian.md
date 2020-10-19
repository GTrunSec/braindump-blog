+++
title = "Debian Linux"
lastmod = 2020-10-11T19:39:49-07:00
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

- <span class="section-num">1</span> [timezone](#timezone)
    - <span class="section-num">1.1</span> [sync time with snapshot](#sync-time-with-snapshot)

</div>
<!--endtoc-->



## <span class="section-num">1</span> timezone {#timezone}


### <span class="section-num">1.1</span> sync time with snapshot {#sync-time-with-snapshot}

-   [sudo apt update error: "Release file is not yet valid" - Ask Ubuntu](https://askubuntu.com/questions/1096930/sudo-apt-update-error-release-file-is-not-yet-valid)

<!--listend-->

```sh
sudo hwclock --hctosys
```
