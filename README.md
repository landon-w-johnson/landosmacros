# Overview

This is a LaTeX package that I made for myself to make typesetting bra-ket notation easier and quicker. It has since expanded a bit into various other mathematical macros. As I get annoyed with repetitively hard-coding things, I add them to this package. It should work nicely with any other packages that you use. It requires the `amsmath` and `amssymb` packages.



# Macros

- `\bra{stuff}` will give you <stuff| where the vertical bar and left angle are both automatically resized (to the same size) so that stuff fits inside of them.

![bra](sample-images/bra.png?raw=true)

- `\ket{stuff}` will give you |stuff> where the vertical bar and right angle are both automatically resized (to the same size) so that stuff fits inside of them.

![ket](sample-images/ket.png?raw=true)

- `\braket{m}[\hat{H}]{n}` will give you <m|H|n> with a hat on the H where the vertical bars and angle brakets are all automatically resized (to the same size) so that the bra, ket, and operator stuff all fit inside of them. The square brakets along with their argument are optional and this macro will automatically detect whether or not you used them to only display a single vertical bar in the middle if you did not use the optional argument.

![braket](sample-images/braket.png?raw=true)
![braket2](sample-images/braket2.png?raw=true)

- `\ketbra{0}{1}` will give you |0><1| where the vertical bars and angle brakets are automaticlly resized (to the same size) so that the stuff fits inside of them.

![ketbra](sample-images/ketbra.png?raw=true)

- `\ev{\hat{H}}` will give you <H> with a hat on the H where the angle brakets are automatically resized (to the same size) so that the stuff fits inside of them. This is intended for use as the *e*xpectation *v*alue.

![ev](sample-images/ev.png?raw=true)

- `\com{x,p_x}` will give you [x,p_x] where the square brakets are automatically resized (to the same size) so that the stuff fits inside of them. This is intended for use as the *com*mutator.

![com](sample-images/com.png?raw=true)

- `\inf` is the infinity symbol. By default, this macro is the infemum and `\infty` is the infinity symbol. I have a hard time believing that anybody uses the infemum more than the infinity symbol, so I changed it.

![inf](sample-images/inf.png?raw=true)

- `\infemum` is the infemum. I had to add this macro in case I still needed the infemum. The sample image below is `$\displaystyle \infemum_{x\in S}x>1$`.

![infemum](sample-images/infemum.png?raw=true)

- `\pd[2][f]{x}` is the partial derivative. This particular example will yield the second partial derivative of f with respect to x. The square brakets along with their contnets are optional. If you only include one set of square brakets, it will be the order of the derivative.

![pd](sample-images/pd.png?raw=true)

- `\td[][u]{t}` is the total derivative. This particular example will yield the first total derivative of u with respect to t. The square brakets along with their contnets are optional. If you only include one set of square brakets, it will be the order of the derivative.

![td](sample-images/td.png?raw=true)

- `\csqr{stuff}` will give you |stuff|^2. It is intended for use as the *c*omplex *square*, but it works just as well for any other magnitude squared as long as you only want single vertical bars on either side of your stuff.

![csqr](sample-images/csqr.png?raw=true)

- `\eval{stuff}` will give you stuff| where there is only a single vertical bar on the right side of your stuff. The vertical bar will automatically resize according to the size of your stuff. It is indended for after you've taken the integral of a function, but you still need to *eval*uate it at the boundaries. The sample image below is `$\displaystyle \eval{\frac{1}{2}x^2}_0^1$`.

![eval](sample-images/eval.png?raw=true)

- `\norm{stuff}` will give you ||stuff|| with double vertical bars on either side that automatically resize (to the same size) so that your stuff fits inside of them. It is intended for use as the norm. The sample image below is `$\norm{f}_{L^2}^2$`.

![norm](sample-images/norm.png?raw=true)

- `\abs{stuff}` will give you |stuff| with single vertical bars on either side that automatically resize (to the same size) so that your stuff fits inside of them. It is intended for use as the *abs*olute value.

![abs](sample-images/abs.png?raw=true)



# How To Make LaTeX See This Package

You have two options for this:

1. Have a copy of `landosmacros.sty` in your working directory, i.e. the one with your `.tex` file. I have verified that this works on Overleaf as well as on a local machine.

1. `texhash` the file `landosmacros.sty` into your LaTeX libraries so that LaTeX can always see it. I virtually always compile locally, so I don't know if there's a way to make this work on Overleaf. On my Linux machines, this means creating the directory `/usr/share/texmf-dist/tex/latex/landosmacros/` and putting `landosmacros.sty` inside that directory. Then run `texhash /usr/share/texmf-dist/tex/latex`. I gave up on Windows and MacOS long ago, so I don't know how the equivalent process works on those operating systems because I haven't had to do it yet. However, it should be pretty close to identical on MacOS, since that's built on Unix.



# Issues/Wish You Had Another Macro?

Email me at landon.w.johnson@ndsu.edu if you run into any problems or if you are also getting tired of hard-coding things into your LaTeX documents over and over again. I'd be happy to help!
