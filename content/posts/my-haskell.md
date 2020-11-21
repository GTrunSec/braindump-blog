+++
title = "My Haskell"
lastmod = 2020-11-21T03:08:29-08:00
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

- <span class="section-num">1</span> [Haskell (programming language)](#haskell--programming-language)
- <span class="section-num">2</span> [Haskell books](#haskell-books)
- <span class="section-num">3</span> [Haskell tutorial](#haskell-tutorial)
    - <span class="section-num">3.1</span> [kowainik/learn4haskell: 👩‍🏫 👨‍🏫 Learn Haskell basics in 4 pull requests](#kowainik-learn4haskell-learn-haskell-basics-in-4-pull-requests)
    - <span class="section-num">3.2</span> [Haskell video](#haskell-video)
        - <span class="section-num">3.2.1</span> [“Haskell for Imperative Programmers #1 - Basics - YouTube”🔊](#haskell-for-imperative-programmers-1-basics-youtube)
        - <span class="section-num">3.2.2</span> [Tsoding - YouTube](#tsoding-youtube)
    - <span class="section-num">3.3</span> [learning Haskell](#learning-haskell)
        - <span class="section-num">3.3.1</span> [kowainik/learn4haskell: 👩‍🏫 👨‍🏫 Learn Haskell basics in 4 pull requests](#kowainik-learn4haskell-learn-haskell-basics-in-4-pull-requests)
        - <span class="section-num">3.3.2</span> [learning-haskell/SExpr.hs at master · stolyaroleh/learning-haskell](#learning-haskell-sexpr-dot-hs-at-master-stolyaroleh-learning-haskell)
        - <span class="section-num">3.3.3</span> [tonymorris/fp-course: Functional Programming Course](#tonymorris-fp-course-functional-programming-course)
        - <span class="section-num">3.3.4</span> [Anton-Latukha/Haskell-Programming-From-First-Principles-exercises: Consists of QUALITY BELABORING of EVERY EXERCISE in the chapters {1-18,26} (~1400 pages) of the "Haskell book" ("Haskell Programming from First Principles"). With literate comments. Additionally notable for use of Nix for exercise projects.](#anton-latukha-haskell-programming-from-first-principles-exercises-consists-of-quality-belaboring-of-every-exercise-in-the-chapters-1-18-26--1400-pages--of-the-haskell-book--haskell-programming-from-first-principles--dot-with-literate-comments-dot-additionally-notable-for-use-of-nix-for-exercise-projects-dot)
- <span class="section-num">4</span> [Haskell Repositories](#haskell-repositories)
    - <span class="section-num">4.1</span> [obsidiansystems/solana-bridges](#obsidiansystems-solana-bridges)
    - <span class="section-num">4.2</span> [GitHub - AJChapman/co-log-polysemy-formatting: A Haskell library: A fancy logging effect for Polysemy using the formatting library to format log messages.](#github-ajchapman-co-log-polysemy-formatting-a-haskell-library-a-fancy-logging-effect-for-polysemy-using-the-formatting-library-to-format-log-messages-dot):logging:
- <span class="section-num">5</span> [Haskell user](#haskell-user)
    - <span class="section-num">5.1</span> [idontgetoutmuch / Repositories](#idontgetoutmuch-repositories):nix:
- <span class="section-num">6</span> [Haskell llvm](#haskell-llvm)
    - <span class="section-num">6.1</span> [llvm-hs Kaleidoscope Tutorial](#llvm-hs-kaleidoscope-tutorial)
- <span class="section-num">7</span> [Haskell lib](#haskell-lib)
    - <span class="section-num">7.1</span> [IO lib](#io-lib)
        - <span class="section-num">7.1.1</span> [haskell-Z/z-io: IO lib for haskell](#haskell-z-z-io-io-lib-for-haskell)
- <span class="section-num">8</span> [Haskell parser](#haskell-parser)
    - <span class="section-num">8.1</span> [Haskell json](#haskell-json)
        - <span class="section-num">8.1.1</span> [ChrisPenner/json-to-haskell: In goes JSON, out comes a complete Haskell model complete with instances! CLI and web interface available.](#chrispenner-json-to-haskell-in-goes-json-out-comes-a-complete-haskell-model-complete-with-instances-cli-and-web-interface-available-dot)
        - <span class="section-num">8.1.2</span> [nikita-volkov/jsonifier: Fast and simple JSON encoding toolkit](#nikita-volkov-jsonifier-fast-and-simple-json-encoding-toolkit)
- <span class="section-num">9</span> [Haskell implemented](#haskell-implemented)
    - <span class="section-num">9.1</span> [Gabriel439/simple-twitter: A bare-bones Twitter clone implemented in a single file](#gabriel439-simple-twitter-a-bare-bones-twitter-clone-implemented-in-a-single-file)
- <span class="section-num">10</span> [Haskell Data](#haskell-data)
    - <span class="section-num">10.1</span> [alasconnect/data-validation: A library that simplifies data validation.](#alasconnect-data-validation-a-library-that-simplifies-data-validation-dot)
- <span class="section-num">11</span> [Haskell Web](#haskell-web)
    - <span class="section-num">11.1</span> [alasconnect/haskell-web-app: Example of a base Haskell Servant web application](#alasconnect-haskell-web-app-example-of-a-base-haskell-servant-web-application):nix:
- <span class="section-num">12</span> [Hasktorch](#hasktorch)
    - <span class="section-num">12.1</span> [GTrunSec/hasktorch-jupyter-examples](#gtrunsec-hasktorch-jupyter-examples):owner:

</div>
<!--endtoc-->

tags
: [My learning Programming languages]({{< relref "programming-languages" >}})


## <span class="section-num">1</span> Haskell (programming language) {#haskell--programming-language}

Haskell is a general-purpose, statically typed, purely functional programming language with type inference and lazy evaluation. Developed to be suitable for teaching, research and industrial application, Haskell has pioneered a number of advanced programming language features such as type classes, which enable type-safe operator overloading. Haskell's main implementation is the Glasgow Haskell Compiler (GHC).


## <span class="section-num">2</span> Haskell books {#haskell-books}

-   [Programming in Haskell]({{< relref "my-books" >}})


## <span class="section-num">3</span> Haskell tutorial {#haskell-tutorial}


### <span class="section-num">3.1</span> [kowainik/learn4haskell: 👩‍🏫 👨‍🏫 Learn Haskell basics in 4 pull requests](https://github.com/kowainik/learn4haskell) {#kowainik-learn4haskell-learn-haskell-basics-in-4-pull-requests}


### <span class="section-num">3.2</span> Haskell video {#haskell-video}


#### <span class="section-num">3.2.1</span> [“Haskell for Imperative Programmers #1 - Basics - YouTube”🔊](https://www.youtube.com/watch?v=Vgu82wiiZ90&list=PLe7Ei6viL6jGp1Rfu0dil1JH1SHk9bgDV) {#haskell-for-imperative-programmers-1-basics-youtube}


#### <span class="section-num">3.2.2</span> [Tsoding - YouTube](https://www.youtube.com/c/Tsoding/playlists) {#tsoding-youtube}


### <span class="section-num">3.3</span> learning Haskell {#learning-haskell}


#### <span class="section-num">3.3.1</span> [kowainik/learn4haskell: 👩‍🏫 👨‍🏫 Learn Haskell basics in 4 pull requests](https://github.com/kowainik/learn4haskell) {#kowainik-learn4haskell-learn-haskell-basics-in-4-pull-requests}


#### <span class="section-num">3.3.2</span> [learning-haskell/SExpr.hs at master · stolyaroleh/learning-haskell](https://github.com/stolyaroleh/learning-haskell/blob/master/cis-194/src/Hw11/SExpr.hs) {#learning-haskell-sexpr-dot-hs-at-master-stolyaroleh-learning-haskell}


#### <span class="section-num">3.3.3</span> [tonymorris/fp-course: Functional Programming Course](https://github.com/tonymorris/fp-course) {#tonymorris-fp-course-functional-programming-course}


#### <span class="section-num">3.3.4</span> [Anton-Latukha/Haskell-Programming-From-First-Principles-exercises: Consists of QUALITY BELABORING of EVERY EXERCISE in the chapters {1-18,26} (~1400 pages) of the "Haskell book" ("Haskell Programming from First Principles"). With literate comments. Additionally notable for use of Nix for exercise projects.](https://github.com/Anton-Latukha/Haskell-Programming-From-First-Principles-exercises) {#anton-latukha-haskell-programming-from-first-principles-exercises-consists-of-quality-belaboring-of-every-exercise-in-the-chapters-1-18-26--1400-pages--of-the-haskell-book--haskell-programming-from-first-principles--dot-with-literate-comments-dot-additionally-notable-for-use-of-nix-for-exercise-projects-dot}


## <span class="section-num">4</span> Haskell Repositories {#haskell-repositories}


### <span class="section-num">4.1</span> [obsidiansystems/solana-bridges](https://github.com/obsidiansystems/solana-bridges) {#obsidiansystems-solana-bridges}


### <span class="section-num">4.2</span> [GitHub - AJChapman/co-log-polysemy-formatting: A Haskell library: A fancy logging effect for Polysemy using the formatting library to format log messages.](https://github.com/AJChapman/co-log-polysemy-formatting) {#github-ajchapman-co-log-polysemy-formatting-a-haskell-library-a-fancy-logging-effect-for-polysemy-using-the-formatting-library-to-format-log-messages-dot}

<span class="timestamp-wrapper"><span class="timestamp">[2020-10-30 Fri 16:32] </span></span> <- [logging library](logging_parser.md)


## <span class="section-num">5</span> Haskell user {#haskell-user}


### <span class="section-num">5.1</span> [idontgetoutmuch / Repositories](https://github.com/idontgetoutmuch?tab=repositories) {#idontgetoutmuch-repositories}


## <span class="section-num">6</span> Haskell llvm {#haskell-llvm}


### <span class="section-num">6.1</span> [llvm-hs Kaleidoscope Tutorial](https://lukelau.me/kaleidoscope/) {#llvm-hs-kaleidoscope-tutorial}


## <span class="section-num">7</span> Haskell lib {#haskell-lib}


### <span class="section-num">7.1</span> IO lib {#io-lib}


#### <span class="section-num">7.1.1</span> [haskell-Z/z-io: IO lib for haskell](https://github.com/haskell-Z/z-io) {#haskell-z-z-io-io-lib-for-haskell}


## <span class="section-num">8</span> Haskell parser {#haskell-parser}


### <span class="section-num">8.1</span> Haskell json {#haskell-json}


#### <span class="section-num">8.1.1</span> [ChrisPenner/json-to-haskell: In goes JSON, out comes a complete Haskell model complete with instances! CLI and web interface available.](https://github.com/ChrisPenner/json-to-haskell) {#chrispenner-json-to-haskell-in-goes-json-out-comes-a-complete-haskell-model-complete-with-instances-cli-and-web-interface-available-dot}


#### <span class="section-num">8.1.2</span> [nikita-volkov/jsonifier: Fast and simple JSON encoding toolkit](https://github.com/nikita-volkov/jsonifier) {#nikita-volkov-jsonifier-fast-and-simple-json-encoding-toolkit}


## <span class="section-num">9</span> Haskell implemented {#haskell-implemented}


### <span class="section-num">9.1</span> [Gabriel439/simple-twitter: A bare-bones Twitter clone implemented in a single file](https://github.com/Gabriel439/simple-twitter) {#gabriel439-simple-twitter-a-bare-bones-twitter-clone-implemented-in-a-single-file}


## <span class="section-num">10</span> Haskell Data {#haskell-data}


### <span class="section-num">10.1</span> [alasconnect/data-validation: A library that simplifies data validation.](https://github.com/alasconnect/data-validation) {#alasconnect-data-validation-a-library-that-simplifies-data-validation-dot}


## <span class="section-num">11</span> Haskell Web {#haskell-web}


### <span class="section-num">11.1</span> [alasconnect/haskell-web-app: Example of a base Haskell Servant web application](https://github.com/alasconnect/haskell-web-app) {#alasconnect-haskell-web-app-example-of-a-base-haskell-servant-web-application}


## <span class="section-num">12</span> Hasktorch {#hasktorch}


### <span class="section-num">12.1</span> [GTrunSec/hasktorch-jupyter-examples](https://github.com/GTrunSec/hasktorch-jupyter-examples) {#gtrunsec-hasktorch-jupyter-examples}
