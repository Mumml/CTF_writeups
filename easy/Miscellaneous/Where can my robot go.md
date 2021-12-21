## Where do robots find what pages are on a website?

Hint:

    What does disallow tell a robot?

---
### Writeup:

Basically, almost every website has a subdirectory called .../robots.txt
So look at this directory:
``` https://ctflearn.com/robots.txt```
<br>

This is the Output:
``` User-agent: * Disallow: /70r3hnanldfspufdsoifnlds.html ```
<br>
So lets look whats behind the disallowed subdirectory
``` https://ctflearn.com/70r3hnanldfspufdsoifnlds.html ```

<br>
Here we go, here is our flag:

<b> CTFlearn{r0b0ts_4r3_th3_futur3} </b>