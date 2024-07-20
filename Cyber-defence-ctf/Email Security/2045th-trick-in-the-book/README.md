# 2045th trick in the book

## Description

This is a common encoding system that phishers abuse in their endless quest to bypass email scanners. Can you figure out what it is?

```
=C6=96=D0=B5=CE=BD=D0=B5=C6=96=D0=B5=C6=92=C6=92=D0=B5=D1=81=C5=A5{=D4=81=
=CE=BF=D5=B8=C5=A5=5F=D1=98=CA=8B=D1=95=C5=A5=5F=D1=81=CE=BF=D1=80=D1=83=5F=
=D1=80=D0=B0=D1=95=C5=A5=D0=B5=5F=C5=A5=C4=A7=D1=96=D1=95=5F=D1=96=D5=B8=
=C5=A5=CE=BF=5F=C5=A5=C4=A7=D0=B5=5F=D0=AC=CE=BF=D1=85}
```


A quick search displays it as Quoted-Printable encoding but that isnt the answer.

The encoding itself also decodes in cyber chef into what looks like a flag:

ƖеνеƖеƒƒесť{ԁοոť_јʋѕť_сοру_раѕťе_ťħіѕ_іոťο_ťħе_Ьοх}

But it is not 100% correct and has some artifacts in it.

leveleffect{ԁοո't_јuѕt_сοру_раѕtе_thіѕ_іոtο_thе_box}

This did not work either..

In the end it just required me to rewrite the entire thing out without any copy paste.

leveleffect{dont_just_copy_paste_this_into_the_box}