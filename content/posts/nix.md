+++
title = "Nix"
lastmod = 2020-09-19T20:10:18-07:00
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

- <span class="section-num">1</span> [Learn materials](#learn-materials)
    - <span class="section-num">1.1</span> [Everything You Always Wanted To Know About Nix (But Were Afraid To Ask) - YouTube](#everything-you-always-wanted-to-know-about-nix--but-were-afraid-to-ask--youtube)
    - <span class="section-num">1.2</span> [Functional programming and Nix for reproducible, immutable infrastructure - YouTube](#functional-programming-and-nix-for-reproducible-immutable-infrastructure-youtube)
- <span class="section-num">2</span> [nixos](#nixos)
    - <span class="section-num">2.1</span> [Doc](#doc)
        - <span class="section-num">2.1.1</span> [Module - NixOS Wiki](#module-nixos-wiki)
        - <span class="section-num">2.1.2</span> [NixOS/hydra: Hydra, the Nix-based continuous build system](#nixos-hydra-hydra-the-nix-based-continuous-build-system)
        - <span class="section-num">2.1.3</span> [NixOS Planet](#nixos-planet)
    - <span class="section-num">2.2</span> [Users's config](#users-s-config)
        - <span class="section-num">2.2.1</span> [leotaku/nixos-config: A git repository to store my nix configurations in](#leotaku-nixos-config-a-git-repository-to-store-my-nix-configurations-in)
        - <span class="section-num">2.2.2</span> [babariviere/dotfiles: Personal dotfiles](#babariviere-dotfiles-personal-dotfiles):flakes:
        - <span class="section-num">2.2.3</span> [niveum/modules at master · kmein/niveum](#niveum-modules-at-master-kmein-niveum)
    - <span class="section-num">2.3</span> [other plantform](#other-plantform)
- <span class="section-num">3</span> [Long-term learning config](#long-term-learning-config):lib:
    - <span class="section-num">3.1</span> [nixos-config/modules at master · wiedzmin/nixos-config](#nixos-config-modules-at-master-wiedzmin-nixos-config)
    - <span class="section-num">3.2</span> [maxhbr/myconfig: my Linux Configuration](#maxhbr-myconfig-my-linux-configuration)
    - <span class="section-num">3.3</span> [nixos\_cfg/work.nix at master · evanjs/nixos\_cfg](#nixos-cfg-work-dot-nix-at-master-evanjs-nixos-cfg)
    - <span class="section-num">3.4</span> [coreyoconnor/nix\_configs: The NixOS configuration for my desktop.](#coreyoconnor-nix-configs-the-nixos-configuration-for-my-desktop-dot)
    - <span class="section-num">3.5</span> [<span class="org-todo todo __TODO">☞ TODO</span> jlesquembre/dotfiles: My dotfiles](#jlesquembre-dotfiles-my-dotfiles)
    - <span class="section-num">3.6</span> [nixos-config/programs at master · charvp/nixos-config](#nixos-config-programs-at-master-charvp-nixos-config)
        - <span class="section-num">3.6.1</span> [<span class="org-todo done __DONE">✔ DONE</span> f..](#f-dot-dot)
    - <span class="section-num">3.7</span> [User](#user)
        - <span class="section-num">3.7.1</span> [zimbatm (zimbatm)](#zimbatm--zimbatm)

</div>
<!--endtoc-->



## <span class="section-num">1</span> Learn materials {#learn-materials}


### <span class="section-num">1.1</span> [Everything You Always Wanted To Know About Nix (But Were Afraid To Ask) - YouTube](https://www.youtube.com/watch?v=2mG0zM%5FwtYs) {#everything-you-always-wanted-to-know-about-nix--but-were-afraid-to-ask--youtube}


### <span class="section-num">1.2</span> [Functional programming and Nix for reproducible, immutable infrastructure - YouTube](https://www.youtube.com/watch?v=mKXLAbrKrno) {#functional-programming-and-nix-for-reproducible-immutable-infrastructure-youtube}


## <span class="section-num">2</span> nixos {#nixos}


### <span class="section-num">2.1</span> Doc {#doc}


#### <span class="section-num">2.1.1</span> [Module - NixOS Wiki](https://nixos.wiki/wiki/Module) {#module-nixos-wiki}


#### <span class="section-num">2.1.2</span> [NixOS/hydra: Hydra, the Nix-based continuous build system](https://github.com/NixOS/hydra) {#nixos-hydra-hydra-the-nix-based-continuous-build-system}


#### <span class="section-num">2.1.3</span> [NixOS Planet](https://planet.nixos.org/) {#nixos-planet}


### <span class="section-num">2.2</span> Users's config {#users-s-config}


#### <span class="section-num">2.2.1</span> [leotaku/nixos-config: A git repository to store my nix configurations in](https://github.com/leotaku/nixos-config) {#leotaku-nixos-config-a-git-repository-to-store-my-nix-configurations-in}


#### <span class="section-num">2.2.2</span> [babariviere/dotfiles: Personal dotfiles](https://github.com/babariviere/dotfiles) {#babariviere-dotfiles-personal-dotfiles}


#### <span class="section-num">2.2.3</span> [niveum/modules at master · kmein/niveum](https://github.com/kmein/niveum/tree/master/modules) {#niveum-modules-at-master-kmein-niveum}


### <span class="section-num">2.3</span> other plantform {#other-plantform}

-   [elitak/nixos-infect: [GPLv3+] install nixos over the existing OS in a DigitalOcean droplet (and others with minor modifications)](https://github.com/elitak/nixos-infect)


## <span class="section-num">3</span> Long-term learning config {#long-term-learning-config}


### <span class="section-num">3.1</span> [nixos-config/modules at master · wiedzmin/nixos-config](https://github.com/wiedzmin/nixos-config/tree/master/modules) {#nixos-config-modules-at-master-wiedzmin-nixos-config}


### <span class="section-num">3.2</span> [maxhbr/myconfig: my Linux Configuration](https://github.com/maxhbr/myconfig) {#maxhbr-myconfig-my-linux-configuration}


### <span class="section-num">3.3</span> [nixos\_cfg/work.nix at master · evanjs/nixos\_cfg](https://github.com/evanjs/nixos%5Fcfg/blob/master/modules/home-manager/randr/work.nix) {#nixos-cfg-work-dot-nix-at-master-evanjs-nixos-cfg}


### <span class="section-num">3.4</span> [coreyoconnor/nix\_configs: The NixOS configuration for my desktop.](https://github.com/coreyoconnor/nix%5Fconfigs/tree/master) {#coreyoconnor-nix-configs-the-nixos-configuration-for-my-desktop-dot}


### <span class="org-todo todo __TODO">☞ TODO</span> <span class="section-num">3.5</span> [jlesquembre/dotfiles: My dotfiles](https://github.com/jlesquembre/dotfiles/tree/master) {#jlesquembre-dotfiles-my-dotfiles}


### <span class="section-num">3.6</span> [nixos-config/programs at master · charvp/nixos-config](https://github.com/charvp/nixos-config/tree/master/programs) {#nixos-config-programs-at-master-charvp-nixos-config}


#### <span class="org-todo done __DONE">✔ DONE</span> <span class="section-num">3.6.1</span> f.. {#f-dot-dot}


### <span class="section-num">3.7</span> User {#user}


#### <span class="section-num">3.7.1</span> [zimbatm (zimbatm)](https://github.com/zimbatm) {#zimbatm--zimbatm}
