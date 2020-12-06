---
title: "Generative grammar for <em>I Ching</em> divination (Part 1): What's <em>I Ching</em>?"
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

Sometimes our brains make connections in unexpected ways. For instance, the other day I was thinking about [*I Ching*](https://en.wikipedia.org/wiki/I_Ching) (can't remember why), the ancient Chinese divination book, and an idea suddenly popped into my head: Isn't the procedural manipulation of symbols in the divination process a sort of syntactic derivation like that in [transformational-generative grammar](https://www.google.com/search?client=safari&rls=en&q=transformational-generative+grammar&ie=UTF-8&oe=UTF-8&safari_group=9)?

The more I thought about the idea, the more curious I got, so I decided to give it a go and see if I could describe _I Ching_ divination in linguistic terms---just for fun. This article is split into six parts:
- [Part 1: What's _I Ching_?]({{ site.baseurl }}{% post_url 2020-04-07-generative-grammar-of-i-ching-part1 %})
- [Part 2: Structure]({{ site.baseurl }}{% post_url 2020-04-10-generative-grammar-of-i-ching-part2 %})
- [Part 3: Meaning I]({{ site.baseurl }}{% post_url 2020-04-13-generative-grammar-of-i-ching-part3 %})
- [Part 4: Meaning II]({{ site.baseurl }}{% post_url 2020-04-17-generative-grammar-of-i-ching-part4 %})
- [Part 5: Linguistics I]({{ site.baseurl }}{% post_url 2020-04-20-generative-grammar-of-i-ching-part5 %})
- [Part 6: Linguistics II]({{ site.baseurl }}{% post_url 2020-04-23-generative-grammar-of-i-ching-part6 %})

Those who already know the basics of the _I Ching_ or are simply impatient can skip the first four parts and directly jump to [Part 5]({{ site.baseurl }}{% post_url 2020-04-20-generative-grammar-of-i-ching-part5 %}).

## The Classic of Changes
_I Ching_ or _Yijing_ (<span class="hanyu">易經</span>),<sup><a href="#fn1" id="ref1">1</a></sup> literally "the Classic of Changes," is the oldest and most important [classic text](https://en.wikipedia.org/wiki/Chinese_classics) in Chinese history. It's also simply (and sometimes preferably) called _I_ (pronounced "ee"), for its canonization as a _Ching_ 'classic text' (in 136 B.C.E.) only happened many centuries after its birth.

As its name suggests, the _I Ching_ is a book about changes. **It models the world in terms of transitions between [hexagrams](https://en.wikipedia.org/wiki/Hexagram_(I_Ching))**, which are little pictures made up of six solid or broken lines such as ䷂ and ䷄. I find the following words from [a divination website](https://divinationlessons.wordpress.com/2019/11/29/i-ching-divination-part-1/) a good summary.

>The I Ching’s operating principle is that **change is the one constant in life**, and that our lives are just a series of changes from one set of circumstances to the next.

## Authorship
The established form of the _I Ching_ is attributed to the [Duke of Zhou](https://en.wikipedia.org/wiki/Duke_of_Zhou) (11th century B.C.E.)---hence its other name _Zhou yi_ 'Changes of the Zhou Dynasty' (<span class="hanyu">周易</span>)<sup><a href="#fn2" id="ref2">2</a></sup>---but the core symbolic system of the book, including its [eight trigrams](https://en.wikipedia.org/wiki/Bagua#Fuxi_.22Earlier_Heaven.22) and [sixty-four hexagrams](https://en.wikipedia.org/wiki/List_of_hexagrams_of_the_I_Ching), is actually the work of the duke's father, [King Wen of Zhou](https://en.wikipedia.org/wiki/King_Wen_of_Zhou). King Wen, on the other hand, had built his work upon that of [Fuxi](https://en.wikipedia.org/wiki/Fuxi) (21st century B.C.E.), a legendary early ruler of the Chinese civilization. The major difference between King Wen's system and Fuxi's system lies in their different arrangements of the eight trigrams or [_bagua_](https://en.wikipedia.org/wiki/Bagua) 'eight gua' (<span class="hanyu">八卦</span>).
<a id="bagua"></a>
{% include figure image_path="/assets/images/fuxi-vs-kingwen.png" alt="fuxi's eight trigrams and king wen's eight trigrams" caption="Fuxi's &ldquo;Earlier Heaven&rdquo; arrangement (left) and King Wen's &ldquo;Later Heaven&rdquo; arrangement (right) of the eight trigrams (sources: Wikimedia Commons [1](https://commons.wikimedia.org/wiki/File:Bagua-name-earlier.svg) [2](https://en.wikipedia.org/wiki/File:Bagua-name-later.svg))" %}

<div style="padding-left:20px; padding-right:20px; padding-top:20px; padding-bottom:7px; margin-bottom: 30px; display:block; background-color:MintCream; font-family:Georgia; font-size:80%;">
<b>A linguistic aside:</b> The <i>I Ching</i> has influenced the root of the Chinese culture so deeply that many divination-specific terms in it have been fossilized in the Chinese language. For example, <i>bagua</i> is now <a href="https://en.wiktionary.org/wiki/八卦#Chinese">used figuratively</a> in everyday language to mean "gossip," "to gossip," or "gossipy."<br>

<ul>
<li><i>Tā shì yí gè fēicháng bāguà de rén.</i><br>
(<span class="hanyu">他是一個非常八卦的人。</span>)<br>
"He is a very gossipy person."</li>
</ul>
</div>

The authorship of the _I Ching_ is usually attached to all three historical/mythical figures mentioned above---together with the much younger [Confucius](https://en.wikipedia.org/wiki/Confucius) (551–479 B.C.E.), who allegedly had added the most important commentaries to the book (called the [Ten Wings](https://en.wikipedia.org/wiki/Ten_Wings)) and played a crucial role in its reclassification as a philosophical book. Luckily this reclassification hadn't taken immediate effect, though, because otherwise the _I Ching_ couldn't have survived [Qin Shi Huang](https://en.wikipedia.org/wiki/Qin_Shi_Huang)'s brutal policy of [burning philosophical books and burying Confucian scholars](https://en.wikipedia.org/wiki/Burning_of_books_and_burying_of_scholars) in 212–213 B.C.E.
>The content of the Changes is very deep. Its creation took the work of three sages [i.e., Fuxi, King Wen of Zhou, and Confucius] and spanned across three ancient ages [i.e., the Neolithic Age, the Bronze Age, and the Iron Age].<br>
>(<span class="hanyu">易道深矣，人更三聖，世歷三古。</span>)<br>
><span style="text-align: right; display: block;"> --- [Book of Han](https://en.wikipedia.org/wiki/Book_of_Han), [Vol. 30](https://zh.wikisource.org/zh-hant/漢書/卷030) (1st century C.E.)</span>

<a id="moment"></a>
## Divination
### Idea
The basic idea behind _I Ching_ divination is that **every moment in spacetime is an all-encompassing picture like a holographic screenshot**; everything in the moment, down to every trifling minutia (such as the occasional falling of leaves), is an indispensable piece in a unique jigsaw puzzle. As the Swiss psychiatrist [Carl Jung](https://en.wikipedia.org/wiki/Carl_Jung) comments in his foreword to Wilhelm/Baynes' translation of the _I Ching_, the ancient Chinese divination method is "more akin to the perception of a work of art." Jung further points out that the idea behind _I Ching_ divination is similar to his own idea of "[synchronicity](https://en.wikipedia.org/wiki/Synchronicity)"---the assumption that events that occur with no causal relationship yet seem to be meaningfully related are actually meaningful coincidences.
>[S]ynchronicity takes the coincidence of events in space and time as meaning something more than mere chance .... Just as causality describes the sequence of events, so synchronicity ... deals with the coincidence of events. ... [T]he sixty-four hexagrams of the _I Ching_ are the instrument by which the meaning of sixty-four different yet typical situations can be determined. These interpretations are equivalent to causal explanations.<br>
><span style="text-align: right; display: block;"> --- Foreword, [The I Ching or Book of Changes](https://books.google.com/books/about/The_I_Ching_or_Book_of_Changes.html?id=ExU6SjX97EwC&redir_esc=y)</span>

In a word, in the philosophy of the _I Ching_ there's no real randomness. The following book excerpt also well summarizes this philosophy:
>[T]he assumption of orthodox Western science that there is no meaning to be gleaned from random events was certainly not shared by the ancient Chinese. Their divinatory practices and their whole cosmology were based on a qualitative notion of time, in which all things happening at a given moment in time share some common features, are part of an organic pattern. Nothing therefore is entirely meaningless.<br>
><span style="text-align: right; display: block;"> --- [The Original I Ching Oracle](https://www.google.com/books/edition/_/JaMttAEACAAJ?hl=en&sa=X&ved=2ahUKEwjV2u-G0ufoAhU3HjQIHSQvArMQ7_IDMA96BAgMEAI), Chapter 1</span>

<a id="method"></a>
### Method
The screenshots of the spacetime moments can be observed from many angles---and for a higher-dimension creature they are indeed observable from every angle, and all at once. For us humans, however, such a bird's-eye view is unavailable; we can only get a glimpse of the bigger picture via some sort of trick. Our tricks will no doubt look primitive and clumsy in our higher-dimension friend's eyes, and they'll only show us a tiny tip of a colossal iceberg, but something is better than nothing!<sup><a href="#fn3" id="ref3">3</a></sup>

{% include figure image_path="/assets/images/i-ching-divination.png" alt="an illustration of a higher-dimension creature's perspective on an earthling's life" caption="A higher-dimension creature can readily see what we call &ldquo;the future.&rdquo;" %}

Each divination method offers its own horizon-broadening trick. The trick of the _I Ching_ is to generate [random numbers](https://www.freecodecamp.org/news/a-brief-history-of-random-numbers-9498737f5b6c/), either by [sorting fifty yarrow stalks](https://en.wikipedia.org/wiki/I_Ching_divination#Yarrow_stalks) or by [tossing three coins](https://en.wikipedia.org/wiki/I_Ching_divination#Coins). Between the two, the yarrow stalk method is the more traditional or "authentic," but it's also highly complex and ritualistic. By comparison, the three-coin method is much simpler and less demanding on materials, but it doesn't yield the same probability distribution as that in the yarrow stalk method (as to which number gets more chance to be generated). The following table is adapted from [Wikipedia](https://en.wikipedia.org/wiki/I_Ching_divination#Yarrow_stalks). (I'll explain what the numbers 6-8-9-7 mean in the next post.)

| Number | yarrow-stalk probability | three-coin probability |
| :-------: | :----------------------: | :--------------------: |
| 6   | 1/16 | 2/16 |
| 8 | 7/16 | 6/16 |
| 9  | 3/16 | 2/16 |
| 7 | 5/16 | 6/16 |

In the oldest _I Ching_ documents (such as the Confucian commentaries) only the yarrow stalk method is mentioned, but in fact both methods have been in frequent use throughout Chinese history. There are also improved coin methods that yield the same distribution of probabilities as that in the yarrow stalk method, such as the [two-coin method](https://en.wikipedia.org/wiki/I_Ching_divination#Two-coin_method), but those aren't used as widely as the three-coin method.

Based on the probability difference, [some people say](https://aleadeum.com/2013/07/12/the-i-ching-random-numbers-and-why-you-are-doing-it-wrong/) that the yarrow stalk method promotes yang or positive energy (e.g., action, imagination, creativity, strength) over yin or negative energy, while no such promotion exists in the three-coin method. But there are also [people who suggest](https://sabazius.oto-usa.org/probability-and-the-yi-jing/) that the probability difference isn't that big a deal if one believes in the _I Ching_ philosophy that nothing is truly random, because probability theory is only relevant when "the events in question are random."

Whichever method one chooses to use, **the goal of the trick is to impose some agency or subjectivity on the moment**. The random number–generating activity, as well as the will of the person who performs it, once initiated, becomes part of the moment. And the random numbers thus generated form a channel to "deduce" the bigger picture---via the _I Ching_ hexagrams.

([link to part 2]({{ site.baseurl }}{% post_url 2020-04-10-generative-grammar-of-i-ching-part2 %}))

<hr>
<div style="font-family: serif; font-size: 0.8em;">
<a id="fn1">1.</a><sup><a href="#ref1" title="Jump back to footnote 1 in the text.">↩</a></sup> <i>I Ching</i> is <a href="https://en.wikipedia.org/wiki/Wade–Giles">Wade-Giles</a> spelling (predominant in the nineteenth to twentieth century) and <i>Yijing</i> is <a href="https://en.wikipedia.org/wiki/Pinyin">pinyin</a> spelling (the current standard in the PRC).<br>
<a id="fn2">2.</a><sup><a href="#ref2" title="Jump back to footnote 2 in the text.">↩</a></sup> Note that <i>Zhouyi</i> is not the only or original version of <i>I</i>. However, with the two alternative and older versions, <i>Lianshan yi</i> &lsquo;changes of linked mountains&rsquo; and <i>Guicang yi</i> &lsquo;changes of returning to the hidden&rsquo; lost in pre-Zhou history (<a href='https://en.wikipedia.org/wiki/Guicang'>Wikipedia says</a> <i>Guicang</i> was rediscovered in 1993), <i>Zhouyi</i> became the only surviving version of the book. According to <a href='http://wenhousecrafts.com/iching/threeichings.htm'>this website</a> the three versions of <i>I</i> &ldquo;contemplate the universe from slightly different angles.&rdquo;<br>
<a id="fn3">3.</a><sup><a href="#ref3" title="Jump back to footnote 3 in the text.">↩</a></sup> The higher-dimension talk here isn't just rhetorical. There has been much interest in the <a href="http://www.secretsofcreation.com/yijing.html">mathematics</a> behind <i>I Ching</i> and, among others, a view that the <i>I Ching</i> system is essentially a <a href="https://www.quora.com/What-is-compositing-of-dimensions-and-how-is-it-used-in-mandalic-geometry/answer/Martin-Hauser">six-dimensional coordinate system</a>.
</div>
