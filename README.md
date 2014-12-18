CharacterTransforms
===================

There exists a one-to-one Unicode character mapping between characters in languages that utilize multuple alphabets. When spoken, there is no difference.  However, when written, there is a large difference.

This repository contains Python Dictionary of character mappings for languages that have this property
Currently supporting:

Cantonese:<br>
    Traditional<br>
    Simplified<br>

Uyghur:<br>
   Arabic<br>
   Latin<br>
   Cyrillic<br>


An example is the Cantonese 'China'
Simplified: 中国
Traditional: 中國

A translation from Cantonese Traditional to Simplified can be accomplished with:

```
import maps
charmap = maps.getChineseMap()
traditional = u'中國'  #u'\u4e2d\u570b'
simplified = ''.join([cmap.get(c,c) for c in traditional])
print simplified #output 中国  or u'\u4e2d\u56fd'
```

Contributing
======

I am not a native speaker of any of these languages, so contributions (and tests) would be appreicated.


Example Use:

http://www.rfa.org/uyghur/?encoding=arabic
http://www.rfa.org/uyghur/?encoding=cyrillic

TODO
=======
Get this out of Python, and host as JSON so it's language independent<br>
Create "translation" function:<br>
  `translate(string, ToAlphabet, encoding='utf-8') #returns an encoded string in destination alphabet` <br>
So users don't have to write the code to iterate over the string, but can simply call `translate()`<br>
  
  
