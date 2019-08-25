---
title: "Category theory notes 3: _Categorial_ or _categorical_?"
categories: [linguistics, mathematics]
tags: [category theory]
header:
  overlay_image: /assets/images/sky.jpg
  show_overlay_excerpt: false
  image_description: "A photo I took from the window of a plane."
  caption: "I took this photo from the window of a plane in 2014."
  teaser: /assets/images/sky.jpg
---

_Category_ in _category theory_ is a noun, but we often need to use the term in other parts of speech (notably adjective and verb). Try the following quiz for example.

(1) An interesting application of category theory is <u>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</u> logic.<br>
A. categorial&nbsp;&nbsp;&nbsp;B. categorical&nbsp;&nbsp;&nbsp;C. categoric&nbsp;&nbsp;&nbsp;D. category

(2) This is a <u>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</u> approach to set theory.<br>
A. categorial&nbsp;&nbsp;&nbsp;B. categorical&nbsp;&nbsp;&nbsp;C. categoric&nbsp;&nbsp;&nbsp;D. category

(3) It's fun to <u>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</u> set-theoretic theorems.<br>
A. categorize&nbsp;&nbsp;&nbsp;B. categorialize&nbsp;&nbsp;&nbsp;C. categoricalize&nbsp;&nbsp;&nbsp;D. categorify

(4) The trend of <u>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</u> has spread from mathematics per se into other disciplines.<br>
A. categorization&nbsp;&nbsp;&nbsp;B. categorification&nbsp;&nbsp;&nbsp;C. categorialization&nbsp;&nbsp;&nbsp;D. categoricalization

(The key is at the end of this post.)

## _Categorial_ or _categorical_?
Mathematicians aren't bothered much by such morphological variation, and as far as I'm concerned no misunderstanding has been caused by it either. For instance, Mac Lane uses _categorical_ in [_CWM_](https://books.google.co.uk/books?id=MXboNPdTv7QC&source=gbs_book_other_versions) while Goldblatt insists on using _categorial_ in [_Topoi_](https://books.google.co.uk/books/about/Topoi.html?id=5qTvoAEACAAJ&source=kp_book_description&redir_esc=y). The latter even insists on his choice:
>I have consistently used the word "categorial" where the literature uniformly employs "categorical." The reason is that while both can serve as adjectival forms of the noun "category," the second of them already has a different and long established usage in the domain of logic, one that derives from its ordinary-language meaning of "absolute." (p.&nbsp;x)

Building on Goldblatt's remark, I think **the current inconsequentiality of the terminological variation in category theory may only be temporary.** With the increasing popularity of "[applied category theory](https://arxiv.org/pdf/1809.05923.pdf)" as an interdisciplinary enterprise, the _category_-derived terms may sooner or later have to be actively disambiguated. After all, _category_ is a term used in numerous fields (see my [previous post]({{ site.baseurl }}{% post_url 2019-08-21-category-theory-notes-2 %})), and each field needs derived forms of the noun. <!--, especially for those interested in applied category theory but are not yet familiar with the connotations of the various _category_-derived terms.-->

## _Categorify_ or _categorize_?
For example, _categorize_ and [_categorization_](https://en.wikipedia.org/wiki/Categorization) are commonly used in linguistics and other cognitive sciences, which refer to the assignment of (classificatory) categories to objects. [Stevan Harnad](https://en.wikipedia.org/wiki/Stevan_Harnad) has an article entitled "[To cognize is to categorize: cognition is categorization](https://eprints.soton.ac.uk/261725/)" (2005).  Here _categorize_ can't be replaced by _categorify_, as the latter means studying something with the toolkit of category theory. But what if someone decides to study cognitive categorization with category theory? That'd be a "categorification of categorization." And what if someone else wants to study how students cognize the categorification method? That'd be the "categorization of categorification."😳

In cases like the above it's vital to disambiguate derived terms from different disciplinary sources. Currently there are not yet automata that help mathematicians do the categorification job, but if they were invented someday they'd probably be called _categorifiers_, which again must be distinguished from the grammatical [_categorizers_](https://www.degruyter.com/view/j/tlir.2011.28.issue-3/tlir.2011.010/tlir.2011.010.xml) in linguistics or the automatic [_categorizers_](https://www.edrm.net/glossary/bayesian-categorizer/) in artificial intelligence.

## _Categorial grammar_ or _categorical grammar_?
If the above example looks a bit contrived, let's look at another real example from linguistics. Which adjectival form should be used in the following sentence?

(5) <u>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</u> grammar takes an algebraic approach to natural language syntax.<br>
A. Categorial&nbsp;&nbsp;&nbsp;B. Categorical&nbsp;&nbsp;&nbsp;C. Categoric&nbsp;&nbsp;&nbsp;D. Category

The answer is either A or B depending on the context. **Categorial grammar in its [classical incarnation](https://link.springer.com/chapter/10.1007/978-3-642-31555-8_1) (the Ajdukiewicz--Bar-Hillel or AB system) wasn't based on category theory.** Category theory was invented in the 1940s---the seminal paper is "[General theory of natural equivalences](https://www.ams.org/journals/tran/1945-058-00/S0002-9947-1945-0013131-6/S0002-9947-1945-0013131-6.pdf)" (Eilenberg &amp; MacLane 1945), but Ajdukiewicz's paper "[Die syntaktische Konnexität](https://www.bibsonomy.org/bibtex/12979b6809c1f9959f99a19bbaa643439/nlp)" (Syntactic connexion), where the conception of a category-based algebraic grammatical theory is first presented, was published in 1935 ([here](https://link.springer.com/chapter/10.1007/978-94-010-1120-4_7) is an English translation).  Bar-Hillel's paper entitled "[A quasi-arithmetical notation for syntactic description](http://ling.umd.edu/~alxndrw/CGReadings/bar-hillel-53.pdf)" was published after category theory's invention, in 1953, but the proposal there apparently isn't based on category theory either.

Both Ajdukiewicz (1935) and Bar-Hillel (1953) define _categories_ in a conventional linguistic way, which are called "semantic categories" by the former and "syntactic/type categories" by the latter. There are basic categories like noun and sentence as well as complex categories like verb and modifier. These categories have nothing to do with category theory and take the adjective form _categorial_ following the standard practice in linguistics.

**The connection between categorial grammar and category theory was actually made much later,** presumably in the 1960s, by Lambek (see Lambek 1988, cited below, for a historical note). In fact Bar-Hillel criticized Lambek's misuse of the adjective _categorical_ for categories in the sense of types (so for Bar-Hillel _categorical grammar_ is wrong). The historical note below is from Lambek's 1988 paper "[Categorial and categorical grammars](https://link.springer.com/chapter/10.1007/978-94-015-6878-4_11)":
>[I]t was quite apparent that one was dealing with a certain kind of "closed" category ([Lambek 1969](https://link.springer.com/content/pdf/10.1007/BFb0079385.pdf)), although this information was suppressed in papers addressed to a linguistic audience. ...Bar-Hillel commented on the carelessness of my typist in writing "categorical" in place of "categorial." I did not dare to tell him that the typist was quite innocent and that I had not realized that these were two distinct words. It appeared that the word "categorical" should only refer to the categories introduced by Eilenberg and MacLane in their pioneering article ... while "categorial" refers to the categories in the sense of types. (p.&nbsp;297)

Anyway, Lambek made the connection in the 1960s and further promoted it from the 1980s onward, though the name "categorial grammar" stayed unchanged. N.b. even in the 1988 paper Lambek didn't change _categorial grammar_ to _categorical grammar_ but merely listed them side by side.

**The connection with category theory blurred the connotation of _category_ in the category-based grammatical theory.** On the one hand, it must still keep the linguistic meaning of syntactic/semantic type, because without this meaning categorial grammar as a whole becomes pointless. On the other hand, it accidentally acquired a new meaning from category theory; namely, that the type-category-based grammatical theory can be viewed as a math-category. In other words, **Lambek categorified categorial grammar.** And now it should be clear that the two occurrences of the morphological root _category_ in the words _categorify_ and _categorial_ are heterogeneous!

I don't see any good solution to the "terminological trap" in categori(c)al grammar, especially with its further combination with Chomsky's theory in recent years (e.g., [categorial minimalist grammar](https://arxiv.org/abs/1012.2661)), because Chomsky's usage of _category_ is again different from that in categorial grammar, and the attempted marriage of categorial grammar with both category theory (via Lambek's theory) and minimalism overloads the term _category_ twice at the same time. **The example of categorial grammar well illustrates the kind of trouble one may encounter in an era of "widespread categorification."** Interdisciplinary collaborators do need to be careful with the _category_-derived terminology.

## Takeaway
The numerous _category_-derived terms are a latent source of confusion in the application of category theory to other nonmathematical fields. Until a more efficient solution is agreed upon, we need to remember and follow the separate disciplinary conventions.
- **categorial:** mainly used in cognitive sciences and especially in linguistics, related to type or class
- **categorical:** used in category theory (in the [technical]({{site.baseurl}}{% post_url 2019-08-21-category-theory-notes-2 %}#catdef) sense) and some branches of logic (derived from the sense "absolute")
- **categorize:** used in linguistics, other cognitive sciences, and artificial intelligence, in the sense of assigning types to objects and thereby classifying them (derivatives: _categorization_, _categorizer_)
- **categorify:** exclusively used in category theory, in the sense of studying various stuff with category theory (derivatives: _categorification_, _?categorifier_)

As of 2019 there are (fortunately!) no such terms as _categorialize_, _categoricalize_, or _categoric_. Let's hope they won't be coined in the future either...

<hr>
<span style="font-family:serif;font-size:0.8em;">(Key to quiz: BBDB)</span>
