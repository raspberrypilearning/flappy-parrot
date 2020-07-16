## फ्लैपी को गिराएँ

अब Flappy नामक sprite जोड़ें और कोड बनाएँ ताकि फ्लैपी स्टेज से नीचे गिर जाए। अगले चरण में, आप कोड जोड़ेंगे ताकि जब आप कोई key (की) दबाएँ तो फ्लैपी उड़ने लग जाए।

--- no-print ---

![फ्लैपी गिरने का एनिमेशन](images/flappy-falling.gif)

--- /no-print ---

--- task ---

एक नया sprite जोड़ें जिसमें दो costumes हों, 'wings up' और 'wings down' के लिए, और इसका नाम `Flappy` रखें।

तोता sprite एक अच्छा विकल्प है।

![तोता sprite](images/flappy-sprite.png)

--- /task ---

फ्लैपी छोटा होना चाहिए।

--- task ---

`when the green flag is clicked`{:class="block3events"} `set Flappy's size to 25%`{:class="block3looks"} के लिए कोड जोड़ें।

![तोता sprite](images/flappy-sprite.png)

```blocks3
when green flag clicked
set size to (25) %
```

--- /task ---

जब गेम शुरू होता है, तो फ्लैपी स्टेज के मध्य में थोड़ा बाईं ओर, समन्वय `-50, 0` पर होना चाहिए।

![फ्लैपी आरंभ की स्थिति में दिखाया गया](images/flappy-starting-position.png)

--- task ---

`go to the x and y`{:class="block3motion"} कोड जोड़ें फ्लैपी को `x: -50`{:class="block3motion"} और `y: 0`{:class="block3motion"} के प्रारंभिक स्थिति में ले जाने के लिए।

![तोता sprite](images/flappy-sprite.png)

```blocks3
when green flag clicked
set size to (25) %
+ go to x: (-50) y: (0)
```

[[[generic-scratch3-set-coordinates]]]

--- /task ---

--- task ---

अब फ्लैपी को `forever`{:class="block3control"} `changing the sprite's y position by -3`{:class="block3motion"} से स्टेज से गिरते रहने दें।

![तोता sprite](images/flappy-sprite.png)

```blocks3
when green flag clicked
set size to (25) %
go to x: (-50) y: (0)
+ forever 
    change y by (-3)
end
```

--- /task ---

--- task ---

यह सुनिश्चित करने के लिए अपने कोड का परीक्षण करें कि फ्लैपी स्क्रीन के मध्य में शुरू होता है और नीचे तक गिरता है। जब आप फ्लैपी को खिसका कर स्टेज के शीर्ष पर ले जाते हैं, तो sprite को फिर से गिरना चाहिए।

--- /task ---