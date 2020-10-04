+++
title = "Nix"
lastmod = 2020-10-03T23:56:27-07:00
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
    - <span class="section-num">6.6</span> [dotfiles/flake.nix at master · berbiche/dotfiles](#dotfiles-flake-dot-nix-at-master-berbiche-dotfiles)
    - <span class="section-num">6.7</span> [nixos-conf/flake.nix at master · ImExtends/nixos-conf](#nixos-conf-flake-dot-nix-at-master-imextends-nixos-conf)
    - <span class="section-num">6.8</span> [nixcfg/flake.nix at template · l5r/nixcfg](#nixcfg-flake-dot-nix-at-template-l5r-nixcfg)
    - <span class="section-num">6.9</span> [nixos-config/flake.nix at nixus · cole-h/nixos-config](#nixos-config-flake-dot-nix-at-nixus-cole-h-nixos-config)
- <span class="section-num">7</span> [flakes](#flakes)
    - <span class="section-num">7.1</span> [Nix Flakes edition | $ zimbatm](#nix-flakes-edition-zimbatm)
    - <span class="section-num">7.2</span> [numtide/flake-utils: Pure Nix flake utility functions](#numtide-flake-utils-pure-nix-flake-utility-functions)
    - <span class="section-num">7.3</span> [hydra CI build packages](#hydra-ci-build-packages)
- <span class="section-num">8</span> [Networking](#networking)
    - <span class="section-num">8.1</span> [icebox-nix/netkit.nix: Verstile tools for advanced networking scenarios in NixOS](#icebox-nix-netkit-dot-nix-verstile-tools-for-advanced-networking-scenarios-in-nixos)
- <span class="section-num">9</span> [Security](#security)
    - <span class="section-num">9.1</span> [localhost/security.nix at master · jollheef/localhost](#localhost-security-dot-nix-at-master-jollheef-localhost)
- <span class="section-num">10</span> [home-manager](#home-manager)
    - <span class="section-num">10.1</span> [home-manager overlay](#home-manager-overlay)
- <span class="section-num">11</span> [Cachix](#cachix)
    - <span class="section-num">11.1</span> [push binary cache with nix-shell](#push-binary-cache-with-nix-shell)
    - <span class="section-num">11.2</span> [Pushing Flake inputs to Cachix](#pushing-flake-inputs-to-cachix)
- <span class="section-num">12</span> [nix expressions](#nix-expressions)
    - <span class="section-num">12.1</span> [zimbatm/nix-experiments](#zimbatm-nix-experiments)
    - <span class="section-num">12.2</span> [parser](#parser)
        - <span class="section-num">12.2.1</span> [orivej/go-nix: Nix language parser and Nix-compatible file hasher in Go](#orivej-go-nix-nix-language-parser-and-nix-compatible-file-hasher-in-go)
- <span class="section-num">13</span> [nix-hash](#nix-hash)
    - <span class="section-num">13.1</span> [jwiegley/nix-update-el: An Emacs command for updating fetch declarations in place](#jwiegley-nix-update-el-an-emacs-command-for-updating-fetch-declarations-in-place)

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


### <span class="section-num">6.6</span> [dotfiles/flake.nix at master · berbiche/dotfiles](https://github.com/berbiche/dotfiles/blob/master/flake.nix) {#dotfiles-flake-dot-nix-at-master-berbiche-dotfiles}


### <span class="section-num">6.7</span> [nixos-conf/flake.nix at master · ImExtends/nixos-conf](https://github.com/ImExtends/nixos-conf/blob/master/flake.nix) {#nixos-conf-flake-dot-nix-at-master-imextends-nixos-conf}


### <span class="section-num">6.8</span> [nixcfg/flake.nix at template · l5r/nixcfg](https://github.com/l5r/nixcfg/blob/template/flake.nix) {#nixcfg-flake-dot-nix-at-template-l5r-nixcfg}


### <span class="section-num">6.9</span> [nixos-config/flake.nix at nixus · cole-h/nixos-config](https://github.com/cole-h/nixos-config/blob/nixus/flake.nix) {#nixos-config-flake-dot-nix-at-nixus-cole-h-nixos-config}


## <span class="section-num">7</span> flakes {#flakes}

-   [ ] [wiki] [Flakes - NixOS Wiki](https://nixos.wiki/wiki/Flakes)
-   [ ] [wiki] [nix-flakes.md](https://gist.github.com/edolstra/40da6e3a4d4ee8fd019395365e0772e7)
-   Output scheme

    ```nix
    { self, ... }@inputs:
    {
      # This will be shown in `nix flake info`
      description = "A description what his flake provides";
      # Executed by `nix flake check`
      checks."<system>"."<attr>" = derivation;
      # Executed by `nix build .#<name>`
      packages."<system>"."<attr>" = derivation;
      # Executed by `nix build .`
      defaultPackage."<system>" = derivation;
      # Executed by `nix run .#<name>`
      apps."<system>"."<attr>" = {
        type = "app";
        program = "<store-path>";
      };
      # Executed by `nix run . -- <args?>`
      defaultApp."<system>" = { type = "app"; program = "..."; };

      # Used for nixpkgs packages, also accessible via `nix build .#<name>`
      legacyPackages."<system>"."<attr>" = derivation;
      # Default overlay, for use in dependent flakes
      overlay = final: prev: { };
      # Same idea as overlay but a list or attrset of them.
      overlays = {};
      # Default module, for use in dependent flakes
      nixosModule = { config }: { options = {}; config = {}; };
      # Same idea as nixosModule but a list or attrset of them.
      nixosModules = {};
      # Attrset of nixos configurations by hostname.
      nixosConfigurations."<hostname>" = {};
      hydraJobs."<attr>"."<system>" = derivation;
      # Used by `nix flake init -t <flake>`
      defaultTemplate = {
        path = "<store-path>";
        description = "template description goes here?";
      };
      # Used by `nix flake init -t <flake>#<attr>`
      templates."<attr>" = { path = "<store-path>"; description = ""; );
    }
    ```


### <span class="section-num">7.1</span> [Nix Flakes edition | $ zimbatm](https://zimbatm.com/NixFlakes/#direnv-integration) {#nix-flakes-edition-zimbatm}

<span class="timestamp-wrapper"><span class="timestamp">[2020-10-01 Thu 23:35] </span></span> <- [Pushing Flake inputs to Cachix](#pushing-flake-inputs-to-cachix)


### <span class="section-num">7.2</span> [numtide/flake-utils: Pure Nix flake utility functions](https://github.com/numtide/flake-utils) {#numtide-flake-utils-pure-nix-flake-utility-functions}

-   [flake-utils/flake.nix at master · numtide/flake-utils](https://github.com/numtide/flake-utils/blob/master/examples/each-system/flake.nix)
    -   eachDefaultSystem

        ```nix

          {
            description = "Flake utils demo";

            inputs.flake-utils.url = "github:numtide/flake-utils";

            outputs = { self, nixpkgs, flake-utils }:
              flake-utils.lib.eachDefaultSystem (system:
                let pkgs = nixpkgs.legacyPackages.${system}; in
                rec {
                  packages = flake-utils.lib.flattenTree {
                    hello = pkgs.hello;
                    gitAndTools = pkgs.gitAndTools;
                  };
                  defaultPackage = packages.hello;
                  apps.hello = flake-utils.lib.mkApp { drv = packages.hello; };
                  defaultApp = apps.hello;
                }
              );
          }
        ```

    -   simple-flake

        ```nix

        ```
-   [zimbatm/flake-static at 0cf37e62aae157409342a85f5f499f216bdcd2fe](https://github.com/zimbatm/flake-static/tree/0cf37e62aae157409342a85f5f499f216bdcd2fe)
    -   nixpkgs lib

        ```sh

        let
          importJSON = file: builtins.fromJSON (builtins.readFile file);
          flakeLock = importJSON ./flake.lock;
          loadInput = { locked, ... }:
            assert locked.type == "github";
            builtins.fetchTarball {
              url = "https://github.com/${locked.owner}/${locked.repo}/archive/${locked.rev}.tar.gz";
              sha256 = locked.narHash;
            };
          nixpkgs = loadInput flakeLock.nodes.nixpkgs;
        in
        import nixpkgs {
          config = { };
          overlays = [ ];
        }

        ```


### <span class="section-num">7.3</span> hydra CI build packages {#hydra-ci-build-packages}

-   [dhdm/flake.nix at master · edolstra/dhdm](https://github.com/edolstra/dhdm/blob/master/flake.nix)

<!--listend-->

```nix
{
  inputs.nixpkgs.url = "nixpkgs/nixos-20.03";

  outputs = { self, nixpkgs }: {

    defaultPackage.x86_64-linux =
      with import nixpkgs { system = "x86_64-linux"; };
      stdenv.mkDerivation {
        name = "dhdm";
        buildInputs = [ mesa_glu glew glfw libpng glm fmt nlohmann_json opensubdiv boost ];
        src = self;
        preBuild = "cd src";
        installPhase = "mkdir -p $out/bin; cp dhdm $out/bin/";
        enableParallelBuilding = true;
      };

    checks.x86_64-linux.build = self.defaultPackage.x86_64-linux;

  };

}
```


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


## <span class="section-num">11</span> Cachix {#cachix}


### <span class="section-num">11.1</span> push binary cache with nix-shell {#push-binary-cache-with-nix-shell}

```sh
nix-store --query --references $(nix-instantiate my-default.nix) | xargs nix-store --realise | xargs nix-store --query --requisites | cachix push nsm-data-analysis
```


### <span class="section-num">11.2</span> Pushing Flake inputs to Cachix {#pushing-flake-inputs-to-cachix}

-   [Nix Flakes edition | $ zimbatm](#nix-flakes-edition-zimbatm)

<!--listend-->

```sh
nix flake archive --json \
  | jq -r '.path,(.inputs|to_entries[].value.path)' \
  | cachix push $cache_name
```


## <span class="section-num">12</span> nix expressions {#nix-expressions}


### <span class="section-num">12.1</span> [zimbatm/nix-experiments](https://github.com/zimbatm/nix-experiments) {#zimbatm-nix-experiments}


### <span class="section-num">12.2</span> parser {#parser}


#### <span class="section-num">12.2.1</span> [orivej/go-nix: Nix language parser and Nix-compatible file hasher in Go](https://github.com/orivej/go-nix) {#orivej-go-nix-nix-language-parser-and-nix-compatible-file-hasher-in-go}


## <span class="section-num">13</span> nix-hash {#nix-hash}


### <span class="section-num">13.1</span> [jwiegley/nix-update-el: An Emacs command for updating fetch declarations in place](https://github.com/jwiegley/nix-update-el) {#jwiegley-nix-update-el-an-emacs-command-for-updating-fetch-declarations-in-place}
