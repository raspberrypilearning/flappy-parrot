## टकरावों का पता लगाएँ

गेम को एक चुनौती बनाने के लिए, खिलाड़ी को फ्लैपी का मार्गदर्शन करने की आवश्यकता होती है ताकि वह पाइप या स्टेज के किनारों को छुए बिना खाली जगहों में से निकल सके। फ्लैपी जब किसी चीज़ से टकराता है तो उसका पता लगाने के लिए आपको कुछ खंड जोड़ने की ज़रूरत होती है।

इसे **collision detection** (टकराव का पता लगाना) कहते हैं।

\--- task \---

लाइब्रेरी से कोई ध्वनि आयात करें जिसे आप फ्लैपी के किसी चीज़ से टकरा जाने पर बजाना चाहते हैं। 'screech' की ध्वनि एक अच्छा विकल्प है।

[[[generic-scratch3-sound-from-library]]]

\--- /task \---

यह जाँच करने के लिए `wait until`{:class="block3control"} खंड आवश्यक है कि क्या फ्लैपी `touching the pipes`{:class="block3sensing"} `or`{:class="block3operators"} `touching the edge`{:class="block3sensing"} को छू रहा है।

\--- task \---

'Flappy' (फ्लैपी) sprite में एक नया `when green flag clicked`{:class="block3control"} खंड जोड़ें, और निम्नलिखित कोड भी जोड़ें:

![तोता sprite](images/flappy-sprite.png)

```blocks3
when green flag clicked
wait until <<touching (Pipes v) ?> or <touching (edge v) ?>>
play sound (screech v)
```

\--- /task \---

\--- task \---

अपने कोड का परीक्षण करें। यदि तोता किसी पाइप को छूता है, तो 'screech' की ध्वनि बजनी चाहिए।

\--- /task \---

इसके बाद, कोड को अपडेट करें ताकि जब फ्लैपी किसी पाइप से टकराए तो गेम रुक जाए।

\--- task \---

टकराने का पता चलने के बाद गेम को रोकने के लिए निम्नलिखित कोड जोड़ें:

![तोता sprite](images/flappy-sprite.png)

```blocks3
when green flag clicked
wait until <<touching (Pipes v) ?> or <touching (edge v) ?>>
play sound (screech v)
+ say [Game Over!]
+ broadcast (Game Over v)
+ stop [other scripts in sprite v]
```

`broadcast`{:class="block3events"} खंड दूसरे sprites को बताता है कि गेम समाप्त हो गया है।

`stop`{:class="block3control"} खंड चल रही दूसरी फ्लैपी स्क्रिप्ट को रोकता है ताकि टकराने के बाद फ्लैपी गिरना बंद हो जाए।

\--- /task \---

\--- task \---

अंत में, `Pipes` sprite में निम्नलिखित कोड जोड़ें ताकि `when the sprite receives Game Over`{:class="block3events"} गेम समाप्त होने की सूचना मिलने पर पाइप `stop`{:class="block3control"} दिखने बंद हो जाएँ।

![पाइप्स sprite](images/pipes-sprite.png)

```blocks3
when I receive [Game Over v]
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

अपने गेम का परीक्षण करें और देखें कि आप 'Game over' होने से पहले कितनी देर तक खेल सकते हैं!

\--- /task \---