---
title: "Another application of category theory in linguistics (Part 1)"
categories: [linguistics, mathematics]
tags: [category theory, generative grammar]
header:
  overlay_image: /assets/images/act2022.png
  show_overlay_excerpt: false
  image_description: "a Rubik's cube"
  caption: "credit: [Kenny Eliason](https://unsplash.com/@neonbrand?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/smart?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)"
  teaser: /assets/images/act2022.png
toc: true
toc_sticky: true
---

This post is part of my portfolio for the poster session at the Applied Category Theory 2022 conference ([ACT2022](https://msp.cis.strath.ac.uk/act2022/index.html)). It is a gentle introduction to my application of the monad tool from category theory to theoretical linguistics, more specifically to the "root syntax" area thereof. The main result of my study can be summarized by the following slogan:

> If we take lexical decomposition in morphosyntax seriously, then monadic composition is everywhere in human language semantics.

In this post, I will clarify what my study is about in informal terms, paying special attention to (inter)disciplinary contextualization. NB this is all work in progress, and I'm yet to write a fully detailed article on the topic. But if you are interested, below are some preliminary published materials:
1. a [proceedings paper](https://www.juliosong.com/doc/Song2021LENLS18.pdf) of mine from 2021, which can be viewed as a "prequel" to my ACT2022 submission
2. my [slides](https://www.juliosong.com/doc/Song2022SynLabJun.pdf) from a recent talk, which contain a further application of the same tool to a different linguistic problem and hence can be viewed as a "sequel" to my ACT2022 submission
3. my [slides](https://www.juliosong.com/doc/Song2022AALslides.pdf) from another recent talk, which contain some general disciplinary remarks

*(Quick Ad: the [Category Theory Notes series](https://blog.juliosong.com/linguistics/mathematics/category-theory-notes-1/) on this blog, which records my personal experiences of learning category theory as a linguist, is gonna have a Season 2 later this year---watch this space. ^_^ )*

***
*Overview of my ACT2022 portfolio:*
- Part I: [Category theory in theoretical linguistics](https://youtu.be/mgS5ePNtHGk) (a 4-min explainer video laying out the disciplinary context of my study in very broad terms---no previous knowledge required in either category theory or linguistics)
- Part II: [Another application of category theory in linguistics]({{ site.baseurl }}{% post_url 2022-07-15-another-application-of-category-theory-in-linguistics-part-1 %}) (this blogpost)
- Part III: [Category theory in theoretical linguistics: A monadic semantics for root syntax](https://www.juliosong.com/doc/Song2022ACTabstract.pdf) (my extended abstract)
- Part IV: the actual [e-poster](https://www.juliosong.com/doc/act2022poster/poster.html)

***

If you are attending ACT2022, feel free to hmu at the **hybrid poster session (July 19, 17:00 -- 17:20 BST/UTC+1)** or in the conference Zulip chat (see conference website for URL). Of course, I am also happy to chat after the conference! 😃

## Category theory & linguistics
Before I introduce my particular research topic, I'd like to first make some general remarks on categorical linguistics (CT-Ling) as an emerging field. In my opinion, CT-Ling is a bona fide interdisciplinary subject, because its development relies on input from both category theorists and linguists. Given the hugely different academic backgrounds, research agendas, etc. of the two groups, however, communication can be difficult, which makes occasions like the ACT conference even more meaningful.

To my knowledge, as of 2022 there's only a very small handful of categorical linguists around the world (or linguistically oriented category theorists, if you prefer that identity), and members within this group are further divided by our preferred linguistic frameworks, which is another challenge to fruitful communication (but of course the same is true in linguistics per se). To borrow some category-theoretic terminology, my impression is that the current situation of CT-Ling is like a [discrete category](https://ncatlab.org/nlab/show/discrete+category) made up of isolated case studies. But what's the big picture of the field? What are its top-level research goals and agenda? And what are the potential morphisms *between* the individual cases if we are to make the category nondiscrete? These are all questions that need to be considered in a more systematic approach to CT-Ling.

As I had mentioned in my [ACT2020 blogpost]({{ site.baseurl }}{% post_url 2020-06-28-a-new-application-of-category-theory-in-linguistics-part-1 %}), existing applications of category theory to linguistics mainly cluster in the areas of [categorial grammar](https://en.wikipedia.org/wiki/Categorial_grammar) and natural language processing, but I believe CT-Ling is by no means confined to those areas. Nor should it be confined to just syntax/semantics, for that matter. Rather, if CT-Ling is to become a general field of study in the future, its impact will be proportionate to the breadth and depth of its linguistic coverage. Again, I think interdisciplinary communication and engagement are crucial to this end. 🤝

## My ACT work
I received graduate education in [transformational generative grammar](https://en.wikipedia.org/wiki/Transformational_grammar) (TGG), so I know this school of theoretical linguistics slightly better. After exposing myself to category theory for a while, I feel like there's actually lots of issues in TGG that can be viewed from a CT perspective.

For instance, in my 2019 [dissertation](https://doi.org/10.17863/CAM.44842), I examined the inventory of syntactic categories (which I called grammatical types in my ACT2020 submission to avoid misunderstanding due to the overloaded term "category") in human language as assumed in current TGG through the lens of CT, which revealed a whole arena of formal analogies between TGG and CT concepts. To name a few,

| TGG concept | CT perspective |
| ------------------ | -------------------- |
| hierarchy of projection (HoP) | poset category |
| cross-HoP parallelism | adjoint situation between posets |
| HoP selection | Yoneda embedding |

While my ACT2020 submission was more about the ontological aspect of linguistics, my submission this year is more about its derivational/compositional aspect. In my impression, the latter aspect has aroused more interest in the ACT community (partly due to the popularity of categorial grammar), so in a sense I'm getting closer to the mainstream now 😃. However, since the biggest appeal of CT is its generality, ontological issues such as the organization of the lexicon can certainly be tackled categorically as well. To quote the opening sentence of Fong & Spivak's fantastic textbook [*An Invitation to Applied Category Theory*](https://www.cambridge.org/core/books/an-invitation-to-applied-category-theory/D4C5E5C2B019B2F9B8CE9A4E9E84D6BC) (CUP, 2019):
> Category theory is unmatched in its ability to organize and layer abstractions and to find commonalities between structures of all sorts.

My ACT2022 submission is about the compositional semantics of [content words](https://en.wikipedia.org/wiki/Content_word)---as well as that of semigrammatical words, because the two classes are unifiable on the theory I'm promoting. They are unifiable because they both contain idiosyncratic or encyclopedic information. Purely grammatical words, by contrast, contain no such information and solely serve grammatical purposes.

## Semigrammaticality
If you have experience speaking or learning a language with [classifiers](https://en.wikipedia.org/wiki/Classifier_(linguistics)), such as Chinese or Japanese, you will immediately understand what I mean, since classifiers are a quintessentially semigrammatical word class. On the one hand, they encode the grammatical function of making mass concepts countable. On the other hand, they bring in miscellaneous conventionalized perspectives while performing their grammatical function. Thus, to say things like 'two mirrors' and 'three pencils' in Chinese, one must insert a suitable classifier between the numeral and the noun. The classifer for mirrors is *mian4* (literally 'face, surface') while that for pencils is *zhi1* (literally 'twig, branch'). They have exactly the same grammatical function as classifiers but each encode a different "shape" of perception---mirrors usually have a flat surface, while pens are usually long and thin.

As the above classifer example shows, semigrammatical words are like "double agents," because their grammatical/logical and lexical/idiosyncratic sides are both salient. And although I keep saying "words" to keep the blogpost simple, semigrammatical items in human language needn't always be words but may also be affixes. For instance, many Native American languages have affixal classifiers (I gave a [talk](https://www.juliosong.com/doc/Song2021ICFL9.pdf) on the typological stuff in 2021 by the way).

So, how are semigrammatical words related to my ACT2022 submission? Well, it turns out that when linguists try to analyze semigrammatical words---as well as content words---in a more fine-grained theoretical setting, things become tricky. In modern-day linguistics, researchers are no longer satisfied with a mere classificatory perspective on word classes. We also want to know how the grammatical and the lexical side of a semigrammatical/content word are structurally related and, more crucially, how they combine into a gestalt. In other words, current theoretical linguistic research, at least on the syntactic side, has reached the "subatomic" level.

## Subatomic compositionality
Intuitively, compositionality should play a key role in this fine-grained inquiry. But the tricky thing is, lexical and compositional semantics have long been studied separately, and when people talk about meaning composition, they usually only care about the purely grammatical (i.e., functional) side of natural language sentences, with lexical idiosyncrasies being merely carried along in the compositional procedure (e.g., as function names or labels). For instance, from a compositional perspective, the two sentences "the cat chased the rat" and "the boy ate the apple" are actually nondistinct, since they have exactly the same syntactic and logical structures:
- syntax: [<sub>vP</sub> DP<sub>1</sub> [<sub>vP</sub> v [<sub>VP</sub> V DP<sub>2</sub>]]] (in TGG notation)
- logic: $\exists e. [\mathrm{V}(e) \wedge \mathrm{Agent}(e) = \mathrm{DP}_1 \wedge \mathrm{Patient}(e) = \mathrm{DP}_2]$ ([neo-Davidsonian](https://www.coli.uni-saarland.de/courses/incsem-12/neodavidsonian.pdf) notation)

My choice of notation here is just a matter of personal taste---the two sentences have the same skeletal representation in other formal linguistic theories too. As such, the observation that the two sentences actually mean different things is a consequence of our lexical semantic knowledge, not one of our grammatical knowledge.

But of course, the hard question is how we manage to integrate lexical and compositional semantic knowledge in our mind. As I said in my [explainer video](https://youtu.be/mgS5ePNtHGk), language is a perfect reflection of the human mind. Since we are repeating the same lexical/compositional meaning integration procedure nonstop everyday, whatever makes that possible must be a super fundamental part of our linguistic capacity. Due to the limitations of science in this era, there's no way to know precisely what is going on in our mind/brain at such a fine-grained level. But it is at least legitimate to ask how we can formally represent and reason about the ubiquitous and seamless integration of lexical and compositional---i.e., purely idiosyncratic and purely logical---meanings in our analyses of natural languages.

And that's the thinking behind the idea in my ACT2022 submission. My main proposal is that the formal representation task above can be handled by the monad tool from category theory---more exactly by a variant of the [writer monad](https://kseo.github.io/posts/2017-01-21-writer-monad.html) popular in functional programming. As I clarified in my preliminary publications, my separation of pure functions and idiosyncrasies in meaning representation via the writer monad heavily builds on [Asudeh & Giorgolo's (2020)](https://global.oup.com/academic/product/enriched-meanings-9780198847854?cc=tw&lang=en&) monad-based approach to [conventional implicature](https://glossary.sil.org/term/conventional-implicature), such as the negative speaker attitude in "Yank." In fact, conventional implicature can be viewed as a special subcase of the more general issue of content/semigrammatical word meanings.

[[Link to Part 2 of this post]({{ site.baseurl }}{% post_url 2022-07-15-another-application-of-category-theory-in-linguistics-part-2 %})]
