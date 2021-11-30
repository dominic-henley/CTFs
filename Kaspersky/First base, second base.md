# First base, second base

_You are in a relationship with a spy. Unfortunately they disappeared one day from your bed, but left this note behind.

Y2Flc2FyIHNhbGFkIHRoaXJ0ZWVuIHN5bnR7eXZzcnZmdW5lcX0=

What was the life advice your spy significant other give to you as a parting gift?_

The string ends with a = character, which immediately tells me it's probably encoded in base64.

Using an online base64 decoder gives us this message:
caesar salad thirteen synt{yvsrvfuneq}

From this point, we apply ROT13 to the flag and obtain the flag.

flag is flag{lifeishard}
