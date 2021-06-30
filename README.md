# mkrpc
https://danpub1.github.io/mkrpc/mkrpc-lite.html

This represents a number of years of trying various other solutions, and accepting these as a reasonable compromise.
Every couple of a months, a forced password change and a bit more thinking about what works for me.
Not saying these choices are for everybody.
All of these solutions are for passcodes which need to be typed occasionally and into places which can't be reached with a password manager.

The wordlist based passcode generator uses a relatively short list of words, only 2048.
Longer lists end up having more obscure words, making them harder to remember.
These were chosen
1. to be unique in the first three characters, resulting in less typing (and less typing mistakes)
1. to be concrete rather than abstract, and hopefully more memorable
2. to be common
3. to be short

The CVC-based passcode generator uses an even shorter list of CVC syllables, just 1296.
(1296 is the number of outcomes from rolling 4 dice.)
There are many more pronounceable 3-letter combinations, so a strong password could be made shorter.
But simplicity won out over length.

The base-32 generator uses an alphabet chosen to be written down.
(My handwriting is not neat enough for base-64.)
Write zero and Z (zed) with a slash and you shouldn't have to wonder what character is what.
