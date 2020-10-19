+++
title = "Nix"
lastmod = 2020-10-13T17:45:26-07:00
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

- <span class="section-num">1</span> [Documents](#documents)
    - <span class="section-num">1.1</span> [Welcome to nix.dev — nix.dev documentation](#welcome-to-nix-dot-dev-nix-dot-dev-documentation)
- <span class="section-num">2</span> [Learn materials](#learn-materials)
    - <span class="section-num">2.1</span> [Everything You Always Wanted To Know About Nix (But Were Afraid To Ask) - YouTube](#everything-you-always-wanted-to-know-about-nix--but-were-afraid-to-ask--youtube)
    - <span class="section-num">2.2</span> [Functional programming and Nix for reproducible, immutable infrastructure - YouTube](#functional-programming-and-nix-for-reproducible-immutable-infrastructure-youtube)
- <span class="section-num">3</span> [nixos](#nixos)
    - <span class="section-num">3.1</span> [Doc](#doc)
        - <span class="section-num">3.1.1</span> [Module - NixOS Wiki](#module-nixos-wiki)
        - <span class="section-num">3.1.2</span> [NixOS/hydra: Hydra, the Nix-based continuous build system](#nixos-hydra-hydra-the-nix-based-continuous-build-system)
        - <span class="section-num">3.1.3</span> [NixOS Planet](#nixos-planet)
    - <span class="section-num">3.2</span> [Users's config](#users-s-config)
        - <span class="section-num">3.2.1</span> [leotaku/nixos-config: A git repository to store my nix configurations in](#leotaku-nixos-config-a-git-repository-to-store-my-nix-configurations-in)
        - <span class="section-num">3.2.2</span> [babariviere/dotfiles: Personal dotfiles](#babariviere-dotfiles-personal-dotfiles):flakes:
        - <span class="section-num">3.2.3</span> [niveum/modules at master · kmein/niveum](#niveum-modules-at-master-kmein-niveum)
    - <span class="section-num">3.3</span> [other plantform](#other-plantform)
- <span class="section-num">4</span> [Long-term learning config](#long-term-learning-config):lib:
    - <span class="section-num">4.1</span> [nixos-config/modules at master · wiedzmin/nixos-config](#nixos-config-modules-at-master-wiedzmin-nixos-config)
    - <span class="section-num">4.2</span> [maxhbr/myconfig: my Linux Configuration](#maxhbr-myconfig-my-linux-configuration)
    - <span class="section-num">4.3</span> [nixos\_cfg/work.nix at master · evanjs/nixos\_cfg](#nixos-cfg-work-dot-nix-at-master-evanjs-nixos-cfg)
    - <span class="section-num">4.4</span> [coreyoconnor/nix\_configs: The NixOS configuration for my desktop.](#coreyoconnor-nix-configs-the-nixos-configuration-for-my-desktop-dot)
    - <span class="section-num">4.5</span> [<span class="org-todo todo TODO">TODO</span> jlesquembre/dotfiles: My dotfiles](#jlesquembre-dotfiles-my-dotfiles)
    - <span class="section-num">4.6</span> [nixos-config/programs at master · charvp/nixos-config](#nixos-config-programs-at-master-charvp-nixos-config)
    - <span class="section-num">4.7</span> [User](#user)
        - <span class="section-num">4.7.1</span> [zimbatm (zimbatm)](#zimbatm--zimbatm)
- <span class="section-num">5</span> [Nix Overlays](#nix-overlays)
    - <span class="section-num">5.1</span> [ROS on Nix](#ros-on-nix)
    - <span class="section-num">5.2</span> [Haskell](#haskell)
    - <span class="section-num">5.3</span> [Python Overlay](#python-overlay)
        - <span class="section-num">5.3.1</span> [How to override Python package (Anki)? - Learn - NixOS Discourse](#how-to-override-python-package--anki--learn-nixos-discourse)
- <span class="section-num">6</span> [Programming languages Environment](#programming-languages-environment)
    - <span class="section-num">6.1</span> [rust](#rust)
        - <span class="section-num">6.1.1</span> [nmattia/naersk: Build rust crates in Nix. No configuration, no code generation, no IFD. Sandbox friendly.](#nmattia-naersk-build-rust-crates-in-nix-dot-no-configuration-no-code-generation-no-ifd-dot-sandbox-friendly-dot)
    - <span class="section-num">6.2</span> [Hashell](#hashell)
        - <span class="section-num">6.2.1</span> [Haskell overlays](#haskell-overlays)
    - <span class="section-num">6.3</span> [python](#python)
        - <span class="section-num">6.3.1</span> [GitHub - DavHau/mach-nix: Tool to create highly reproducible python environments](#github-davhau-mach-nix-tool-to-create-highly-reproducible-python-environments)
- <span class="section-num">7</span> [configuration flakes](#configuration-flakes)
    - <span class="section-num">7.1</span> [nrdxp/nixflk: highly structured NixOS configuration database](#nrdxp-nixflk-highly-structured-nixos-configuration-database)
    - <span class="section-num">7.2</span> [nixrc/flake.nix at live · bqv/nixrc](#nixrc-flake-dot-nix-at-live-bqv-nixrc)
    - <span class="section-num">7.3</span> [abcdw/rde: My reproducible development environment](#abcdw-rde-my-reproducible-development-environment)
    - <span class="section-num">7.4</span> [LEXUGE/nixos: A fully automated replicable nixos configuration set](#lexuge-nixos-a-fully-automated-replicable-nixos-configuration-set)
    - <span class="section-num">7.5</span> [Ninlives/nixos-config: Bunch of Nix expressions for my working environment](#ninlives-nixos-config-bunch-of-nix-expressions-for-my-working-environment)
    - <span class="section-num">7.6</span> [dotfiles/flake.nix at master · berbiche/dotfiles](#dotfiles-flake-dot-nix-at-master-berbiche-dotfiles)
    - <span class="section-num">7.7</span> [nixos-conf/flake.nix at master · ImExtends/nixos-conf](#nixos-conf-flake-dot-nix-at-master-imextends-nixos-conf)
    - <span class="section-num">7.8</span> [nixcfg/flake.nix at template · l5r/nixcfg](#nixcfg-flake-dot-nix-at-template-l5r-nixcfg)
    - <span class="section-num">7.9</span> [nixos-config/flake.nix at nixus · cole-h/nixos-config](#nixos-config-flake-dot-nix-at-nixus-cole-h-nixos-config)
    - <span class="section-num">7.10</span> [https://github.com/Kloenk/nix/blob/master/flake.nix](#https-github-dot-com-kloenk-nix-blob-master-flake-dot-nix)
- <span class="section-num">8</span> [flakes](#flakes)
    - <span class="section-num">8.1</span> [Flakes wiki](#flakes-wiki)
        - <span class="section-num">8.1.1</span> [Output scheme](#output-scheme)
    - <span class="section-num">8.2</span> [Nix Flakes edition | $ zimbatm](#nix-flakes-edition-zimbatm)
    - <span class="section-num">8.3</span> [numtide/flake-utils: Pure Nix flake utility functions](#numtide-flake-utils-pure-nix-flake-utility-functions)
    - <span class="section-num">8.4</span> [hydra CI build packages](#hydra-ci-build-packages)
- <span class="section-num">9</span> [Networking](#networking)
    - <span class="section-num">9.1</span> [icebox-nix/netkit.nix: Verstile tools for advanced networking scenarios in NixOS](#icebox-nix-netkit-dot-nix-verstile-tools-for-advanced-networking-scenarios-in-nixos)
- <span class="section-num">10</span> [Security](#security)
    - <span class="section-num">10.1</span> [localhost/security.nix at master · jollheef/localhost](#localhost-security-dot-nix-at-master-jollheef-localhost)
- <span class="section-num">11</span> [home-manager](#home-manager)
    - <span class="section-num">11.1</span> [home-manager overlay](#home-manager-overlay)
    - <span class="section-num">11.2</span> [IsLinux or IsDarwin](#islinux-or-isdarwin)
- <span class="section-num">12</span> [Cachix](#cachix)
    - <span class="section-num">12.1</span> [push binary cache with nix-shell](#push-binary-cache-with-nix-shell)
    - <span class="section-num">12.2</span> [Pushing Flake inputs to Cachix](#pushing-flake-inputs-to-cachix)
- <span class="section-num">13</span> [nix expressions](#nix-expressions)
    - <span class="section-num">13.1</span> [zimbatm/nix-experiments](#zimbatm-nix-experiments)
    - <span class="section-num">13.2</span> [parser](#parser)
        - <span class="section-num">13.2.1</span> [orivej/go-nix: Nix language parser and Nix-compatible file hasher in Go](#orivej-go-nix-nix-language-parser-and-nix-compatible-file-hasher-in-go)
    - <span class="section-num">13.3</span> [<span class="org-todo done __IMPORTANT">✰ IMPORTANT</span> Nix Expression Language - NixOS Wiki](#nix-expression-language-nixos-wiki)
- <span class="section-num">14</span> [nix-hash](#nix-hash)
    - <span class="section-num">14.1</span> [jwiegley/nix-update-el: An Emacs command for updating fetch declarations in place](#jwiegley-nix-update-el-an-emacs-command-for-updating-fetch-declarations-in-place)
    - <span class="section-num">14.2</span> [numtide/rnix-hashes: Nix Hash Converter](#numtide-rnix-hashes-nix-hash-converter)
- <span class="section-num">15</span> [nix-env](#nix-env)
    - <span class="section-num">15.1</span> [target/lorri: Your project's nix-env](#target-lorri-your-project-s-nix-env)
- <span class="section-num">16</span> [Nix template](#nix-template)
    - <span class="section-num">16.1</span> [nix-dot-dev/getting-started-nix-template: Based on nix.dev tutorials, repository template to get you started with Nix.](#nix-dot-dev-getting-started-nix-template-based-on-nix-dot-dev-tutorials-repository-template-to-get-you-started-with-nix-dot)
- <span class="section-num">17</span> [Audio](#audio)
    - <span class="section-num">17.1</span> [zeus\_audio/flake.nix at master · lopsided98/zeus\_audio](#zeus-audio-flake-dot-nix-at-master-lopsided98-zeus-audio)

</div>
<!--endtoc-->

tags
: [My learning Programming languages]({{< relref "programming-languages" >}})


## <span class="section-num">1</span> Documents {#documents}


### <span class="section-num">1.1</span> [Welcome to nix.dev — nix.dev documentation](https://nix.dev/) {#welcome-to-nix-dot-dev-nix-dot-dev-documentation}


## <span class="section-num">2</span> Learn materials {#learn-materials}


### <span class="section-num">2.1</span> [Everything You Always Wanted To Know About Nix (But Were Afraid To Ask) - YouTube](https://www.youtube.com/watch?v=2mG0zM%5FwtYs) {#everything-you-always-wanted-to-know-about-nix--but-were-afraid-to-ask--youtube}


### <span class="section-num">2.2</span> [Functional programming and Nix for reproducible, immutable infrastructure - YouTube](https://www.youtube.com/watch?v=mKXLAbrKrno) {#functional-programming-and-nix-for-reproducible-immutable-infrastructure-youtube}


## <span class="section-num">3</span> nixos {#nixos}


### <span class="section-num">3.1</span> Doc {#doc}


#### <span class="section-num">3.1.1</span> [Module - NixOS Wiki](https://nixos.wiki/wiki/Module) {#module-nixos-wiki}


#### <span class="section-num">3.1.2</span> [NixOS/hydra: Hydra, the Nix-based continuous build system](https://github.com/NixOS/hydra) {#nixos-hydra-hydra-the-nix-based-continuous-build-system}


#### <span class="section-num">3.1.3</span> [NixOS Planet](https://planet.nixos.org/) {#nixos-planet}


### <span class="section-num">3.2</span> Users's config {#users-s-config}


#### <span class="section-num">3.2.1</span> [leotaku/nixos-config: A git repository to store my nix configurations in](https://github.com/leotaku/nixos-config) {#leotaku-nixos-config-a-git-repository-to-store-my-nix-configurations-in}


#### <span class="section-num">3.2.2</span> [babariviere/dotfiles: Personal dotfiles](https://github.com/babariviere/dotfiles) {#babariviere-dotfiles-personal-dotfiles}


#### <span class="section-num">3.2.3</span> [niveum/modules at master · kmein/niveum](https://github.com/kmein/niveum/tree/master/modules) {#niveum-modules-at-master-kmein-niveum}


### <span class="section-num">3.3</span> other plantform {#other-plantform}

-   [elitak/nixos-infect: [GPLv3+] install nixos over the existing OS in a DigitalOcean droplet (and others with minor modifications)](https://github.com/elitak/nixos-infect)


## <span class="section-num">4</span> Long-term learning config {#long-term-learning-config}


### <span class="section-num">4.1</span> [nixos-config/modules at master · wiedzmin/nixos-config](https://github.com/wiedzmin/nixos-config/tree/master/modules) {#nixos-config-modules-at-master-wiedzmin-nixos-config}


### <span class="section-num">4.2</span> [maxhbr/myconfig: my Linux Configuration](https://github.com/maxhbr/myconfig) {#maxhbr-myconfig-my-linux-configuration}


### <span class="section-num">4.3</span> [nixos\_cfg/work.nix at master · evanjs/nixos\_cfg](https://github.com/evanjs/nixos%5Fcfg/blob/master/modules/home-manager/randr/work.nix) {#nixos-cfg-work-dot-nix-at-master-evanjs-nixos-cfg}


### <span class="section-num">4.4</span> [coreyoconnor/nix\_configs: The NixOS configuration for my desktop.](https://github.com/coreyoconnor/nix%5Fconfigs/tree/master) {#coreyoconnor-nix-configs-the-nixos-configuration-for-my-desktop-dot}


### <span class="org-todo todo TODO">TODO</span> <span class="section-num">4.5</span> [jlesquembre/dotfiles: My dotfiles](https://github.com/jlesquembre/dotfiles/tree/master) {#jlesquembre-dotfiles-my-dotfiles}


### <span class="section-num">4.6</span> [nixos-config/programs at master · charvp/nixos-config](https://github.com/charvp/nixos-config/tree/master/programs) {#nixos-config-programs-at-master-charvp-nixos-config}


### <span class="section-num">4.7</span> User {#user}


#### <span class="section-num">4.7.1</span> [zimbatm (zimbatm)](https://github.com/zimbatm) {#zimbatm--zimbatm}


## <span class="section-num">5</span> Nix Overlays {#nix-overlays}

-   [home-manager overlay](#home-manager-overlay)


### <span class="section-num">5.1</span> ROS on Nix {#ros-on-nix}

-   [lopsided98/nix-ros-overlay: ROS overlay for the Nix package manager](robot.md)


### <span class="section-num">5.2</span> Haskell {#haskell}

-   [Haskell overlays](#haskell-overlays)


### <span class="section-num">5.3</span> Python Overlay {#python-overlay}

<span class="timestamp-wrapper"><span class="timestamp">[2020-10-11 Sun 02:02] </span></span> <- [python](#python)


#### <span class="section-num">5.3.1</span> [How to override Python package (Anki)? - Learn - NixOS Discourse](https://discourse.nixos.org/t/how-to-override-python-package-anki/8213) {#how-to-override-python-package--anki--learn-nixos-discourse}


## <span class="section-num">6</span> Programming languages Environment {#programming-languages-environment}


### <span class="section-num">6.1</span> rust {#rust}


#### <span class="section-num">6.1.1</span> [nmattia/naersk: Build rust crates in Nix. No configuration, no code generation, no IFD. Sandbox friendly.](https://github.com/nmattia/naersk) {#nmattia-naersk-build-rust-crates-in-nix-dot-no-configuration-no-code-generation-no-ifd-dot-sandbox-friendly-dot}

<span class="timestamp-wrapper"><span class="timestamp">[2020-09-22 Tue 18:58] </span></span> <- [nix](rust.md)


### <span class="section-num">6.2</span> Hashell {#hashell}


#### <span class="section-num">6.2.1</span> Haskell overlays {#haskell-overlays}

<span class="timestamp-wrapper"><span class="timestamp">[2020-10-06 Tue 19:52] </span></span> <- [Haskell](#haskell)

-   [nixpkgs/configuration-common.nix at master · NixOS/nixpkgs](https://github.com/NixOS/nixpkgs/blob/master/pkgs/development/haskell-modules/configuration-common.nix)


### <span class="section-num">6.3</span> python {#python}

-   [Python Overlay](#python-overlay)


#### <span class="section-num">6.3.1</span> [GitHub - DavHau/mach-nix: Tool to create highly reproducible python environments](https://github.com/DavHau/mach-nix) {#github-davhau-mach-nix-tool-to-create-highly-reproducible-python-environments}

```sh
nix-env -if https://github.com/DavHau/mach-nix/tarball/2.4.1 -A mach-nix
```


## <span class="section-num">7</span> configuration flakes {#configuration-flakes}


### <span class="section-num">7.1</span> [nrdxp/nixflk: highly structured NixOS configuration database](https://github.com/nrdxp/nixflk/) {#nrdxp-nixflk-highly-structured-nixos-configuration-database}


### <span class="section-num">7.2</span> [nixrc/flake.nix at live · bqv/nixrc](https://github.com/bqv/nixrc/blob/live/flake.nix) {#nixrc-flake-dot-nix-at-live-bqv-nixrc}


### <span class="section-num">7.3</span> [abcdw/rde: My reproducible development environment](https://github.com/abcdw/rde/) {#abcdw-rde-my-reproducible-development-environment}


### <span class="section-num">7.4</span> [LEXUGE/nixos: A fully automated replicable nixos configuration set](https://github.com/LEXUGE/nixos) {#lexuge-nixos-a-fully-automated-replicable-nixos-configuration-set}


### <span class="section-num">7.5</span> [Ninlives/nixos-config: Bunch of Nix expressions for my working environment](https://github.com/Ninlives/nixos-config) {#ninlives-nixos-config-bunch-of-nix-expressions-for-my-working-environment}


### <span class="section-num">7.6</span> [dotfiles/flake.nix at master · berbiche/dotfiles](https://github.com/berbiche/dotfiles/blob/master/flake.nix) {#dotfiles-flake-dot-nix-at-master-berbiche-dotfiles}


### <span class="section-num">7.7</span> [nixos-conf/flake.nix at master · ImExtends/nixos-conf](https://github.com/ImExtends/nixos-conf/blob/master/flake.nix) {#nixos-conf-flake-dot-nix-at-master-imextends-nixos-conf}


### <span class="section-num">7.8</span> [nixcfg/flake.nix at template · l5r/nixcfg](https://github.com/l5r/nixcfg/blob/template/flake.nix) {#nixcfg-flake-dot-nix-at-template-l5r-nixcfg}


### <span class="section-num">7.9</span> [nixos-config/flake.nix at nixus · cole-h/nixos-config](https://github.com/cole-h/nixos-config/blob/nixus/flake.nix) {#nixos-config-flake-dot-nix-at-nixus-cole-h-nixos-config}


### <span class="section-num">7.10</span> <https://github.com/Kloenk/nix/blob/master/flake.nix> {#https-github-dot-com-kloenk-nix-blob-master-flake-dot-nix}


## <span class="section-num">8</span> flakes {#flakes}

-   [Pushing Flake inputs to Cachix](#pushing-flake-inputs-to-cachix)


### <span class="section-num">8.1</span> Flakes wiki {#flakes-wiki}

-   [ ] [wiki] [Flakes - NixOS Wiki](https://nixos.wiki/wiki/Flakes)
-   [ ] [wiki] [nix-flakes.md](https://gist.github.com/edolstra/40da6e3a4d4ee8fd019395365e0772e7)
-   [ ] [] ~/.config/nix/nix.conf

    ```conf
      experimental-features = nix-command flakes
    ```


#### <span class="section-num">8.1.1</span> Output scheme {#output-scheme}

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
  templates."<attr>" = { path = "<store-path>"; description = "";
}
```


### <span class="section-num">8.2</span> [Nix Flakes edition | $ zimbatm](https://zimbatm.com/NixFlakes/#direnv-integration) {#nix-flakes-edition-zimbatm}

<span class="timestamp-wrapper"><span class="timestamp">[2020-10-01 Thu 23:35] </span></span> <- [Pushing Flake inputs to Cachix](#pushing-flake-inputs-to-cachix)


### <span class="section-num">8.3</span> [numtide/flake-utils: Pure Nix flake utility functions](https://github.com/numtide/flake-utils) {#numtide-flake-utils-pure-nix-flake-utility-functions}

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


### <span class="section-num">8.4</span> hydra CI build packages {#hydra-ci-build-packages}

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


## <span class="section-num">9</span> Networking {#networking}


### <span class="section-num">9.1</span> [icebox-nix/netkit.nix: Verstile tools for advanced networking scenarios in NixOS](https://github.com/icebox-nix/netkit.nix) {#icebox-nix-netkit-dot-nix-verstile-tools-for-advanced-networking-scenarios-in-nixos}


## <span class="section-num">10</span> Security {#security}


### <span class="section-num">10.1</span> [localhost/security.nix at master · jollheef/localhost](https://github.com/jollheef/localhost/blob/master/security.nix) {#localhost-security-dot-nix-at-master-jollheef-localhost}


## <span class="section-num">11</span> home-manager {#home-manager}

-   [Home Manager Manual](https://rycee.gitlab.io/home-manager/index.html#%5Fhow%5Fdo%5Fset%5Fup%5Fa%5Fconfiguration%5Ffor%5Fmultiple%5Fusers%5Fmachines)


### <span class="section-num">11.1</span> home-manager overlay {#home-manager-overlay}

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


### <span class="section-num">11.2</span> IsLinux or IsDarwin {#islinux-or-isdarwin}

-   [Infinite Recursion With stdenv functions · Issue #414 · nix-community/home-manager · GitHub](https://github.com/nix-community/home-manager/issues/414)


## <span class="section-num">12</span> Cachix {#cachix}


### <span class="section-num">12.1</span> push binary cache with nix-shell {#push-binary-cache-with-nix-shell}

```sh
nix-store --query --references $(nix-instantiate my-default.nix) | xargs nix-store --realise | xargs nix-store --query --requisites | cachix push nsm-data-analysis
```


### <span class="section-num">12.2</span> Pushing Flake inputs to Cachix {#pushing-flake-inputs-to-cachix}

<span class="timestamp-wrapper"><span class="timestamp">[2020-10-13 Tue 17:45] </span></span> <- [flakes](#flakes)

-   [Nix Flakes edition | $ zimbatm](#nix-flakes-edition-zimbatm)

<!--listend-->

```sh
nix flake archive --json \
  | jq -r '.path,(.inputs|to_entries[].value.path)' \
  | cachix push $cache_name
```

-   soultion

    ```sh
    nix path-info --json | jq -r '.[].path' | cachix push $cache_name
    ```

    -   nix develop

        ```sh
        nix develop --profile dev-profiile && cachix push mycache dev-profile

        ```


## <span class="section-num">13</span> nix expressions {#nix-expressions}


### <span class="section-num">13.1</span> [zimbatm/nix-experiments](https://github.com/zimbatm/nix-experiments) {#zimbatm-nix-experiments}


### <span class="section-num">13.2</span> parser {#parser}


#### <span class="section-num">13.2.1</span> [orivej/go-nix: Nix language parser and Nix-compatible file hasher in Go](https://github.com/orivej/go-nix) {#orivej-go-nix-nix-language-parser-and-nix-compatible-file-hasher-in-go}


### <span class="org-todo done __IMPORTANT">✰ IMPORTANT</span> <span class="section-num">13.3</span> [Nix Expression Language - NixOS Wiki](https://nixos.wiki/wiki/Nix%5FExpression%5FLanguage) {#nix-expression-language-nixos-wiki}


## <span class="section-num">14</span> nix-hash {#nix-hash}


### <span class="section-num">14.1</span> [jwiegley/nix-update-el: An Emacs command for updating fetch declarations in place](https://github.com/jwiegley/nix-update-el) {#jwiegley-nix-update-el-an-emacs-command-for-updating-fetch-declarations-in-place}


### <span class="section-num">14.2</span> [numtide/rnix-hashes: Nix Hash Converter](https://github.com/numtide/rnix-hashes) {#numtide-rnix-hashes-nix-hash-converter}


## <span class="section-num">15</span> nix-env {#nix-env}


### <span class="section-num">15.1</span> [target/lorri: Your project's nix-env](https://github.com/target/lorri) {#target-lorri-your-project-s-nix-env}


## <span class="section-num">16</span> Nix template {#nix-template}


### <span class="section-num">16.1</span> [nix-dot-dev/getting-started-nix-template: Based on nix.dev tutorials, repository template to get you started with Nix.](https://github.com/nix-dot-dev/getting-started-nix-template) {#nix-dot-dev-getting-started-nix-template-based-on-nix-dot-dev-tutorials-repository-template-to-get-you-started-with-nix-dot}


## <span class="section-num">17</span> Audio {#audio}


### <span class="section-num">17.1</span> [zeus\_audio/flake.nix at master · lopsided98/zeus\_audio](https://github.com/lopsided98/zeus%5Faudio/blob/master/flake.nix) {#zeus-audio-flake-dot-nix-at-master-lopsided98-zeus-audio}
