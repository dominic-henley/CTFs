# HTML was my first coding language

_Fun fact about me is that HTML was my first coding language. Anyways I made this URL and i was told that decoding it will let you guys capture another flag. How exciting!!!_

_ugzy%20pbqvat%20(synt%7Bjro_qri_vf_njrfbzr%7D)vf%20fb%20zhpu%20sha!_

Applying ROT13 to this string gives us 

html%20coding%20(flag%7Oweb_dev_is_awesome%7Q)is%20so%20much%20fun!

We can see bits of the flag, but there seems to be some parts that look weird. Remember thata this is an encoded URL, so %7B and %7D from the encoded URL will give us { } respectively, thus revealing the flag.

flag is flag{web_dev_is_awesome}
