+++
title = "Nix"
lastmod = 2020-09-30T20:54:20-07:00
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
    - <span class="section-num">3.5</span> [<span class="org-todo todo TODO">TODO</span> jlesquembre/dotfiles: My dotfiles](#jlesquembre-dotfiles-my-dotfiles)
    - <span class="section-num">3.6</span> [nixos-config/programs at master · charvp/nixos-config](#nixos-config-programs-at-master-charvp-nixos-config)
    - <span class="section-num">3.7</span> [User](#user)
        - <span class="section-num">3.7.1</span> [zimbatm (zimbatm)](#zimbatm--zimbatm)
- <span class="section-num">4</span> [Nix Overlays](#nix-overlays)
    - <span class="section-num">4.1</span> [ROS on Nix](#ros-on-nix)
- <span class="section-num">5</span> [Programming languages Environment](#programming-languages-environment)
    - <span class="section-num">5.1</span> [rust](#rust)
        - <span class="section-num">5.1.1</span> [nmattia/naersk: Build rust crates in Nix. No configuration, no code generation, no IFD. Sandbox friendly.](#nmattia-naersk-build-rust-crates-in-nix-dot-no-configuration-no-code-generation-no-ifd-dot-sandbox-friendly-dot)
- <span class="section-num">6</span> [configuration flakes](#configuration-flakes)
    - <span class="section-num">6.1</span> [nrdxp/nixflk: highly structured NixOS configuration database](#nrdxp-nixflk-highly-structured-nixos-configuration-database)
    - <span class="section-num">6.2</span> [nixrc/flake.nix at live · bqv/nixrc](#nixrc-flake-dot-nix-at-live-bqv-nixrc)
    - <span class="section-num">6.3</span> [abcdw/rde: My reproducible development environment](#abcdw-rde-my-reproducible-development-environment)
    - <span class="section-num">6.4</span> [LEXUGE/nixos: A fully automated replicable nixos configuration set](#lexuge-nixos-a-fully-automated-replicable-nixos-configuration-set)
    - <span class="section-num">6.5</span> [Ninlives/nixos-config: Bunch of Nix expressions for my working environment](#ninlives-nixos-config-bunch-of-nix-expressions-for-my-working-environment)
- <span class="section-num">7</span> [flakes lib](#flakes-lib)
    - <span class="section-num">7.1</span> [numtide/flake-utils: Pure Nix flake utility functions](#numtide-flake-utils-pure-nix-flake-utility-functions)
- <span class="section-num">8</span> [Networking](#networking)
    - <span class="section-num">8.1</span> [icebox-nix/netkit.nix: Verstile tools for advanced networking scenarios in NixOS](#icebox-nix-netkit-dot-nix-verstile-tools-for-advanced-networking-scenarios-in-nixos)
- <span class="section-num">9</span> [Security](#security)
    - <span class="section-num">9.1</span> [localhost/security.nix at master · jollheef/localhost](#localhost-security-dot-nix-at-master-jollheef-localhost)
- <span class="section-num">10</span> [home-manager](#home-manager)
    - <span class="section-num">10.1</span> [home-manager overlay](#home-manager-overlay)

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


### <span class="org-todo todo TODO">TODO</span> <span class="section-num">3.5</span> [jlesquembre/dotfiles: My dotfiles](https://github.com/jlesquembre/dotfiles/tree/master) {#jlesquembre-dotfiles-my-dotfiles}


### <span class="section-num">3.6</span> [nixos-config/programs at master · charvp/nixos-config](https://github.com/charvp/nixos-config/tree/master/programs) {#nixos-config-programs-at-master-charvp-nixos-config}


### <span class="section-num">3.7</span> User {#user}


#### <span class="section-num">3.7.1</span> [zimbatm (zimbatm)](https://github.com/zimbatm) {#zimbatm--zimbatm}


## <span class="section-num">4</span> Nix Overlays {#nix-overlays}

-   [home-manager overlay](#home-manager-overlay)


### <span class="section-num">4.1</span> ROS on Nix {#ros-on-nix}

-   [lopsided98/nix-ros-overlay: ROS overlay for the Nix package manager](robot.md)


## <span class="section-num">5</span> Programming languages Environment {#programming-languages-environment}


### <span class="section-num">5.1</span> rust {#rust}


#### <span class="section-num">5.1.1</span> [nmattia/naersk: Build rust crates in Nix. No configuration, no code generation, no IFD. Sandbox friendly.](https://github.com/nmattia/naersk) {#nmattia-naersk-build-rust-crates-in-nix-dot-no-configuration-no-code-generation-no-ifd-dot-sandbox-friendly-dot}

<span class="timestamp-wrapper"><span class="timestamp">[2020-09-22 Tue 18:58] </span></span> <- [nix](rust.md)


## <span class="section-num">6</span> configuration flakes {#configuration-flakes}


### <span class="section-num">6.1</span> [nrdxp/nixflk: highly structured NixOS configuration database](https://github.com/nrdxp/nixflk/) {#nrdxp-nixflk-highly-structured-nixos-configuration-database}


### <span class="section-num">6.2</span> [nixrc/flake.nix at live · bqv/nixrc](https://github.com/bqv/nixrc/blob/live/flake.nix) {#nixrc-flake-dot-nix-at-live-bqv-nixrc}


### <span class="section-num">6.3</span> [abcdw/rde: My reproducible development environment](https://github.com/abcdw/rde/) {#abcdw-rde-my-reproducible-development-environment}


### <span class="section-num">6.4</span> [LEXUGE/nixos: A fully automated replicable nixos configuration set](https://github.com/LEXUGE/nixos) {#lexuge-nixos-a-fully-automated-replicable-nixos-configuration-set}


### <span class="section-num">6.5</span> [Ninlives/nixos-config: Bunch of Nix expressions for my working environment](https://github.com/Ninlives/nixos-config) {#ninlives-nixos-config-bunch-of-nix-expressions-for-my-working-environment}


## <span class="section-num">7</span> flakes lib {#flakes-lib}

-   [ ] [wiki] [Flakes - NixOS Wiki](https://nixos.wiki/wiki/Flakes)


### <span class="section-num">7.1</span> [numtide/flake-utils: Pure Nix flake utility functions](https://github.com/numtide/flake-utils) {#numtide-flake-utils-pure-nix-flake-utility-functions}


## <span class="section-num">8</span> Networking {#networking}


### <span class="section-num">8.1</span> [icebox-nix/netkit.nix: Verstile tools for advanced networking scenarios in NixOS](https://github.com/icebox-nix/netkit.nix) {#icebox-nix-netkit-dot-nix-verstile-tools-for-advanced-networking-scenarios-in-nixos}


## <span class="section-num">9</span> Security {#security}


### <span class="section-num">9.1</span> [localhost/security.nix at master · jollheef/localhost](https://github.com/jollheef/localhost/blob/master/security.nix) {#localhost-security-dot-nix-at-master-jollheef-localhost}


## <span class="section-num">10</span> home-manager {#home-manager}


### <span class="section-num">10.1</span> home-manager overlay {#home-manager-overlay}

<span class="timestamp-wrapper"><span class="timestamp">[2020-09-30 Wed 20:54] </span></span> <- [Nix Overlays](#nix-overlays)

-   [Using an overlay in home-manager - Learn - NixOS Discourse](https://discourse.nixos.org/t/using-an-overlay-in-home-manager/6302)

    ```nix
    { config, pkgs, ... }:

    let
      pkgsUnstable = import <unstable> {};
    in

    {
      nixpkgs.overlays = [
        (final: previous: {
          skim = pkgsUnstable.skim;
        })
      ];

      programs.home-manager.enable = true;
      programs.skim.enable = true;
    }
    ```
