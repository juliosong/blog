---
title: "Category theory notes 7: Categorical idioms"
categories: [linguistics, mathematics]
tags: [category theory]
header:
  overlay_image: /assets/images/sky.jpg
  show_overlay_excerpt: false
  image_description: "A photo I took from the window of a plane."
  caption: "I took this photo from the window of a plane in 2014."
  teaser: /assets/images/sky.jpg
---

Idioms and slangs are an important part of human language. They are short, expressive, and vividly reflect regional/historical mind-sets. And they are usually fun to learn! For example, I was rather amused by the English phrase _rain cats and dogs_ in elementary school; and I've also found the Cantonese name for elephants <span class="hanyu">大笨象</span> 'big silly elephant' adorable.

{% include figure image_path="/assets/images/idiom.jpg" alt="An illustration of two idioms" caption="An illustration of the English idiom <em>rain cats and dogs</em> and the Cantonese slang 大笨象<br>Source: [Pixabay](https://pixabay.com/), created by [OpenClipart-Vectors](https://pixabay.com/vectors/rainstorm-rain-cats-and-dogs-rain-156134/) and [andremsantana](https://pixabay.com/vectors/elephant-animal-jungle-savannah-1598359/)" %}

## What's wrong with idioms?
**There are also idioms in category theory, and it's super helpful for beginners to realize this from day one.** I had tried following textbooks line by line and word by word, but there were always a few recurring phrases that I found hard to understand or even parse, as if they were not written in grammatically felicitous English. Since mathematicians used them all the time and hardly any textbooks included them in their terminology lists, my linguistician's nerve told me they must be somewhat idiomatic within the field.

**The difficulty with idiomatic terms, just like that with everyday idioms, is that they can't be understood literally (i.e., compositionally).** For example, _rain cats and dogs_ doesn't mean cats and dogs are really falling from the sky, and Cantonese speakers surely don't really think elephants are silly. These are just metaphors instead, which are an important facet of human language and cognition.

{% include figure image_path="/assets/images/metaphor.jpg" alt="The cover of the book Metaphors We Live By" caption="The cover of Lakoff &amp; Johnson's monograph [_Metaphors We Live By_](https://books.google.co.uk/books?id=m8Sp5m9vZcwC&source=gbs_book_other_versions) (source: [Wikipedia](https://commons.wikimedia.org/wiki/File:Metaphors_We_Live_By_book_cover.jpg))" %}

Due to their unpredictable meanings, idioms require extra efforts in language acquisition. Sadly, unlike language textbooks, mathematical textbooks rarely specify which phrases are idiomatic, let alone explicitly explain their meanings. This is not ideal, because it means that **readers can only grasp idiomatic terms through experience, which total beginners don't have any.**

What's worse, a large number of math learners aren't native speakers of English, who might have difficulty in understanding even everyday English idioms, let alone scholarly ones. Therefore, I generally object to the coinage or standardization of idiomatic terms in academic contexts, especially when the relevant phrases can also be understood literally (that is, falsely).

**To avoid unnecessary linguistic barriers, academic terms should be maximally compositional.**
{: .text-center .notice}

## Two categorical idioms
Nevertheless, since all human knowledge---including mathematics---must be recorded and passed on in human tongues, convention frequently overpowers rationality in verbal communication. This is just part of human nature. Since we can hardly do anything about it, we'd better be more sensitive and learn idioms in the idiomatic way; namely, by rote. In particular, I've found the following two idiomatic expressions useful to know at the beginning stage of category theory learning.

### 1. _up to (unique) isomorphism_
This phrase actually involves two closely related expressions: _up to isomorphism_ and _up to unique isomorphism_. When I first met it I had already learned what an isomorphism was; I also knew what _up to_ meant in everyday English. But I couldn't figure out what the combination was supposed to mean. Tai-Danae Bradley similarly "complains" in her [blog post](https://www.math3ma.com/blog/up-to-isomorphism) that "'[u]p to isomorphism' is a phrase that seems to get thrown around a lot without ever being explained."

As a linguistician, when I see a word or phrase I don't understand, the first thing I do is turn to dictionaries. So, [Merriam-Webster](https://www.merriam-webster.com/dictionary/up%20to) lists two definitions for the phrasal preposition _up to_:

>(1) used as a function word to indicate extension as far as a specified place<br>
>e.g., _sank **up to** his knees in the mud_<br>
>(2) used as a function word to indicate a limit or boundary<br>
>e.g., _**up to** 50,000 copies a month_, _worked **up to** the last minute_

However, neither dictionary definition fits in the mathematical phrase in any self-evident way. Isomorphism surely isn't "a specified place" like knees, but nor does it sound like "a limit or boundary." So, there must be something left implicit---that is, hidden behind the words---by the inventor of the phrase.

As it turns out, **the phrase actually means "as far as isomorphism allows" or "by way of isomorphism."** It's usually used to modify propositions of the pattern
- _X and Y are the same **up to isomorphism**,_

which means that _X_ and _Y_ aren't exactly the same but can be taken as the same in category theory because they are isomorphic. In other words, **_up to isomorphism_ is an adverbial specifying a condition under which the proposition is true.** So, the above pattern can be paraphrased as _X and Y, being isomorphic, are the same if we treat isomorphic constructs as the same._ In category theory two constructs that are isomorphic behave identically in whatever way that matters to the theory. In [Bradley's words](https://www.math3ma.com/blog/up-to-isomorphism):
>[W]e say two groups (or any other algebraic structures) are the same "up to isomorphism" if they're isomorphic! In other words, they share the exact same structure and therefore they are essentially indistinguishable. Hence we consider them to be one and the same!

Sometimes the phrase is also used in the pattern _X is unique **up to isomorphism**_, which, following our above explication, simply means "X is unique if we view isomorphic constructs as one and the same." Goldblatt has an illuminating explanation in [_Topoi_](https://books.google.co.uk/books/about/Topoi.html?id=5qTvoAEACAAJ&source=kp_book_description&redir_esc=y):
>Within any mathematical theory, isomorphic objects are indistinguishable in terms of that theory. ... An object will be said to be "unique up to isomorphism" in possession of a particular attribute if the only other objects possessing that attribute are isomorphic to it. A concept will be "defined up to isomorphism" if its description specifies a particular entity, not uniquely, but only uniquely up to isomorphism. (p.&nbsp;42)

In sum, **the idiom _up to isomorphism_ essentially reflects the externally oriented approach pursued in category theory,** whereby a construct can be completely defined and identified by how it interacts with other constructs, without reference to its internal makeup (which in turn can be ignored when comparing constructs).

After the above discussion, now the meaning of _up to unique isomorphism_ should also be clear---it simply means that the isomorphism in question is unique; namely, there's only one isomorphism. So, whenever the textbook says _up to unique isomorphism_ we can replace it by _up to isomorphism_ (but not vice versa!), because the condition for the proposition the adverbial modifies is merely **an** isomorphism.

The phrase _up to unique isomorphism_ is usually used in propositions related to [_universal properties_](https://en.wikipedia.org/wiki/Universal_property) or [_universal constructions_](https://ncatlab.org/nlab/show/universal+construction). For example, a [_terminal object_](https://ncatlab.org/nlab/show/terminal+object) in any category, if it exists, is unique up to unique isomorphism. A terminal object by definition is an object to which there's a unique arrow from any object in the same category, like this (I have highlighted the terminal object in red and omitted all irrelevant arrows):

![one terminal object](\assets\images\terminal-1.png)

This means that if there are two terminal objects in the category, the diagram should look like this:

![two terminal objects](\assets\images\terminal-2.png)

In particular, there are a pair of back-and-forth arrows between the two red-colored terminal objects, which together define two composite loop arrows $!g\circ!f$ and $!f\circ!g$. However, since there is exactly one arrow to a terminal object from **any** object, including the terminal object itself, we must have $!g\circ!f=id_1$ and $!f\circ!g=id_2$; that is, $!f$ and $!g$ form an isomorphism. Hence, the two red objects are indistinguishable from a category-theoretic perspective, and for the category in question its terminal object is "unique up to unique isomorphism."

### 2. _have (all) products/coproducts/exponentials_

The second categorical idiom that I've found useful to know as a beginner is _have (all)_, where _all_ is optional, as in _the category $\mathbb{C}$ has (all) products_ and _the category $\mathbb{D}$ has (all) exponentials_. For example, Awodey (2010) defines a [_cartesian closed category_](https://en.wikipedia.org/wiki/Cartesian_closed_category) as follows:
>A category is called cartesian closed, if it has all finite products
and exponentials. ([_Category Theory_](https://global.oup.com/ukhe/product/category-theory-9780199237180?cc=gb&lang=en&), p.&nbsp;122)

Similarly, Goldblatt defines an [_elementary topos_](https://ncatlab.org/nlab/show/elementary+%28infinity%2C1%29-topos) as follows:
>An elementary topos is a category $\mathbb{C}$ such that (1) $\mathbb{C}$ is finitely complete, (2) $\mathbb{C}$ is finitely co-complete, (3) $\mathbb{C}$ has exponentiation, (4) $\mathbb{C}$ has a subobject classifier. ([_Topoi_](https://books.google.co.uk/books/about/Topoi.html?id=5qTvoAEACAAJ&source=kp_book_description&redir_esc=y), p.&nbsp;84)

But what do "has all finite products and exponentials" and "has exponentiation" mean? I don't think I've ever seen the verb _have_ and the quantifier _all_ being used together like this in everyday English. I mean, I've seen expressions like _have all the luck_ and _have all the cards_, but _all_ always precedes a definite noun phrase _the NP_. And Goldblatt's "has exponentiation" is even worse. It sounds terribly like an existential quantification (i.e., "there exists exponentiation in the category") when it's actually synonymous with Awodey's apparently universal quantification "has all ... exponentials."

After being exposed to category theory for some time, I finally realized that **the phrase _have (all) X_ really means "X exists for all objects or suitable object combinations in a category."** Thus, Awodey's definition of a cartesian closed category really says "a category is called cartesian closed if for any pair of objects in it there exists a product object and an exponential object based on them in the category." And the third condition in Goldblatt's definition of an elementary topos really says "for any pair of objects in $\mathbb{C}$ there exists an exponential object based on them in $\mathbb{C}$."

In other words, in _have all X_ the quantifier _all_ doesn't modify X at all but modifies an implicit, separate noun phrase "(pairs of) objects in the category." But how are inexperienced pupils, especially those without expert guidance, supposed to know this?! 😵

{% include figure image_path="/assets/images/frustrated.png" alt="A frustrated student in front of a desktop" caption="I felt like this when I first met the _has (all)_ expressions. (source: [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Frustrated_Cartoon_Guy_Using_A_Computer.svg))" %}

## Takeaway
- There are idiomatic terms in category theory, some of which are important.
- The phrase _up to (unique) isomorphism_ means "by way of isomorphism" or "if we view isomorphic constructs as the same."
- The phrase _have (all) X_ means "X exists for all (pairs/tuples of) objects in the category."
- Since idiomatic terms are beginner- and foreigner-unfriendly, they should either be accompanied by nonidiomatic explanations or better avoided in formal definitions.
