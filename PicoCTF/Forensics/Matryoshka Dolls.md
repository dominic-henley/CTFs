# Matryoshka Dolls

*Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one?*

This challenge comes with an image.

![dolls](https://user-images.githubusercontent.com/80395298/126905999-b90e24c0-e483-42c6-97c3-5d2e271ebcce.jpg)

Right off the bat, instict points me towards this challenge being a steganography challenge. The description also supports this idea, hinting that there are probably files within the files.

repeatedly extracting files in the image using binwalk results in the flag.

`flag:picoCTF{4cf7ac000c3fb0fa96fb92722ffb2a32}`
