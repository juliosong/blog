---
title: "Generative grammar for <em>I Ching</em> divination (Part 2): Structure"
categories: [linguistics, metaphysics]
tags: [I Ching, divination, generative grammar]
header:
  overlay_image: /assets/images/iching.png
  show_overlay_excerpt: false
  image_description: "the eight trigrams of I Ching and the tai chi symbol"
  caption: "I Ching trigrams and the Tai Chi symbol (credit: <a href='https://commons.wikimedia.org/wiki/File:Pakua.svg' title='via Wikimedia Commons'>Benoît Stella alias BenduKiwi</a> / <a href='http://creativecommons.org/licenses/by-sa/3.0/'>CC BY-SA</a>)"
  teaser: /assets/images/iching.png
toc: true
---

In the [previous post]({{ site.baseurl }}{% post_url 2020-04-07-generative-grammar-of-i-ching-part1 %}) I introduced the historical and cultural background of the ancient Chinese divination book _I Ching_ 'the Classic of Changes'. In this post I go on to introduce the structural components of the _I Ching_'s symbolic system.

## Hexagrams
The _I Ching_ uses hexagrams to model situations in the universe. There are altogether sixty-four hexagrams, which allegedly cover everything a human may experience in his life. These also constitute the entire content of the book, with each hexagram taking up a chapter.

{% include figure image_path="/assets/images/sixty-four-hexagrams.png" alt="the sixty-four I Ching hexagrams" caption="<i>I Ching</i> hexagrams in King Wen's order (source: [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:King_Wen_(I_Ching).png))" %}

At the lowest structural level, **a hexagram is made up of two basic types of lines**, the solid or _yang_ line ⚊ and the broken or _yin_ line ⚋ (not sure why the unicode rendering of the two symbols look like underscores). These are called the two primary forces or _liang yi_ 'two modes' (<span class="hanyu">兩儀</span>). The building of hexagrams from yin and yang is essentially a matter of combinatorics (there's an entire [book](http://linguistics.berkeley.edu/~rscook/images/CCCprev/CCCprev.html) on this published by UC Berkeley). Since there are two basic line types, the number 64 is just 2<sup>6<sup>.

Each _I Ching_ hexagram is a complex symbol with multilayered structures.<a id="pritri"></a> The most salient structure is the stacking of two trigrams; for instance, ䷂ = ☵ + ☳. The trigrams, together with their basic meanings, are _I Ching_'s way of categorizing [various basic phenomena and relationships](https://en.wikipedia.org/wiki/Bagua#Trigrams). The archetypal or design category for the trigrams is that of nature, in which the eight trigrams respectively represent heaven, lake, fire, thunder, wind, water, mountain, and earth (in Fuxi's order).<a id="arche"></a>

| Trigrams |  ☰ | ☱	| ☲	| ☳	| ☴	| ☵	| ☶	| ☷ |
| ------- | :-: |:-: |:-: |:-: |:-: |:-: |:-: |:-: |
| _Nature_ | 🌌| 🏖|🔥|⚡️|🌪|💦|⛰|🌏|

## Trigrams
Like the hexagrams, the trigrams are also made up of the two primary forces, hence their total number 8 (2<sup>3</sup>). The sixty-four hexagrams can thus be alternatively conceived as 8×8 (instead of 2<sup>6</sup>). There's also an alternative (and more dynamic) way to derive the eight trigrams---by successively dividing the initial, biggest category of the universe (called the [_tai chi_](https://en.wikipedia.org/wiki/Tai_chi) <span class="hanyu">太極</span> and variously translated as the Great Primal Beginning or the Supreme Ultimate) into two subcategories. The Confucian commentaries contain a famous quote about this:
>There is in the Changes the Great Primal Beginning. This generates the two primary forces. The two primary forces generate the four images. The four images generate the eight trigrams.<br>
>(<span class="hanyu">易有太極，是生兩儀，兩儀生四象，四象生八卦。</span>)<br>
><span style="text-align: right; display: block;"> --- [The Great Commentary](https://zh.wikisource.org/zh-hant/易傳/繫辭上#第十一章) (Wilhelm/Baynes' translation)</span>

<a id="tree"></a>
The process can be more clearly seen in a binary branching tree:
{% include figure image_path="/assets/images/bagua-binary-branching.png" alt="the generation of I Ching trigrams" caption="the generation of <i>I Ching</i> trigrams via successive category division" %}

The binary division of the _tai chi_ can in principle go on forever, but King Wen thought the sixty-four hexagrams were already enough to cover all situations in the universe. There have been attempts in history to continue the division. One such attempt is found in [_Jiaoshi yilin_](https://en.wikipedia.org/wiki/Jiaoshi_Yilin) 'Forest of Changes of the Jiao Clan' (<span class="hanyu">焦氏易林</span>) (the book surprisingly exists on [Amazon](https://www.amazon.com/Forest-Changes-Dynasty-Divination-Manual/dp/1505566843?ie=UTF8&refRID=S42DN9QS5EK0R96BB98Q&ref_=pd_ybh_a_1) in English), authored by Jiao Gong (<span class="hanyu">焦贛</span>) in the first century B.C.E. Jiao's book contains altogether 4096 (64×64) twelve-line diagrams, each consisting of two stacked hexagrams. However, it is difficult to see the usefulness of further extensions like this, as [Zhu Xi](https://en.wikipedia.org/wiki/Zhu_Xi) (1130–1200 C.E.) commented in [_Yixue qimeng_](https://www.itsfun.com.tw/易學啟蒙/wiki-610739-654688) 'Introduction to the Study of the Changes'.
>If from the 12-line diagrams we continue generating odd and even lines, eventually we come to 24-line diagrams, for a total of 16,777,216 changes. Taking 4,096 and multiplying it by itself also gives this sum. Expanding this we do not know where it ultimately ends. Although we cannot see its usefulness, it is sufficient to show that the Way of Change is indeed inexhaustible.<br>
>(<span class="hanyu">若自十二畫上，又各生一奇一耦，累至二十四畫，則成千六百七十七萬七千二百一十六變，以四千九十六自相乘，其數亦與此合。引而伸之，蓋未知其所終極也。雖未見其用處，然亦足以見易道之無窮矣。</span>)<br>
><span style="text-align: right; display: block;"> --- [_Yixue qimeng_](https://www.eee-learning.com/book/4714), pp.<a href="https://www.eee-learning.com/eeebook/middleyi/1951.png">26</a>–[27](https://www.eee-learning.com/eeebook/middleyi/1952.png) ([Adler's translation](https://www2.kenyon.edu/Depts/Religion/Fac/Adler/Writings/Qimeng-3.pdf))</span>

## Old and young
The design of the _I Ching_ system is such that each symbol at each level of the binary branching tree has a dedicated name; that is, each available symbolic category is actually used in divination. The names of the eight trigrams were shown in the [previous post]({{ site.baseurl }}{% post_url 2020-04-07-generative-grammar-of-i-ching-part1 %}#bagua), and the names of the sixty-four hexagrams are simply the chapter names of the _I Ching_. As to the four images, they are respectively named _old yang_ (⚌), _young yang_ (⚍), _old yin_ (⚏), and _young yin_ (⚎). The two young images are in a stable state whereas the two old images are unstable and about to change to their opposite forces. Importantly, the transition between yin and yang is gradual rather than discrete, as can be clearly seen in the [_tai chi liang yi tu_](https://en.wikipedia.org/wiki/Taijitu) 'picture of the great ultimate and the two primary forces' (<span class="hanyu">太極兩儀圖</span>), where the young forces are slimmer than the old forces and the old forces carry "embryos" of the opposite forces.

{% include figure image_path="/assets/images/yin-yang.png" alt="the picture of the great ultimate and the two primary forces" caption="the picture of the great ultimate and the two primary forces" %}

The names of the four images are also used to distinguish the four types of lines referenced in _I Ching_ divination; that is, the two basic lines (young) plus two changing or moving lines (old). The moving lines are important because they are what give rise to hexagram changes.

## Hexagram generation
As I mentioned in the [previous post]({{ site.baseurl }}{% post_url 2020-04-07-generative-grammar-of-i-ching-part1 %}#method), there are two main methods of generating natural numbers in _I Ching_ divination: the older yarrow stalk method and the simpler three-coin method. I won't go into the step-by-step procedures here; see the following sources if you're interested.
- Online resources:
  + Wikipedia: [I Ching divination](https://en.wikipedia.org/wiki/I_Ching_divination)👌
  + [Consult the _I Ching_ with yarrow stalks](https://www.instructables.com/id/Consult-the-I-Ching-with-Yarrow-Stalks/)👍
  + www.ich-ng.com: [yarrow stalk method](https://www.ichi-ng.com/divination/divination-yarrow-stalks/), [coin method](https://www.ichi-ng.com/divination/three-coins/)👍
  + [_I Ching_ divination part 2: casting the hexagram](https://divinationlessons.wordpress.com/2020/01/17/i-ching-divination-part-2-casting-the-hexagram/)
  + [How to consult the _I Ching_](https://divination.com/how-to-consult-the-i-ching/)
  + [_I Ching_ reading: a step-by-step guide](https://exemplore.com/fortune-divination/I_Ching_divination)
- Books (translations of the _I Ching_ with divination guidance):
  + [Baynes' translation](https://www.amazon.com/I-Ching-Book-Changes/dp/B000J4GE6Q) from [Wilhelm's German edition](https://www.amazon.com/Ging-Das-Buch-Wandlungen-German-ebook/dp/B00ECC5X36/ref=sr_1_1?dchild=1&keywords=Wilhelm+i+ging&qid=1586921045&s=books&sr=1-1)👍<br>
  (full text available at [iching-online.com](https://www.iching-online.com/hexagrams/))
  + [Legge's translation](https://www.amazon.com/I-Ching-Book-Changes/dp/B000JJI0TA/ref=sr_1_1?dchild=1&keywords=I+Ching+James+lege&qid=1586952431&sr=8-1)👌
  + [A translation based on Wang Bi's interpretation](https://www.amazon.com/Classic-Changes-Translation-Interpreted-Translations/dp/0231082959/ref=sr_1_1?dchild=1&keywords=The+Classic+of+Changes%3A+A+New+Translation+of+the+I+Ching+as+Interpreted+by+Wang+Bi&qid=1586920643&s=books&sr=1-1)
  + [A translation by the Eranos Project](https://www.amazon.com/Original-Ching-Oracle-Book-Changes-ebook/dp/B0782ZYJ3N/ref=sr_1_2?dchild=1&keywords=the+original+I+Ching+oracle&qid=1586921019&s=books&sr=1-2)
  + [A Chinese-born Taoist master's translation](https://www.amazon.com/Complete-Ching-Anniversary-Definitive-Translation-ebook/dp/B004GEAWQS/ref=sr_1_1?dchild=1&keywords=the+complete+I+Ching+huang&qid=1586921255&s=books&sr=1-1)
  + [A more scholarly translation by a Chinese Literature PhD](https://www.amazon.com/Original-Ching-Authentic-Translation-Changes-ebook/dp/B0078XFUJS/ref=sr_1_fkmr0_1?dchild=1&keywords=The+Original+I+ching%3A+an+Authentic+Translation+of+the+Book+of+Changes%2C+Based+on+Recent+Discoveries.&qid=1586922604&s=books&sr=1-1-fkmr0)

{% include figure image_path="/assets/images/wilhelm-i-ching.png" alt="the cover of Wilhelm's German translation of the I Ching" caption="Wilhelm's influential German translation of the _I Ching_ (picture: my copy)" %}

What I'd like to introduce here is how to build hexagrams from random numbers. Imagine we've followed either method above and gotten six whole numbers between 6 and 9 (inclusive)---note that **these are the only possibilities if we've followed the divination procedure correctly**. I write the six numbers in a [tuple](https://en.wikipedia.org/wiki/Tuple) because the order in which they are obtained matters. Below is an example.
```
tuple1 = (6, 7, 8, 9, 8, 7)
```
The six numbers in the tuple correspond to the six lines in a hexagram *from bottom up* (the direction is important). The mapping between the two obeys four rules. For each number in the 6-tuple:
- draw a broken line (⚋) if the number is 6 or 8;
- draw a cross (&#10005;) over the broken line if it is 6;     
- draw a solid line (⚊) if the number is 7 or 9;
- draw a circle (&#9711;) over the broken line if it is 9.

The hexagram thus generated is the _present hexagram_. It is one half of our divination basis; to get the other half we need to follow two more rules. For each line in the present hexagram:
- change it from broken to solid if it has a cross;
- change it from solid to broken if it has a circle.

Applying these two rules to the entire hexagram will give us a new hexagram, which is called the _future hexagram_. If there are no 6s or 9s in the present hexagram, then the present hexagram itself forms the divination basis. As an example, `tuple1` gives rise to the following two hexagrams:

```
present_hexagram1 = ䷿
future_hexagram1 = ䷨
```
In case the unicode hexagrams are a bit too tiny to be legible, I've created a magnified illustration of the mapping process.👇<a id="weichi"></a>
{% include figure image_path="/assets/images/tuple-hexagram.png" alt="mapping from tuple to hexagram" caption="A 6-tuple is mapped to two hexagrams in <i>I Ching</i> divination (from bottom up)." %}

([link to part 3]({{ site.baseurl }}{% post_url 2020-04-13-generative-grammar-of-i-ching-part3 %}))
