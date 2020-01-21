## तोते को उड़ाएँ

अब जब आप <kbd>space</kbd> बार को दबाएँगे तो आपका Flappy (तोता) ऊपर की तरफ उड़ेगा। जब आप गेम खेलते हैं, तो आपको अपने कुंजी दबाने के समय पर ध्यान देना होगा ताकि Flappy (तोता) पाइपों की खाली जगहों में से निकल सके।

\--- no-print \---

![जब स्पेस बार दबाया जाता है तो तोता ऊपर की ओर उड़ता है](images/flappy-flying.gif)

\--- /no-print \---

जब आप <kbd>space</kbd> बार को दबाएँगे तो Flappy (तोता) ऊपर की तरफ उड़ेगा।

\--- task \---

`space key is pressed`{:class="block3events"} होने पर, Flappy (तोता) `changing its y coordinate`{:class="block3motion"} थोड़ा सा, उदाहरण के लिए `6` ऊपर उठेगा।

इस `repeating`{:class="block3control"} गतिविधि को `10 times`{:class="block3control"} बार करने पर Flappy (तोता) ऊपर की ओर उड़ता है।

इस कोड को अपने `Flappy` स्प्राइट में जोड़ें:

![तोता स्प्राइट](images/flappy-sprite.png)

```blocks3
when [space v] key pressed
repeat (10) 
  change y by (6)
end
```

\--- /task \---

अब आपको तोते के पंखों को फड़फड़ाना होगा!

\--- task \---

**Costumes (परिधान)** टैब पर क्लिक करें, और तोते के परिधानों का नाम 'wings up' (पंख ऊपर) और 'wings down' (पंख नीचे) रखें।

![परिधानों का नामकरण](images/flappy-wings.png)

\--- /task \---

\--- task \---

क्या आप तोते के परिधान को बीच रास्ते ऊपर की ओर उड़ते समय <kbd>space</kbd> दबाकर `wings down` में, और फिर इसे वापस `wings up` में बदल सकते हैं?

\--- hints \---

\--- hint \---

आपको ऊपर के हिलने-डुलने को आधे हिस्से के रूप में बाँटना होगा ताकि आप तोते के परिधान को आरंभ में और बीच में बदलने के लिए दो `repeat`{:class="block3control"} ब्लॉकों का उपयोग कर सकें।

तोता कैसा दिखता है इसे बदलने के लिए `switch costume to`{:class="block3looks"} ब्लॉक जोड़ें।

\--- /hint \--- \--- hint \---

आपको इन ब्लॉकों का उपयोग करने की आवश्यकता है:

![तोता स्प्राइट](images/flappy-sprite.png)

```blocks3
repeat (5) 
  change y by (6)
end

repeat (5) 
  change y by (6)
end

switch costume to (wings up v)

switch costume to (wings down v)

when [space v] key pressed
```

\--- /hint \---

\--- hint \---

आपका कोड इस प्रकार दिखना चाहिए:

![तोता स्प्राइट](images/flappy-sprite.png)

```blocks3
when [space v] key pressed
switch costume to (wings down v)
repeat (5) 
  change y by (6)
end
switch costume to (wings up v)
repeat (5) 
  change y by (6)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

अपने कोड का परीक्षण करें। जैसा कि आप देख रहे हैं, अगर आप तोते को पाइप से टकराने देते हैं तो इस समय कुछ भी नहीं होता है।

\--- /task \---