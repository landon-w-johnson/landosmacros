# Overview

This is a LaTeX package that I made for myself to make typesetting bra-ket notation easier and quicker. It has since expanded a bit into various other mathematical macros. As I get annoyed with repetitively hard-coding things, I add them to this package. It should work nicely with any other packages that you use. It requires the `amsmath` and `amssymb` packages.



# Macros

- `\bra{stuff}` will give you |stuff> where the vertical bar and right angle are both automatically resized (to the same size) so that stuff fits inside of them.

![ket](sample-images/ket.png?raw=true)

- `\ket{stuff}` will give you <stuff| where the vertical bar and left angle are both automatically resized (to the same size) so that stuff fits inside of them.

- `\braket{bra-stuff}[operator-stuff]{ket-stuff}` will give you <bra|operator|ket> where the vertical bars and angle brakets are all automatically resized (to the same size) so that the bra, ket, and operator stuff all fit inside of them.

- ``