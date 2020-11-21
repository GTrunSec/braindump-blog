+++
title = "Jupyter Haskell"
lastmod = 2020-11-21T03:18:33-08:00
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

- <span class="section-num">1</span> [Jupter Notebook Programming in Haskell org-mode](#jupter-notebook-programming-in-haskell-org-mode--org-mode-dot-md)
    - <span class="section-num">1.1</span> [Chapter 1](#chapter-1)
    - <span class="section-num">1.2</span> [Chapter 2](#chapter-2)
- <span class="section-num">2</span> [diagrams-gallery -> Jupyter Data Science](#diagrams-gallery-jupyter-data-science--jupyter-data-science-dot-md)

</div>
<!--endtoc-->

tags
: [Jupyter Data Science]({{< relref "Jupyter-data-science" >}}), [My Haskell]({{< relref "my-haskell" >}})


## <span class="section-num">1</span> Jupter Notebook Programming in Haskell [org-mode]({{< relref "org-mode" >}}) {#jupter-notebook-programming-in-haskell-org-mode--org-mode-dot-md}

:ID:       6438c7d9-22f2-4aff-9c68-3ac5f5b7caab

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-10-29 Thu 18:28] </span></span> -> [Programming in Haskell](my-books.md)


### <span class="section-num">1.1</span> Chapter 1 {#chapter-1}

```ein

```

<a id="code-snippet--04a67be7-62e0-4865-a46e-d2fd38743400"></a>
```ein-haskell
let pair = (2, "orange")
```

<a id="code-snippet--3945a629-cafb-4b58-be8a-6b07f91aa96d"></a>
```ein-haskell
pair
```

```text
orange
```

<a id="code-snippet--93b73bda-ab8e-47dd-a31f-3d0c8364b6bf"></a>
```ein-haskell
1:[2,3,4]
```

```text
[1,2,3,4]
```


### <span class="section-num">1.2</span> Chapter 2 {#chapter-2}

&#x2013; Hanoi

```haskell
hanoiN :: Integer -> [Peg] -> [Move]
hanoiN 0 _ = []
hanoiN 1 (p1 : p2 : rest) = [(p1, p2)]
hanoiN n (p1 : p2 : p3 : rest) =
    hanoiN k (p1 : p3 : p2 : rest) ++
    hanoiN (n - k) (p1 : p2 : rest) ++
    hanoiN k (p3 : p2 : p1 : rest)
    where k = if null rest then n - 1 else n `quot` 2
hanoiN _ _ = error "Invalid configuration"
```


## <span class="section-num">2</span> diagrams-gallery -> [Jupyter Data Science]({{< relref "Jupyter-data-science" >}}) {#diagrams-gallery-jupyter-data-science--jupyter-data-science-dot-md}

-   [jupyter/Gray.ipynb at master · Yvee1/jupyter](https://github.com/Yvee1/jupyter/blob/master/Haskell/diagrams-gallery/Gray.ipynb) -> [My Haskell]({{< relref "my-haskell" >}})
