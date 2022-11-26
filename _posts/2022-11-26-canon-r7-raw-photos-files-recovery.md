---
layout: single
title:  "Canon R7 Raw files recovery with Photorec"
date:   2022-11-26 11:47:00 +0100
categories: canon r7 photorec recovery 
---

Data loss can be painful. And I think everyone has experienced it at least once. Recently It happened to me - my SDCARD reader, which I use to transfer photos from my Canon R7, reformated my card rendering all RAW and JPG disappeared.

I had previous experience with Data Recovery, so I was not really afraid. I launched [Photorec](https://www.cgsecurity.org/wiki/PhotoRec), my Swiss Army tool, to get the data back. I quickly learned that the recent format CRAW used in Canon R7 is not supported yet. Well.

I have decided not to give up and keep reading about the internals of Photorec. I found this - [how to add your own extensions to Photorec](https://www.cgsecurity.org/wiki/Add_your_own_extension_to_PhotoRec) - to learn that I need to find a place where a file starts.

I launched the hex editor, and I did start to compare other CRAW files created with Canon R7. And I found this string:

```hex
cr3 0 0x000000186674797063727820000000016372782069736f6d0000
```

I created a special file `photorec.sig`, started Photorec again, and had my files back!

I recorded also a mini tutorial which you can watch it in a multimedia way, enjoy:

{% include video id="r_jX0nbsfYY" provider="youtube" %}
