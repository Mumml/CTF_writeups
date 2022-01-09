So the main task here is to find the flag using basic python scripting and have base knowledge of BASE64 encryption.

So letzs downlaod the picture:
- using strings and binwalnk gave no direct results.
Binwalk showed us a zip inside the picture.

with "foremost" command i extracted the zip file.
the zip file was protected.

after grep -R flag gave me an interesting output:
folders/73/47/p:The password is: "ctflag*****" where * is a number.
folders/73/43/p:The password is: "ctflag*****" where * is a number.

so lets try brute force this file:

i used python:

#!usr/bin/python3
from zipfile import ZipFile
from string import digits
import itertools

brute = itertools.product(digits,repeat=5)

with ZipFile("00000012.zip") as zf: # Path to 00000012.zip to be mentioned
    for i in brute:
        i = ''.join(i)
        password = "ctflag" + i
        try:
            zf.extractall(pwd=bytes(password,'utf-8'))
            print("Flag: " + password)
        except:
            pass


after running the script the password is: ctflag48625
after entering i got an arcive with a string in flag.txt:
RkxBR3ttYXlfdGhlX2JydXRlX2ZvcmNlX2JlX3dpdGhfeW91fQ==

ist clear that this is base64 encrypted so lets decypt it:
cat flag.txt|base64 -d

here we go!
FLAG{may_the_brute_force_be_with_you}