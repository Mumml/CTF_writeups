# QR Code

Do you remember something known as QR Code? Simple. Here for you : <br /> https://mega.nz/#!eGYlFa5Z!8mbiqg3kosk93qJCP-DBxIilHH2rf7iIVY-kpwyrx-0


---
### Writeup:
So lets download the Image

Lets put the QR Code into an online decoder or scan the QR Code with your smartphone.
<br>
As a result we get something like this as raw text:
" c3ludCB2ZiA6IGEwX29icWxfczBldHJnX2RlX3BicXI "

Seems like ist encrypted in Base64...
So lets fire up CyberChef :D
https://gchq.github.io/CyberChef/
<br>
Put in the "From Base64"-Block and put the string into the right field.
As a result there is something like this:
"synt vf : a0_obql_s0etrg_de_pbqr"

<b>Hmm looks more like a solution but still encoded?</b>

Looks like a caesar-encryption or something like that.
Cyberchef has a simple block called ROT 13 (ist basically a caesar encryption algo)

So lets decode this with ROT 13

<br>
Yeah, we got our solution:

<b>CTFLearn{n0_body_f0rget_qr_code}</b>