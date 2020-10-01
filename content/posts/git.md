+++
title = "Git"
lastmod = 2020-09-30T20:48:25-07:00
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

- <span class="section-num">1</span> [git CONTRIBUTING](#git-contributing)

</div>
<!--endtoc-->



## <span class="section-num">1</span> git CONTRIBUTING {#git-contributing}

-   [python38Packages.coloredlogs: disable tests on darwin by tobim · Pull Request #96037 · NixOS/nixpkgs](https://github.com/NixOS/nixpkgs/pull/96037)

    ```sh
    git reset HEAD~1                    # move fix-up commits into unstaged
    git add -- pkgs/                    # move changes into staged
    git commit --amend --no-edit        # add changes to previous commit
    git push ... ... --force            # modify current PR branch

    ```
