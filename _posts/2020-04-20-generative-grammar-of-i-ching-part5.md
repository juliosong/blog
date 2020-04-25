---
title: "Generative grammar for <em>I Ching</em> divination (Part 5): Linguistics I"
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

The original motivation for this article was an occasional idea about the similarity between _I Ching_ divination and transformational-generative grammar. I ended up using four out of the total six posts to introduce the _I Ching_ because I wanted to present a fuller picture of its content and philosophy before comparing it with something apparently orthogonal to it in the public's eyes (aka science vs. superstition). I hope that reading has been fun---that is, if you haven't skipped the previous posts. But if you have, I hope you'll enjoy this one and the next.😃

Quick links: [Part 1]({{ site.baseurl }}{% post_url 2020-04-07-generative-grammar-of-i-ching-part1 %})&nbsp;&nbsp;[Part 2]({{ site.baseurl }}{% post_url 2020-04-10-generative-grammar-of-i-ching-part2 %})&nbsp;&nbsp;[Part 3]({{ site.baseurl }}{% post_url 2020-04-13-generative-grammar-of-i-ching-part3 %})&nbsp;&nbsp;[Part 4]({{ site.baseurl }}{% post_url 2020-04-17-generative-grammar-of-i-ching-part4 %})&nbsp;&nbsp;[Part 5]({{ site.baseurl }}{% post_url 2020-04-20-generative-grammar-of-i-ching-part5 %})&nbsp;&nbsp;[Part 6]({{ site.baseurl }}{% post_url 2020-04-23-generative-grammar-of-i-ching-part6 %})

## Transformational-generative grammar
[Transformational-generative grammar](https://en.wikipedia.org/wiki/Transformational_grammar), or simply generative grammar/syntax as it's more commonly called today (despite the [inaccuracy](https://linguistics.stackexchange.com/a/30431)), is a linguistic theory put forward by [Noam Chomsky](https://en.wikipedia.org/wiki/Noam_Chomsky) in the 1960s. It has become a mainstream theoretical school in linguistics (especially in the study of [syntax](https://en.wikipedia.org/wiki/Syntax)) since then as well as gone through several major shifts (currently in the shape of "[minimalism](https://en.wikipedia.org/wiki/Minimalist_program)"), though the basic idea hasn't changed that much---both the earliest "[standard theory](https://en.wikipedia.org/wiki/Generative_grammar#Standard_theory_(1957–1965))" and the latest minimalism derive sentences by building up hierarchical structures and manipulating them via form-changing operations (i.e., transformations). For example, to derive the English sentence _What did you eat?_ a generative syntactician would
1. postulate a set of ground terms (either concrete or abstract),
2. combine them into a hierarchically organized complex term step by step (Chomsky insists on [binary combination](https://en.wikipedia.org/wiki/Merge_(linguistics))), and
3. do something to that complex term along the way.<a id="code"></a>

<div style="padding-left:20px; padding-right:20px; padding-top:20px; padding-bottom:20px; margin-bottom: 30px; display:block; background-color:#eff; font-family:monospace; font-size:80%;">
<span style="display:block; color:gray; padding-bottom:12px;"><i>In the illustration below ignore what the abstract terms v, T, and C mean and simply treat them as functional keywords. &ldquo;Did&rdquo; is not among the initial ground terms but only inserted later.</i></span>
Ground terms: {what, you, eat, <i>v</i>, T, C...}<br>
Step 1: [eat what]<br>
Step 2: [<i>v</i> [eat what]]<br>
Step 3: [you [<i>v</i> [eat what]]]<br>
...<br>
Step m: [C [T [you [<i>v</i> [eat what]]]]]<br>
...<br>
Step n: [what [T-C [you [<s>T</s> [<s>you</s> [<i>v</i> [eat <s>what</s>]]]]]]]<br>
...<br>
Final product: what did you eat<br>
</div>

This process is "transformational" in the sense that the initially assembled structure (e.g., `step m`) is substantially different from the post-manipulation structure (e.g., `step n`); the former is closer to the understood form while the latter is closer to the pronounced form. The two structures used to be called ["deep" and "surface" structures](https://en.wikipedia.org/wiki/Deep_structure_and_surface_structure) respectively but I guess nowadays no one uses those terms anymore, at least not in the spotlight.

## Syntax and semantics
A first similarity between transformational-generative grammar and _I Ching_ divination is that they both separate syntax from semantics. By syntax I mean term manipulation, such as concatenating them into a string or stacking them into a pile, and by semantics I mean the interpretation of syntactically manipulated objects.

The syntactic objects in linguistics are ground terms and bracketed hierarchical structures like those <a href="#code">above</a>, while those in _I Ching_ divination are lines, trigrams, and hexagrams. In linguistics every syntactic stage (i.e., every step in the derivation) has a semantic interpretation, either complete or partial. Similarly, every structural level in _I Ching_ divination has a corresponding interpretation.

<span style="font-family:serif; font-variant:small-caps; background-color:GoldenRod;">&nbsp;Example&nbsp;</span> &nbsp;The derivation stage `[eat what]` has an incomplete predicate-argument interpretation (i.e., an event of eating something); it's incomplete in that the eater is unspecified. Similarly, ☰ has an intrinsic meaning of 'heaven; strength', which is incomplete in that its upper/lower position is not yet specified (not until the whole hexagram is derived).

In linguistics the meaning of a sentence is built from meanings of its parts (this is known as the [principle of compositionality](https://en.wikipedia.org/wiki/Principle_of_compositionality)); in _I Ching_ the overall meaning of a hexagram can be deduced from meanings of its structural components. The latter isn't strictly compositional due to its divinatory nature, but the strategy is similar.

<span style="font-family:serif; font-variant:small-caps; background-color:GoldenRod;">&nbsp;Example&nbsp;</span> &nbsp;The meaning of the syntactic object `[eat what]` is built from the meanings of `eat` and `what`, <a id="sung"></a>and the meaning of the hexagram ䷅ (_sung_ 'conflict' <span class="hanyu">訟</span>) is largely deducible from the meanings of ☰ 'heaven; strength' and ☵ 'water; danger, guile'---someone who is cunning inside and strong outside tends to be quarrelsome according to the Confucian commentators.

## Derivation and transformation
In both transformational-generative grammar and _I Ching_ divination complex terms are derived from simple ones in two ways: combination and transformation.

In current transformational-generative grammar the combinatorial operation is called "[merge](https://en.wikipedia.org/wiki/Merge_(linguistics))," which takes two syntactic objects at a time and joins them together.
```
merge(eat, what) = [eat what]
merge(v, [eat what]) = [v [eat what]]
...
```
In _I Ching_ divination, on the other hand, individual lines are stacked on top of one another. Since this operation always increases the existing stack by one, it may as well be treated as a binary operation similar to the `push` operation in [programming languages](https://en.wikipedia.org/wiki/Stack_(abstract_data_type)).
```
push(⚊, []) = [⚊]
push(⚋, [⚊]) = [⚍]
push(⚋, [⚍]) = [☳]
...
```

Transformation is **the** operation that distinguishes transformational-generative grammar from other grammatical theories and _I Ching_ divination from other divination methods. Moreover, in both fields the transformation procedure is triggered by properties on ground terms---namely, lexical items in linguistics and lines in divination. In linguistics the distinctive properties of lexical items are called [features](https://en.wikipedia.org/wiki/Feature_(linguistics)); similarly, we can treat properties on _I Ching_ lines as their "features" (more on this later).

<span style="font-family:serif; font-variant:small-caps; background-color:GoldenRod;">&nbsp;Example&nbsp;</span> &nbsp;The functional keyword `C` in some English clauses bears a transformation feature---let's call it [attractive]---which draws other words---for example, the question word `what` and the keyword `T` (which by the way also bears a transformation feature)---from deeper down in the structure up to its own level, hence the inverted word order. Similarly, in _I Ching_ divination we can assume each changing line bears a transformation feature---call it [changing]---which converts the line to its opposite gender (e.g., ䷀ with a changing first line becomes ䷫).

{% include figure image_path="/assets/images/chien-kou-tree.png" alt="a syntactic tree with movement arrows and a pair of present-future I Ching hexagrams" caption="transformation in transformational-generative grammar and in _I Ching_ divination" %}

## Categories
Both transformational-generative grammar and _I Ching_ divination make heavy use of categories, and the categorial disciplines of the two systems have a number of similarities, two of which came to my mind immediately when I was preparing for the article, respectively regarding category formation and decomposition.

<span style="font-family:serif; font-variant:small-caps; background-color:GoldenRod;">&nbsp;Example&nbsp;</span> &nbsp;Every natural language word belongs to at least one category; for example, _dog_ is typically a noun and _run_ a verb. <a id="cat"></a>Every _I Ching_ symbol (hexagram, trigram, or line) defines a category of patterns or situations in the world; for example, the above-mentioned ䷀ (_ch'ien_ 'the Creative' <span class="hanyu">乾</span>) represents those highly powerful and creative situations (as it consists of purely yang energy).

### Category division
Categories in both generative grammar and _I Ching_ divination can be given a binary tree organization, where a broadest category is divided again and again into increasingly detailed subcategories. This in a sense reveals how an entire category inventory can be formed from scratch. I have presented the tree of _I Ching_ categories in [Part 2]({{ site.baseurl }}{% post_url 2020-04-10-generative-grammar-of-i-ching-part2 %}#tree). Below I put it next to a similar tree of syntactic categories adapted from [a paper by my PhD supervisors](https://www.researchgate.net/publication/283363230_Rethinking_Formal_Hierarchies_A_Proposed_Unification) (I use the big circle on top to represent the initial, undivided category space).

{% include figure image_path="/assets/images/trigram-vs-syntax.png" alt="binary category division in I Ching and in linguistics" caption="successive division of _I Ching_ categories and syntactic categories" %}

I guess the parallelism above isn't that exciting a discovery, because binary division is probably just how category formation works in the human mind in general, so it's no wonder that the same pattern shows up again and again in different domains of knowledge imagined by humans.

### Categorization
Another parallelism between the categorial discipline of transformational-generative grammar and that of _I Ching_ divination, which I find more special, concerns the intrinsic meanings of trigrams. I first mentioned this in [Part 3]({{ site.baseurl }}{% post_url 2020-04-13-generative-grammar-of-i-ching-part3 %}#intrinsic): the eight trigrams in the _I Ching_ have been associated with numerous meanings in numerous categories, but none of the specialized meanings of a trigram is a perfect candidate as its semantic core.

<span style="font-family:serif; font-variant:small-caps; background-color:GoldenRod;">&nbsp;Example&nbsp;</span> &nbsp;While the "lake" and "openness" meanings of ☱ _tui_ (<span class="hanyu">兌</span>) are conceptually related (a lake is an open area), neither is related to its "third daughter" meaning.

I concluded in Part 3 that the shared core of the multiple meanings of a trigram is none other than the trigram itself---namely, the visual form---detached from any concrete concept. This is reminiscent of a popular trend in transformational-generative grammar, especially in its [distributed morphology](https://en.wikipedia.org/wiki/Distributed_morphology#Derivation) branch, where words like _dog_ and _flower_ are not taken to be combinatorial atoms but assumed to have a derived status instead. They are derived from two more basic types of unit---a categorial keyword (e.g., noun, verb) plus a category-neutral "root." The root part is void of any concrete meaning (or pronunciation, for that matter) and only gets concretized via a special process called "categorization."

<span style="font-family:serif; font-variant:small-caps; background-color:GoldenRod;">&nbsp;Example&nbsp;</span> &nbsp;In distributed morphology _dog_ (the animal) is derived by combining a nominal categorizer _n_ with the root √DOG; the same root can be combined with a verbal categorizer _v_ and yield a verb (as in _he is dogged by bad health_). It just so happens that in English words sharing a single root often have the same form (hence the traditional term [zero derivation](https://en.wikipedia.org/wiki/Conversion_(word_formation))), but there are also languages where roots get distinct forms in distinct categories, such as _katab_ 'he wrote' and _miktab_ 'letter' in [Hebrew](https://en.wikipedia.org/wiki/Semitic_root), whose shared root is _k-t-b_ (the general phenomenon is called [root and pattern morphology](https://www.britannica.com/topic/root-and-pattern-system)).

Abstracting away from obvious differences (such as the fact that a linguistic root does define some sort of core meaning, albeit very vague), it feels like the trigram forms in the _I Ching_ are just roots of a certain kind---maybe we can call them visual roots---and a specialized trigram meaning is derived by combining such a root with a particular categorizer (such as _nature_ or _animal_).

<span style="font-family:serif; font-variant:small-caps; background-color:GoldenRod;">&nbsp;Example&nbsp;</span> &nbsp;The trigram root √☱ has no meaning of its own; it comes to mean "lake" when being combined with the categorizer _nature_ and "third daughter" when being combined with the categorizer _family_, which in turn define two intrinsic meanings for the trigram.

```
categorize(√DOG, n) = dog (the quadruped)
categorize(√DOG, v) = dog (the unpleasant action)
categorize(√☱, nature) = lake
categorize(√☱, family) = third daughter
```

The categorization of linguistic roots is verbally-conceptually based; for example, the root √DOG encodes the concept underlying both the quadruped _dog_ and the unpleasant action _to dog_. The underlying concept is highly nebulous or downright ineffable, but it has to be there, or we wouldn't be able to feel the conceptual connection between the two senses of the word form _dog_.

By contrast, the categorization of trigram roots isn't based on verbal concepts (or at least that's not a major factor at play), so the intrinsic meanings of a trigram needn't share a core concept. That's why a trigram root can link meanings as disparate as "lake" and "third daughter" together, which is not possible with linguistic roots.

Note that the above distinction doesn't make the parallelism between linguistic roots and trigram roots less real. It's just that linguistics and _I Ching_ divination are two totally different fields after all, and so one shouldn't expect their components to work in exactly the same way.🤷‍♂️

Also, I said <a href="#cat">above</a> that each _I Ching_ symbol was a category. That doesn't contradict my idea here that trigrams are categoryless roots, because these are two distinct perspectives and "category" is an extremely broad notion. Each trigram is a category in the sense that it groups a number of situations or patterns together, but those situations and patterns are precisely the intrinsic meanings of the trigram, which in turn are derived by combining the trigram root with the relevant categorizers.

So, a trigram-qua-category is actually the category of all categorized meanings of a trigram-qua-root; in other words, the trigram-qua-category and the trigram-qua-root define each other. We may therefore treat them as two sides of the same coin---all we need to beware of is that the "category" in trigram-qua-category and that in "categoryless root" aren't one and the same sort of category. What in the human world isn't a category after all?🌝

{% include figure image_path="/assets/images/trigram-root-category.png" alt="a trigram root and its related intrinsic meanings" caption="Categorized meanings of a trigram root together form a category defined by the root." %}

(Check out [my PhD dissertation](https://www.repository.cam.ac.uk/handle/1810/297789) if you're really into categories.)

([link to part 6]({{ site.baseurl }}{% post_url 2020-04-23-generative-grammar-of-i-ching-part6 %}))
