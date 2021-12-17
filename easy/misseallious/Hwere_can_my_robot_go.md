# Where do robots find what pages are on a website?

Hint:

    What does disallow tell a robot?

---
So basically there is nearly on very website an subdir called .../robots.txt
So look at this directory:
``` https://ctflearn.com/robots.txt```

This is the Output:

``` User-agent: * Disallow: /70r3hnanldfspufdsoifnlds.html ```

So lets look whats behind the disallowed subdirectory
``` https://ctflearn.com/70r3hnanldfspufdsoifnlds.html ```

Here we go, here is our flag:

CTFlearn{r0b0ts_4r3_th3_futur3}