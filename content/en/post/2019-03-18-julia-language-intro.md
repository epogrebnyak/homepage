+++
title = "Julia Programming Language Introduction"
date = 2019-03-18T11:23:56+03:00
draft = false

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["julia", "programming", "econometrics"]
categories = []

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""
+++

On DEV.to ["Julia, surprise me!"](https://dev.to/epogrebnyak/julialang-and-surprises---what-im-learning-with-a-new-programming-language--21df) maps my learning of the Julia programming language as a series of pleasant and 
less satisfying surprises. 

Since then my biggest roadblock to Julia was the [recompilation time of the dependencies](
https://discourse.julialang.org/t/mac-resolving-package-versions-takes-a-long-time/16905/3?u=epogrebnyak).

Not much fun seeing your code execute in milliseconds, if you have to wait a minute for a dependency to 'precompile'. Repeating that in cylces each time you run a test is not good.  

```
julia> @time using LessOLS
[ Info: Precompiling LessOLS [3e4c6e70-f926-11e8-0fa5-39915c5a2b72]
 57.375232 seconds (2.92 M allocations: 159.585 MiB, 0.20% gc time)
```

The issue is [addressed by the Julia community](https://github.com/JuliaLang/julia/issues/28425),
and may possibly be fixed by [Revise.jl drop in](https://discourse.julialang.org/t/mac-resolving-package-versions-takes-a-long-time/16905/12?u=epogrebnyak). 

My primary project with Julia is [LessOLS.jl](https://github.com/epogrebnyak/LessOLS.jl), a from-scratch excercise in econometrics.