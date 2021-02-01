# Krypton Level 7
## Part I
Enter the following command in your Terminal :

```bash
find / -name krypton7 -type f
cd /krypton/krypton6/
cat /krypton/krypton6/krypton7
# PNUKLYLWRQKGKBE
# The password for level 7 (krypton7) is encrypted with ‘encrypt6’.
```
```
mkdir /tmp/reda
cd /tmp/reda
ln -s /krypton/krypton6/keyfile.dat
chmod 777 .
echo 'LOREMIPSUMDOLORSITAMET' > plain1.txt
/krypton/krypton6/encrypt6 plain1.txt cipher1.txt
cat cipher1.txt
# PWTXPONASLNHSBJAZYXKGI : its the same lenght as the Lorem Ipsum
xxd -b plain1.txt
xxd -b cipher1.txt
```

```
  0101 0000
- 0100 1100
= 0000 0100 = (4) ~ (E)
```

```
printf 'A%.0s' {1..50} > plain2.txt
/krypton/krypton6/encrypt6 plain2.txt cipher2.txt
# EICTDGYIYZKTHNSIRFXYCPFUEOCKRN
# EICTDGYIYZKTHNSIRFXY
# It repeats
xxd -b plain2.txt
xxd -b cipher2.txt
# the first letter in the "key" is "E"
```
I'll try to decode with [Vigenere Cipher Decoder](https://www.dcode.fr/vigenere-cipher)
```
KEY : EICTDGYIYZKTHNSIRFXYCPFUEOCKRN
```
![Capture](https://github.com/Reda-BELHAJ/OverTheWire/blob/main/Krypton/Captures/Capture4.PNG)

## Part II
The ***host*** to which you need to connect is *krypton.labs.overthewire.org*, on ***port*** 2231. The ***username*** is *krypton7* and the ***password*** is the text from your clipboard [Part 1](https://github.com/Reda-BELHAJ/OverTheWire/edit/main/Krypton/Level7.md#part-i).
```bash
ssh krypton.labs.overthewire.org -p 2231 -l krypton7
# OR ssh krypton7@krypton.labs.overthewire.org -p 2231
# password: LFSRISNOTRANDOM
```
