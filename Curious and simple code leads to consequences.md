# Curious and simple code leads to consequences

Standard buffer overflow attack.

Upon inspecting the code `char buf[128]` we find that the buffer is 128 bytes big. Simply inputting 128 characters causes a buffer overflow, spitting out the flag.

Flag is flag{pls_work}
