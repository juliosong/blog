---
title: "Category theory notes 6: Think big"
categories: [linguistics, mathematics]
tags: [category theory]
header:
  overlay_image: /assets/images/sky.jpg
  show_overlay_excerpt: false
  image_description: "A photo I took from the window of a plane."
  caption: "I took this photo from the window of a plane in 2014."
  teaser: /assets/images/sky.jpg
---

**Category theory is spectacularly big.** But exactly how big is it? Consider a set $A$. It can hold a huge number of elements, say, all grains of sand on Earth. That's already too humongous a size for my mundane brain to imagine, but in the category $\mathbf{Set}$ it just takes up the space of a single object, alongside many other sets $B, C, D,$ etc. For example, let $B$ be the set of all human beings that have ever existed on Earth, $C$ the set of all natural languages that have ever been spoken, and $D$ the set of all puli dogs. I guess none of the four sets can be considered "big" in a mathematical sense---they all have a finite number of members and can be easily compared for cardinality (presumably $D<C<B<A$).

{% include figure image_path="/assets/images/category-set.jpg" alt="A set as an object in the category Set" caption="A set is an object in the category $\mathbf{Set}$ (the arrows are merely expository)." %}

## Category sizes
$\mathbf{Set}$ is the category of all sets and functions, which surely is enormous. Yet in the world of categories it's just a single category, and a _locally small_ one (see [this](https://www.quora.com/Why-is-the-category-Sets-locally-small) Quora page for a beginner-friendly explanation). In category theory **there are three conventional sizes of categories.** A category is
- _small_ if both its object collection and its arrow collection are sets;
- _large_ if both its object collection and its arrow collection are [proper classes](https://en.wikipedia.org/wiki/Class_(set_theory));
- _locally small_ if, even though its object collection is a proper class, the arrows between any two objects in it form a set (i.e., a [hom-set](https://en.wiktionary.org/wiki/hom-set); see my [Aug 28 post]({{ site.baseurl }}{% post_url 2019-08-28-category-theory-notes-5 %})).

Crucially, here "small" and "large" shouldn't be understood in the everyday sense. They should be recognized and learned as mathematical terms instead. Locally small categories are a subclass of large categories. So, **if a category is locally small, it's automatically large, but not vice versa.** The classificatory relation between the three sizes is as follows.

![relative sizes of categories](/assets/images/relative-size.png)

We linguisticians love cross classifications. To cross-classify category sizes we need three binary features: `[object-collection (oc): ±set]` (whether the object collection is a set), `[arrow-collection (ac): ±set]` (whether the arrow collection is a set), and `[hom: ±set]` (whether the hom-collections are sets).

|                 | [oc:±set] | [ac:±set]       | [hom:±set]  |
|:---------------:|:---------:|:---------------:|:-----------:|
| small           |  +        | +               |  +          |
| locally small   | -         | -               |  +          |
| (properly) large| -         | -               |  -          |
| ?               | +         | -               | ±           |


As the table shows, the three features cross-classify categories into five licit sizes,<sup><a href="#fn1" id="ref1">1</a></sup> among which three are officially recognized. What are the `[[oc:+set],[ac:-set],[hom:±set]]` sizes? I don't know.🤷‍♂️

Beyond the above cross classification, some people also speak of a fourth category size, _very large_ (see [this](https://ncatlab.org/nlab/show/CAT) nLab page), which describes a category whose objects are all categories, including the properly large ones (this is what Mac Lane means by [_metacategory_](https://ncatlab.org/nlab/show/metacategory) in _CWM_). But nowadays that concept is not often used and certainly not mentioned in many introductory textbooks.

### Examples
To illustrate, many of the categories standardly studied in mathematics, such as $\mathbf{Set}, \mathbf{Grp},$ and $\mathbf{Pos},$ are locally small. By comparison, most categories of interest outside mathematics, such as the category [$\mathbf{Hask}$](https://en.wikibooks.org/wiki/Haskell/Category_theory) for Haskell types and functions, are properly small. Some specially designed "toy categories" in mathematics are also small, such as monoid categories (see my [Aug 24 post]({{ site.baseurl }}{% post_url 2019-08-24-category-theory-notes-4 %})), [poset](https://en.wikiversity.org/wiki/Introduction_to_Category_Theory/Categories#Posets) categories (see my [Aug 28 post]({{ site.baseurl }}{% post_url 2019-08-28-category-theory-notes-5 %})), and [ordinal number](https://unapologetic.wordpress.com/2007/05/24/cardinals-and-ordinals-as-categories/) categories ($\mathbf{1}, \mathbf{2}, \mathbf{3},$ etc.).

Properly large categories are much rarer (at least to my knowledge; see [this page](https://math.stackexchange.com/questions/678287/what-is-an-example-of-a-large-category) for a discussion): the category $\mathbf{Cat}$ of all small categories is in fact [locally small](https://math.stackexchange.com/questions/2606803/the-category-of-all-small-categories); the category $\mathbf{Cat^\*}$ of all locally small categories seems to be properly large (see [_Gentle Intro_](https://www.logicmatters.net/2018/01/29/category-theory-a-gentle-introduction/), p.&nbsp;153); and the category $\mathbf{CAT}$ of all categories (large and small) is very large.

{% include figure image_path="/assets/images/category-cat.png" alt="An illustration of the relative sizes of categories" caption="Relative sizes of categories" %}

At the $\mathbf{CAT}$ scale our initial sand set $A$ is already too minuscule to be noticeable or cared about, like an amoeba in an ocean or a person in the universe. Indeed, sometimes size comparison in category theory reminds me of videos that compare celestial body sizes, like this one:

{% include video id="i93Z7zljQ7I" provider="youtube" %}

## Ladder of abstraction
**What good do the size-related concepts in category theory do to us nonmathematicians?** In my own experience, a most important benefit I've got is the "ladder of abstraction" mind-set. Given a particular system, there may be multiple angles to view it. The categorical mind-set guides us to organize those angles into ascending levels of abstraction, with constructs at lower levels "feeding" constructs at higher levels.

{% include figure image_path="/assets/images/ladder.jpg" alt="A ladder carved with Chinese characters" caption="A ladder carved with five Chinese characters and showing their gradual abstraction" %}

**Since I'm a linguistician, I'll use human language as an example.** At the lowest level of abstraction, a language is just a (presumably infinite) set of utterances, containing elements like _apple_ and _It's sweet._ At a higher level of abstraction, the utterances can be assigned and described by syntactic types (i.e., linguisticians' _categories_), such as noun and sentence. Most people's understanding of human language stops at this level, which is also the level of abstraction school grammars dwell in.

At an even higher level of abstraction, the numerous syntactic types can be divided into several sets, such as "nouny" types (e.g., noun, determiner, classifier) and "verby" types (e.g., verb, sentence, tense). These sets are internally structured and externally interconnected---IMHO following some simple yet powerful "templates," which I'm inclined to call the "DNA of human language grammar." And the abstraction continues. In my PhD dissertation I used nearly 300 pages to illustrate the intricately layered structures arising from grammatical types, and quite a few discoveries I made were inspired by category theory.

**The more abstract the perspective is, the more useful category theory is.**
{: .text-center .notice}

## Takeaway
- Category theory is **really** large-scale!
- There are three standardly recognized sizes of categories: small, large, and locally small.
- Most categories in mathematics per se are locally small, while most categories outside mathematics are small.
- Understanding the size-related concepts in category theory can help us form a highly useful ladder-of-abstraction mind-set.

<hr>
<div style="font-family: serif; font-size: 0.8em;">
<a id="fn1">1.</a><sup><a href="#ref1" title="Jump back to footnote 1 in the text.">↩</a></sup> The three features in theory give rise to eight combinations. However, only five of them (i.e., those shown in the table) are licit in practice, because if the arrow collection is a set (i.e., [ac:+set]), the hom-collections are necessarily also sets (i.e., [hom:+set]), hence the absence of the [[oc:±set], [ac:+set], [hom:-set]] combinations. Similarly, if the object collection isn't a set (i.e., [oc:-set]), then the arrow collection can't be a set either (i.e., [ac:-set]), for each object brings about at least an identity arrow, and so there are at least as many arrows as objects in a category; hence the absence of the [[oc:-set], [ac:+set], [hom:±set]] combinations.
</div>
