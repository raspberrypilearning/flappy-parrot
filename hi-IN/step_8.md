## स्कोर जोड़ें

हर बार जब फ्लैपी पाइपों के बीच की खाली जगह से निकल जाए तो खिलाड़ी को एक अंक प्राप्त होना चाहिए।

\--- task \---

एक नया वेरिएबल बनाए **सभी sprites** के लिए और इसका नाम `score`{:class="block3variables"} रखें।

[[[generic-scratch3-add-variable]]]

\--- /task \---

प्रत्येक 'Pipes' (पाइप्स) sprite क्लोन को `wait until`{:class="block3control"} फ्लैपी के उड़ कर निकल जाने की प्रतीक्षा करनी चाहिए और फिर `score`{:class="block3variables"} में वृद्धि करनी चाहिए।

\--- task \---

पहले, गेम के शुरू होने पर `set score to 0`{:class="block3variables"} का उपयोग करें:

![पाइप्स sprite](images/pipes-sprite.png)

```blocks3
when green flag clicked
+ set [score v] to [0]
set size to (200) %
hide
forever 
  create clone of (myself v)
  wait (2) seconds
end
```

\--- /task \---

\--- task \---

फिर `Pipes` sprite में निम्नलिखित कोड जोड़ें:

![पाइप्स sprite](images/pipes-sprite.png)

```blocks3
when I start as a clone
wait until <>
```

\--- /task \---

\--- task \---

और अधिक कोड जोड़ें ताकि, जब फ्लैपी की `x` स्थिति पाइप क्लोन की `x` स्थिति से अधिक हो, तो `score`{:class="block3variables"} में `1` की वृद्धि होती है और आपकी पसंद की ध्वनि बजती है।

यदि आप चाहें तो 'pop' की ध्वनि का उपयोग कर सकते हैं, या लाइब्रेरी से कोई ध्वनि जोड़ सकते हैं, उदाहरण के लिए 'bird'।

\--- hints \---

\--- hint \---

आपको `wait until`{:class="block3control"} तब तक प्रतीक्षा करनी होगी जब तक `Flappy's x position`{:class="block3sensing"} `Pipes` की `x position`{:class="block3motion"} स्थिति `greater than (>)`{:class="block3operators"} से अधिक हो।

![पाइप्स sprite](images/pipes-sprite.png)

```blocks3
when I start as a clone
+ wait until <>
```

फिर `change score by 1`{:class="block3variables"} और `play a sound`{:class="block3sound"}।

\--- /hint \---

\--- hint \---

इन खंडो का सही क्रम में उपयोग करें:

![पाइप्स sprite](images/pipes-sprite.png)

```blocks3
when I start as a clone
wait until <>

play sound (pop v)

change [score v] by (1)

[x position v] of (Flappy v)

x position

() > ()
```

\--- /hint \---

\--- hint \---

आपका कोड इस प्रकार दिखना चाहिए:

![पाइप्स sprite](images/pipes-sprite.png)

```blocks3
when I start as a clone
wait until <([x position v] of (Flappy v)) > (x position)>
change [score v] by (1)
play sound (pop v)
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

अपने कोड का परीक्षण करें और सुनिश्चित करें कि हर बार जब फ्लैपी पाइपों के बीच की खाली जगह में से निकलता है तो आप एक अंक स्कोर करते हैं। जाँच करें कि जब आप कोई नया गेम शुरू करते हैं तो `score`{:class="block3variables"} (स्कोर) `0` पर सेट किया होता है।

\--- /task \---