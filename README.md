# mkrpc - make random passcode
[https://danpub1.github.io/mkrpc/mkrpc-lite.html](https://danpub1.github.io/mkrpc/mkrpc-lite.html)

This represents a number of years of trying various other solutions, and accepting these as a reasonable compromise.
Every couple of a months, a forced password change and a bit more thinking about what works.
Not saying these choices are for everybody.
All of these solutions are for passcodes which need to be typed occasionally and into places which can't be reached with a password manager.

The wordlist based passcode generator uses a relatively short list of words, only 2048.
Longer lists end up having more obscure words, making them harder to remember.
These were chosen to be:
1. Unique in the first three characters, resulting in less typing (and less typing mistakes)
1. Concrete rather than abstract, and hopefully more memorable
2. Common
3. Short

The CVC-based passcode generator uses an even shorter list of CVC syllables, just 1296.
(1296 is the number of outcomes from rolling 4 dice.)
There are many more pronounceable 3-letter combinations, so a strong password could be made shorter.
But simplicity won out over shortness.

The base-32 generator uses an alphabet chosen to be written down.
(My handwriting is not neat enough for base-64.)
Write zero and Z (zed) with a slash and you shouldn't have to wonder what character is what.

### Update
[https://danpub1.github.io/mkrpc/mkrpc-air.html](https://danpub1.github.io/mkrpc/mkrpc-air.html)

Simplicity may win out.  Can't be convinced that the CVC-based passcodes are usefully pronounceable, and that the complexity of typing just the first three letters of words is worth it.

This version has a 2048-word dictionary of 4 letter words.  Just use them

### Update

Trying mixed case for the word-based passcodes in [mkrpc-air](https://danpub1.github.io/mkrpc/mkrpc-air.html), safer to write down.

## Base-32 / Base-36 Alphabet Rationale

The base-36 alphabet includes all 10 digits and all the letters, 13 uppercase and 13 lowercase,
so that the distribution of digits, uppercase, and lowercase are as similar as possible.
The lowercase letters are those found in 'doze with sky up',
which sounds like a suggestion to nap lying on your back.

The base-32 alphabet is all 10 digits, 11 uppercase letters, and 11 lowercase letters - 
so the distribution of digits, uppercase, and lowercase are all about the same.
The 4 letters excluded are those in ***sVG-y***,
which describes something with qualities similar to a Scalable Vector Graphics image. 

* 0 - Slash 0 to distinguish from o
* 1 - ok to write as one vertical stroke
* 7 - Do not slash 7 to avoid similarity with F
* A - Prefer A because a and o are similar
* B - Uppercase B because b is similar to 6, but take care to write the vertical stroke clearly to avoid confusion with 8
* C - Either would be ok, upper and lower are similar, choose upper to avoid similarity with a and e
* d - Lowercase d is preferred becauase D may be confused with 0 or o.
* e - Lowercase e is preferred to distinguish from F
* F - Uppercase F to distinguish from lowercase t
* G - be careful to write the 'chin' with straight lines to avoid similarity with 6. Not in base-32 because G is similar to 6 and g is similar to 8
* h - H or h is ok - use opposite case of N
* i - i is preferred because I may be confused with 1
* J - avoid j for similarity with i
* k - prefer lowercase k to distinguish from R
* L - Uppercase L to distinguish from 1
* M - Either would be ok, upper and lower are similar
* N - N or n is ok - use opposite case of H
* o - Lowercase o to distinguish from 0
* p - Either would be ok, upper and lower are similar
* Q - Uppercase Q to distinguish from 9
* R - Avoid lowercase r because of similarity with n or h
* s - Use lowercase to decrease similarity with 5.  Not in base-32 because of similarity with 5
* t - Lowercase t to distinguish from uppercase F
* u - Either would be ok, upper and lower are similar
* V - Uppercase to avoid similarity with u.  Not in base-32 because of similarity with U
* w - Either would be ok, upper and lower are similar
* X - Either would be ok, upper and lower are similar
* y - Use lowercase to avoid similarity with 4 or X, not in base-32 because of similarity to 4 or X
* z - lowercase z to distinguish from 2, Slash Z to distinguish from 2
