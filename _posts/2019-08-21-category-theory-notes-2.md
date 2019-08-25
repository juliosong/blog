---
title: "Category theory notes 2: What's a _category_?"
categories: [linguistics, mathematics]
tags: [category theory]
header:
  overlay_image: /assets/images/sky.jpg
  show_overlay_excerpt: false
  image_description: "A photo I took from the window of a plane."
  caption: "I took this photo from the window of a plane in 2014."
  teaser: /assets/images/sky.jpg
---

The term _category_ is anything but unfamiliar to linguisticians. Human language is all about categories. For example, speech sounds are grouped into various [natural classes](https://en.wikipedia.org/wiki/Natural_class), words are assigned different [parts of speech](https://en.wikipedia.org/wiki/Part_of_speech), sentences fall in several structure- or purpose-based [types](https://en.wikipedia.org/wiki/Sentence_(linguistics)#Classification), and discourses have numerous formality levels or [registers](https://en.wikipedia.org/wiki/Register_(sociolinguistics)).

_Category_ is also a common word in our everyday vocabulary. It's labeled B2-level in the [Cambridge Dictionary](https://dictionary.cambridge.org/dictionary/english/category) and defined as "(in a system for dividing things according to appearance, quality, etc.) a type, or a group of things having some features that are the same." [Merriam-Webster](https://www.merriam-webster.com/dictionary/category) similarly defines it as "any of several fundamental and distinct classes to which entities or concepts belong."

## Why are mathematical categories called categories?
The linguistic and dictionary senses of _category_ sound close to each other, but why are mathematical categories also called categories? What do they have to do with the familiar sense of the word _category_?  I've raised the question to a few categorists, and the experts' answers range from "little" to "nothing." The common sense is that it's just a term chosen by mathematicians.

That indeed is the case if we look at the definition of a mathematical category: <a id="catdef"></a>
>A _category_ $C$ consists of a class of _objects_ $ob(C)$ and a class $hom(C)$ of _morphisms_ between the objects, such that for every three objects $a, b, c$ there is a binary operation $hom(a,b) \times hom(b,c) \rightarrow hom(a,c)$ called _composition_, which satisfies two axioms _associativity_ and _identity_. ([Wikipedia](https://en.wikipedia.org/wiki/Category_(mathematics)#Definition))

It's so not familiar!

However, as a linguistician I'm naturally curious about the layers of meanings behind words. **I believe each term is chosen for a reason.** If a seemingly self-defining term clearly overlaps in form with some other established, familiar term(s), then the relevant terms most likely also somehow overlap in meaning. There are probably some shared characteristics between the relevant concepts, which when investigated further may reveal deeper cross-disciplinary connections. Actually one of the inventors of category theory, [Saunders Mac Lane](https://en.wikipedia.org/wiki/Saunders_Mac_Lane), notes on pages 29--30 of [_Categories for the Working Mathematician_](https://books.google.co.uk/books?id=MXboNPdTv7QC&source=gbs_navlinks_s) (CWM) that the term _category_ had been "purloined" from Aristotle and Kant. Now that's something we can further look up.

## Philosophers' categories
**Ancient philosophers' uses of the term _category_ often have linguistic bases.**  Aristotle's categories, as introduced in the [_Categories_](https://en.wikipedia.org/wiki/Categories_(Aristotle)) (_Κατηγορίαι_), are obviously linguistically oriented; it's essentially a semantic classification of subjects and predicates. The following quote is from [Ackrill's English translation](https://global.oup.com/academic/product/categories-and-de-interpretatione-9780198720867?cc=gb&lang=en&) via [Wikipedia](https://en.wikipedia.org/wiki/Categories_(Aristotle)#The_praedicamenta):
>Of things said without any combination, each signifies either substance or quantity or qualification or a relative or where or when or being-in-a-position or having or doing or being-affected. To give a rough idea, examples of substance are man, horse; of quantity: four-foot, five-foot; of qualification: white, grammatical; ....

Kant's categories are also highly linguistic in nature. According to [Wikipedia](https://en.wikipedia.org/wiki/Category_(Kant)), he writes in [_Critique of Pure Reason_](https://en.wikipedia.org/wiki/Critique_of_Pure_Reason) (_Kritik der reinen Vernunft_) that categories are "pure cоncepts of the undеrstanding which apply to objects of intuition in general" (Werner S. Pluhar's [translation](https://books.google.co.uk/books?id=Iz1xiAIcWiMC&dq=isbn:0872202577&source=gbs_navlinks_s)) and calls them "ontological predicates" in [_Critique of Judgement_](https://en.wikipedia.org/wiki/Critique_of_Judgement) (_Kritik der Urteilskraft_). There are twelve categories in Kant's system, which are divided into four major classes:
1. **Quantity:** unity, plurality, totality
2. **Quality:** reality, negation, limitation
3. **Relation:** substance and accident, cause and effect, reciprocity
4. **Modality:** possibility, existence, necessity

Since Kant believes such pure concepts are an a priori part of human mind, his approach to categories has been labeled "[conceptualist](https://plato.stanford.edu/entries/categories/#KanCon)." And since the Kantian categories are inherent in and modeled by verbal statements, they are "related only to human language" ([Wikipedia](https://en.wikipedia.org/wiki/Category_(Kant)#Meaning_of_.22category.22)).

## Mathematical categories are just... categories
The philosophical _category_ is not too distant in meaning from the linguistic/dictionary sense of the word. They just differ in **abstraction level.** For most everyday/linguistic scenarios any particular class of similar objects can be called a category, whereas in philosophy (at least for Aristotle and Kant) only "the highest genera of entities"---namely, the ultimate abstractions of human cognition---are called categories ([Stanford Encyclopedia of Philosophy](https://plato.stanford.edu/index.html)). In fact this already resembles the mathematical category. The following quote is from [Wikipedia](https://en.wikipedia.org/wiki/Category_(mathematics)):
>Category theory ... seeks to generalize all of mathematics in terms of categories .... Virtually every branch of modern mathematics can be described in terms of categories, and doing so often reveals deep insights and similarities between seemingly different areas of mathematics.

So, in a sense, **the mathematical category and the philosophical category are parallel notions**---both seek an ultimate, universal "template" for the field of inquiry, a template for which everything else can be viewed as a total or partial instantiation. As such, both the mathematical and the philosophical category have narrower meanings than the linguistic category, and all three disciplinary categories are narrower in meaning than the dictionary category. _Category_ is such a busy term!🗣

**Mathematical categories are called categories because they are cognitively just categories.**
{: .text-center .notice}

I've found the following remark from Goldblatt's [_Topoi: The Categorial Analysis of Logic_](https://books.google.co.uk/books/about/Topoi.html?id=5qTvoAEACAAJ&source=kp_book_description&redir_esc=y) (henceforth _Topoi_) illuminating, which by the way is a textbook I highly recommend.
>We may thus regard the broad mathematical spectrum as being blocked out into a number of "subject matters" or categories .... Category theory provides the language for dealing with these domains and for developing methods of passing from one to the other. (p.&nbsp;1)

**For Goldblatt a mathematical category is just a subarea of mathematics, and category theory itself is just the theory about the division of mathematics into subareas.** It turns out to be also applicable to such divisions in other disciplines or even to the division of human knowledge as a whole; but all the particular "blocks," when examined with sufficient abstraction, are just instantiations of the abstract notion "category."

More specifically, _category_ is used for both the abstract metatheoretical notion and its various specific instantiations (e.g., $\mathbf{Set}, \mathbf{Pos}, \mathbf{Mon}$), just as _language_ is used for both the general verbal capacity of Homo sapiens and its thousands of instantiations (e.g., English, Chinese, French).

## Two angles to characterize _category_
In the above we have actually seen two angles to characterize the mathematical category. The <a href="#catdef">technical definition</a> is what I call an _insider's characterization;_ namely, a definition developed by mathematicians for mathematicians.

The more big-picture-oriented remark from Goldblatt, on the other hand, is an *outsider's characterization;* namely, the definition one gets when jumping out of the box termed mathematics and perceiving the matter from a general epistemic height.

I personally have found it easier for the mathematically uninitiated (aka myself) to approach category theory with an outsider's mindset, at least at first. Even after one becomes versed enough to deal with the technical details, it's still helpful to think about the big picture from time to time.

## Conclusion
In this post I have noted down my thoughts on why the mathematical category is called _category_.

- The official answer is that the term is borrowed from philosophy.
- Both philosophers and mathematicians use _category_ to mean a most general "template."
<!-- - The philosophers' categories are more linguistically based while the mathematicians' categories are more cognized as blocks divided from the disciplinary spectrum.-->
- Categories in linguistics are defined much more casually than those in philosophy and mathematics and much closer to the ordinary, dictionary sense of _category_.
- The mathematical category can be characterized from an insider's angle or an outsider's angle. The latter is more helpful if you're a total beginners from humanities and want to quickly understand the purpose of category theory.
