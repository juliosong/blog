---
title: "Generative grammar for <em>I Ching</em> divination (Part 6): Linguistics II"
categories: [linguistics, metaphysics]
tags: [I Ching, divination, generative grammar]
header:
  overlay_image: /assets/images/iching.png
  show_overlay_excerpt: false
  image_description: "the eight trigrams of I Ching and the tai chi symbol"
  caption: "I Ching trigrams and the Tai Chi symbol (credit: <a href='https://commons.wikimedia.org/wiki/File:Pakua.svg' title='via Wikimedia Commons'>Benoît Stella alias BenduKiwi</a> / <a href='http://creativecommons.org/licenses/by-sa/3.0/'>CC BY-SA</a>)"
  teaser: /assets/images/iching.png
toc: true
toc_sticky: true
---

([link to part 5]({{ site.baseurl }}{% post_url 2020-04-20-generative-grammar-of-i-ching-part5 %}))

## Feature structure
Generative grammarians love using features to represent linguistic objects. This is a basic methodology in both transformational-generative grammar and other, [nontransformational](https://en.wikipedia.org/wiki/Generative_grammar#Frameworks) generative frameworks (most typically in [head-driven phrase structure grammar](https://en.wikipedia.org/wiki/Head-driven_phrase_structure_grammar)). Features are usually put in square brackets in an `[attribute: value]` format.

<span style="font-family:serif; font-variant:small-caps; background-color:GoldenRod;">&nbsp;Example&nbsp;</span> &nbsp;That _dog_ is a singular noun can be represented by the feature `[number: singular]` and that _ran_ is a past-tense verb by the feature `[tense: past]`. Features can be grouped into sets, called [feature structures](https://en.wikipedia.org/wiki/Feature_structure), such as
```
[person: third, number: singular, gender: masculine]
```
which represents the pronoun _he_. This way of representing properties shouldn't be too alien; it's also used in many other fields. For instance, the CSS code for my <span style="font-family:serif; font-variant:small-caps; background-color:GoldenRod;">&nbsp;Example&nbsp;</span> icon is
```
{font-family: serif; font-variant: small-caps; background-color: GoldenRod;}
```
which is essentially also a feature structure.

The divinatory properties associated with _I Ching_ lines and line slots can be represented by features. Recall from Parts [3]({{ site.baseurl }}{% post_url 2020-04-13-generative-grammar-of-i-ching-part3 %}) and [4]({{ site.baseurl }}{% post_url 2020-04-17-generative-grammar-of-i-ching-part4 %}) that there are four types of lines in the _I Ching_, which are defined by two properties: yin/yang (i.e., the line's _gender_) and old/young (i.e., the developmental _stage_ the line represents).

<span style="font-family:serif; font-variant:small-caps; background-color:GoldenRod;">&nbsp;Example&nbsp;</span> &nbsp;The old yang line (⚊&#9711;) can be represented as
```
[gender: yang, stage: old]
```
and the young yin line (⚋) as
```
[gender: yin, stage: young]
```
A hexagram is just a more complex feature structure---with an additional feature indicating each line's position---such as
```
[
  [position: 1, gender: yin, stage: young],
  [position: 2, gender: yang, stage: young],
  [position: 3, gender: yang, stage: old],
  [position: 4, gender: yin, stage: old],
  [position: 5, gender: yang, stage: young],
  [position: 6, gender: yin, stage: old]
]
```
which <a id="ching"></a>represents ䷯ (_ching_ 'the well' <span class="hanyu">井</span>) with three changing lines (1, 3, 4). Since old lines are changing by definition, there's no need for an extra transformation feature `[changing]`.

Now, suppose there's a transformation function, which takes a hexagram as input and returns another hexagram as output. It would convert the above feature structure to a new one with
1. the gender values of all `old` lines toggled, and
2. all `stage` features deleted.

```
transform(䷯) =
[
  [position: 1, gender: yin],
  [position: 2, gender: yang],
  [position: 3, gender: yin],
  [position: 4, gender: yang],
  [position: 5, gender: yang],
  [position: 6, gender: yang]
]
= ䷅
```
This is just the [aforementioned]({{ site.baseurl }}{% post_url 2020-04-20-generative-grammar-of-i-ching-part5 %}#sung) _sung_ 'conflict' (<span class="hanyu">訟</span>), which by the way isn't too good a change.😔

## Further exploitation of the featural tool
### Agreement
An important functionality of features in generative grammar is to model the widespread grammatical phenomenon of [agreement](https://en.wikipedia.org/wiki/Agreement_(linguistics)). In transformational-generative grammar this is done via a pair of "valued" and "unvalued" features.

<span style="font-family:serif; font-variant:small-caps; background-color:GoldenRod;">&nbsp;Example&nbsp;</span> &nbsp;Nominal phrases have valued person and number features while tensed verbs have unvalued ones. By copying over the person/number values from the former to the latter we can derive the subject-verb agreement phenomenon. Thus, in _he sings_ the pronoun _he_ bears
```
[person: third, number: singular]
```
and the tensed verb _sing_ bears
```
[person: [], number: []]
```
We copy the two values from _he_ onto _sing_, and the latter gets pronounced as _sings_, which reflects the agreement process.

There's no feature-copying or overt pronunciation in _I Ching_ divination, but some sort of feature-based agreement does exist. We've already seen this in [Part 4]({{ site.baseurl }}{% post_url 2020-04-17-generative-grammar-of-i-ching-part4 %}#agree), where I mentioned that one of the criteria for an auspicious line was the agreement between its gender and the gender of its slot. This can be modeled by a boolean-valued function
```
agree(line gender, slot gender) = True | False
```
Thus, a yin line in a yang slot isn't good because
```
agree(yin, yang) = False
```
We can evaluate the overall degree of auspiciousness of a hexagram by counting the number of Trues returned by the agreement process, though we should probably count in other factors like the [cross-line relationships]({{ site.baseurl }}{% post_url 2020-04-17-generative-grammar-of-i-ching-part4 %}#crossline) as well if we want to get an accurate evaluation (more on this later).

<span style="font-family:serif; font-variant:small-caps; background-color:GoldenRod;">&nbsp;Example&nbsp;</span> &nbsp;Applying the agreement function to the six lines in ䷓ (_kuan_ 'view' <span class="hanyu">觀</span>), we get three Trues and three Falses.
```
agree(line1, slot1) = [gender(line1) == gender(slot1)]
= [yin == yang] = False
agree(line2, slot2) = [yin == yin] = True
agree(line3, slot3) = [yin == yang] = False
agree(line4, slot4) = [yin == yin] = True
agree(line5, slot5) = [yang == yang] = True
agree(line6, slot6) = [yang == yin] = False
```
However, since two out of the three Trues occur in central slots (i.e., they are [perfectly central]({{ site.baseurl }}{% post_url 2020-04-17-generative-grammar-of-i-ching-part4 %}#perfectly)), the auspiciousness level of the hexagram is actually much higher than average. Next I turn to represent this state of affairs in featural terms.

### Unification
We can let the feature structure of a line and that of its insertion slot go through a unification process similar to that in unification-based grammars like [HPSG](https://web.archive.org/web/20120204060804/http://emsah.uq.edu.au/linguistics/Working%20Papers/ananda_ling/HPSG_Summary.htm#_2.2._Rules,_principles).

<div style="padding-left:20px; padding-right:20px; padding-top:20px; padding-bottom:20px; margin-bottom: 30px; display:block; background-color:#eff; font-family:monospace; font-size:80%;">
<span style="display:block; color:gray; padding-bottom:12px;"><i>Unification is a conjunction-like operation that integrates information from compatible feature structures. The following examples are adapted from <a href="https://dash.harvard.edu/handle/1/11576719">Shieber (2003)</a>.</i></span>
<i>Example 1:</i><br>
[category: noun] ⨆ [agreement: [number: singular]] =<br>
[category: noun, agreement: [number: singular]]<br>
<span style="display: block; padding-top: 12px;"><i>Example 2:</i></span>
[agreement: [number: singular]] ⨆<br>
[agreement: [person: third]] = <br>
[agreement: [number: singular, person: third]]
</div>

Now let's do two things:
1. Suppose the "gender agreement" in _I Ching_ divination replaces the respective gender features of a line and its insertion slot with a new, boolean feature `[agree: True | False]`.
2. Equip the line slot feature structure with an additional boolean feature `[central: True | False]`, which indicates whether a slot has a central position in its ambient trigram.

With the above preparation, if we sequence line/slot unification after line/slot agreement, we'll get an integrated feature structure that contains both `agree` and `central`.
```
(unify ∘ agree) (line1, slot1) =
[stage: young, agree: False] ⨆
[position: 1, central: False, agree: False] =
[
  position: 1,
  stage: young,
  central: False,
  agree: False
]
```
And we are now able to represent the [central and correct]({{ site.baseurl }}{% post_url 2020-04-17-generative-grammar-of-i-ching-part4 %}#correctly) line property in featural terms---by counting how many times the substructure `[central: True, agree: True]` occurs in a hexagram's `unify ∘ agree` values. Let's still take ䷓ (_kuan_ 'view' <span class="hanyu">觀</span>) for example---and let's ignore its potential changing lines for now.
<pre style="margin-bottom:0;">
<code style="font-family:Monaco; font-size:75%; background-color:#1d1f21; color:#c6c8c6; line-height:1.8; display:block; height:300px; overflow:scroll; padding-left:15px; padding-bottom:20px; border-radius:5px;">
(unify ∘ agree) (line1, slot1) =
[position: 1, central: False, agree: False]
(unify ∘ agree) (line2, slot2) =
[position: 2, central: True, agree: True]
(unify ∘ agree) (line3, slot3) =
[position: 3, central: False, agree: False]
(unify ∘ agree) (line4, slot4) =
[position: 4, central: False, agree: True]
(unify ∘ agree) (line5, slot5) =
[position: 5, central: True, agree: True]
(unify ∘ agree) (line6, slot6) =
[position: 6, central: False, agree: False]
</code>
</pre>
There are two `[central: True, agree: True]` occurrences in _kuan_'s `unify ∘ agree` values, which makes it a perfectly-central hexagram---namely, it's awesome.

Next, let's turn to a hexagram with changing lines. Take the <a href="#ching">above-mentioned</a> ䷯ (_ching_ 'the well' <span class="hanyu">井</span>) for example, whose first, third, and fourth lines are changing. I've also filled in the [slot-quality]({{ site.baseurl }}{% post_url 2020-04-17-generative-grammar-of-i-ching-part4 %}#qualit) features mentioned in Part 4.
<pre style="margin-bottom:0;">
<code style="font-family:Monaco; font-size:75%; background-color:#1d1f21; color:#c6c8c6; line-height:1.8; display:block; height:300px; overflow:scroll; padding-left:15px; padding-bottom:20px; border-radius:5px;">
(unify ∘ agree) (line1, slot1) =
[
  position: 1,
  quality: n/a,
  stage: old,
  central: False,
  agree: False
]
(unify ∘ agree) (line2, slot2) =
[
  position: 2,
  quality: meritorious,
  stage: young,
  central: True,
  agree: False
]
(unify ∘ agree) (line3, slot3) =
[
  position: 3,
  quality: dangerous,
  stage: old,
  central: False,
  agree: True
]
(unify ∘ agree) (line4, slot4) =
[
  position: 4,
  quality: disquieting,
  stage: old,
  central: False,
  agree: True
]
(unify ∘ agree) (line5, slot5) =
[
  position: 5,
  quality: best,
  stage: young,
  central: True,
  agree: True
]
(unify ∘ agree) (line6, slot6) =
[
  position: 6,
  quality: n/a,
  stage: young,
  central: False,
  agree: True
]
</code>
</pre>
There's only one double-`True` line in this hexagram (i.e., the hexagram has a central and correct line), but it occupies the best (i.e., fifth) slot in the hexagram. As such, the hexagram _ching_ is not as auspicious as _kuan_ but still quite okay, especially considering it in addition has four single-`True` lines.

The two examples above well illustrate how the feature tool in generative grammar can provide a new perspective on _I Ching_ divination. There may still be other aspects of the divination process that can be given a feature-based modeling, but I'll stop here before the post becomes too long-winded. Anyway, I think I've made my point.

## Final thoughts
Generative grammar is a theoretical school in linguistics, but its ideas and methods can potentially have a wider impact. In this article I demonstrated how it can be used to examine the symbolic system of the _I Ching_, and I remember once seeing a Nobel Prize lecture entitled "[The Generative Grammar of the Immune System](https://www.nobelprize.org/prizes/medicine/1984/jerne/lecture/)" (Niels K. Jerne, 1984). Perhaps someday there will eventually be a field of study named "applied generative grammar." That would be super cool.

I appreciate the profoundness and neatness of the _I Ching_---both as a divination manual and as a philosophical classic---and also admire its intricate yet highly organized symbolic system, which essentially builds the entire universe on just two notions: yin and yang (at least that's the idea). This system is so remarkable---especially considering how old it is---that [Gottfried Leibniz](https://en.wikipedia.org/wiki/Binary_number#Leibniz_and_the_I_Ching) actually [referenced it](https://www.inverse.com/article/46593-gottfried-wilhelm-leibniz-i-ching-binary-system) in the title of one of his most influential papers: "[Explanation of the binary arithmetic, which uses only the characters 1 and 0, with some remarks on its usefulness, and on the light it throws on the ancient Chinese figures of Fu Xi](http://www.leibniz-translations.com/binary.htm)."
>Binary code, powered by modern computers, has an amazing capacity to represent reality, which Gottfried Wilhelm von Leibniz could barely have conceived. The ancient authors of the I-Ching might have understood its potential---and its pitfalls---even better than we do.<br>
><span style="text-align: right; display: block;"> --- [The Guardian](https://www.theguardian.com/books/2014/mar/21/ancient-book-wisdom-i-ching-computer-binary-code)</span>

Leibniz wasn't the only famous scholar in history who had publicly expressed their interest in the _I Ching_---[Niels Bohr](https://sureshemre.wordpress.com/2015/02/14/niels-bohrs-fascination-with-yin-and-yang/) had even sewed the yin-yang symbol (☯) on his coat of arms when he received the Order of the Elephant from the King of Denmark.

{% include figure image_path="/assets/images/leibniz-bohr.png" alt="Leibniz's copy of I Ching hexagrams and Bohr's coat of arms with the yin-yang symbol" caption="[Leibniz's copy of _I-Ching_ hexagrams](https://commons.wikimedia.org/wiki/File:Diagram_of_I_Ching_hexagrams_owned_by_Gottfried_Wilhelm_Leibniz,_1701.jpg) (left) and [Bohr's coat of arms](https://commons.wikimedia.org/wiki/File:Coat_of_Arms_of_Niels_Bohr.svg) (right)" %}

In our own era, the advent of new technology has only increased the public's interest in this ancient "book of wisdom" and its implications for various domains of knowledge. For instance, I have seen repeated attempts to draw parallelisms between the _I Ching_ and DNA (see [this book](https://books.google.com/books/about/I_Ching_and_the_Genetic_Code.html?id=0X0IAAAACAAJ&source=kp_book_description&redir_esc=y), [this paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3575644/), and [this blogpost](https://taobabe.rocks/dna-and-the-i-ching-the-connection/)). I don't have the expertise to evaluate the scientific validity of these attempts, though I find [this blogger](https://aeon.co/essays/forget-prophecy-the-i-ching-is-an-uncertainty-machine)'s cold water–throwing not without reason:
>On the internet, whole armies of crazies advanced their theories about the book.

My personal opinion on this renewed _I Ching_ craze is that any serious result in "applied _I Ching_ studies"---if that's a well-defined area of study at all---must be based on scholarly team effort rather than merely enthusiastic surmise. Former President of Peking University [Hu Shih](https://en.wikipedia.org/wiki/Hu_Shih) (<span class="hanyu">胡適</span>) has a famous epithet regarding the methodology of learning: [Daring in putting forward hypotheses; careful in searching for proofs](http://readopac1.ncl.edu.tw/nclserialFront/search/summny_list.jsp?sysId=0005762457&dtdId=000040) (<a href="http://terms.naer.edu.tw/detail/1302054/?index=7"><span class="hanyu">大膽假設小心求證</span></a>). I find this a great criterion to follow, especially as we step into a zone as mysterious as the _I Ching_.

In the last years of his life, Confucius told his disciples that if he could live longer he'd devote his remaining time to the _I Ching_.
>The Master said, "If some years were added to my life, I would give five or ten to the study of the Yi, and then I might come to be without great faults."<br>
>(<span class="hanyu">子曰：「加我數年，五十以學易，可以無大過矣。」</span>)<br>
><span style="text-align: right; display: block;"> --- [Shu Er, The Analects](https://ctext.org/analects/shu-er) (<span class="hanyu">論語・述而</span>)</span>

Since the _I Ching_ has appealed to such great minds as Confucius, Leibniz, and Bohr, I imagine having a real understanding of it must be a highly illuminating experience. People tend to assume that such an old and mystical book must be all kinds of obscure, but that's not necessarily true. With the help of modern tools, either from mathematics (as in [this paper](https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1540-6253.1975.tb00366.x), [this website](http://yijing.co.uk/writing/index.html), and [this book](https://books.google.com/books/about/The_Symbols_of_Yi_King.html?id=8RrjngEACAAJ&source=kp_book_description)) or from linguistics (as in the current article), I believe a systematic rethinking of the old book of wisdom should be not only feasible but also fruitful.🙏

*-The End-*
