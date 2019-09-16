---
title: "Category theory notes 8: Functoriality"
categories: [linguistics, mathematics]
tags: [category theory]
header:
  overlay_image: /assets/images/sky.jpg
  show_overlay_excerpt: false
  image_description: "A photo I took from the window of a plane."
  caption: "I took this photo from the window of a plane in 2014."
  teaser: /assets/images/sky.jpg
---

Fong &amp; Spivak refer to category, functor, and natural transformation as the "big three" of category theory in their newly published textbook [_An Invitation to Applied Category Theory: Seven Sketches in Compositionality_](https://www.cambridge.org/core/books/an-invitation-to-applied-category-theory/D4C5E5C2B019B2F9B8CE9A4E9E84D6BC) (henceforth _Seven Sketches_). In the previous seven posts of this series I've only written about categories. In this post I'm finally touching on functors.

The definition of a functor is straightforward. It's just an arrow between two categories. Unlike arrows between objects (i.e., "arrows" when the word is used alone), **functors map two types of data at once: objects and (inter-object) arrows.** This is because at the functorial level the internal structures of the source and target categories are visible---recall that at the category-internal level the source and target objects are opaque.

{% include figure image_path="/assets/images/functor.jpg" alt="An illustration of a functor" caption="A functor $F$ between two categories $\mathbb{C}$ and $\mathbb{D}$ (the arrows are merely expository)" %}
<a id="functorr"></a>

## Functor defined
I mentioned the axiomatic definition of categories in my [Aug 28 post]({{ site.baseurl }}{% post_url 2019-08-28-category-theory-notes-5 %}). A category consists of a collection of _objects_ and a collection of _arrows_ (aka. _morphisms_), where each object is associated with an _identity arrow_ and every pair of composable arrows actually compose, with the _composition_ obeying _associativity_ and the _unit law_. **A functor maps all these data and their structures from one category to another.** In Awodey's words,<a id="functordef"></a>
> A functor $F\colon \mathbb{C}\rightarrow \mathbb{D}$ between categories $\mathbb{C}$ and $\mathbb{D}$ is a mapping of objects to objects and arrows to arrows, in such a way that <br>
> (a) $F(f\colon A\rightarrow B) = F(f)\colon F(A) \rightarrow F(B),$ <br>
> (b) $ F(1\_A) = 1\_{F(A)}, $ <br>
> (c) $F(g\circ f) = F(g)\circ F(f).$ ([_Category Theory_](https://global.oup.com/ukhe/product/category-theory-9780199237180?cc=gb&lang=en&), pp.&nbsp;8--9)

So, a functor sort of creates an "image" of its source inside its target. Specifically, it may distort or collapse the source category but may not break connectivity.

{% include figure image_path="/assets/images/functors.png" alt="Three good candidates and a bad candidate for functors" caption="Three good candidates ($F, G, H$) and a bad candidate ($I$) for functors" %}

## A functor is two mappings
Functoriality is a highly compact notion. When we say $F\colon\mathbb{C}\rightarrow\mathbb{D}$ is a functor, we mean that $F$ maps all the above-specified data from $\mathbb{C}$ to $\mathbb{D}$. In other words, $F$ is not a single mapping but a "bundle" of mappings. In Mac Lane's words:<a id="maclane"></a>
> [A] functor $T$ ... consists of two suitably related functions: The object function $T$ ... and the arrow function (also written $T$) .... (_CWM_, p.&nbsp;13)

Mathematicians habitually write the object and the arrow functions both with the same letter (e.g., $T$). By contrast, the two functions have separate notations in some applied areas such as functional programming. Take Haskell for example. Its type class [Functor](https://en.wikibooks.org/wiki/Haskell/The_Functor_class) is defined as follows:
```haskell
class Functor f where
  -- one method
  fmap :: (a -> b) -> f a -> f b
  -- two laws
  fmap id == id
  fmap (f . g) == fmap f . fmap g
```
As the definition shows, the `Functor` class in Haskell has a single method `fmap` that maps a function `a -> b` to another function `f a -> f b`, and this mapping must satisfy two laws: (i) it must preserve identity; (ii) it must preserve composition.

Comparing the definition of the Haskell Functor with that of the mathematical functor (see <a href="#functordef">above</a>), we can easily find that the two are essentially the same: `fmap` is just the arrow function, and `f` is the categorical object function. As such, the Haskell Functor class itself is merely half of a mathematical functor, while the other half is defined as a method of the class. For those who want to learn more about the categorical nature of Haskell I recommend Bartosz Milewski's 2018 book [_Category Theory for Programmers_](https://books.google.co.uk/books/about/Category_Theory_for_Programmers.html?id=ZaP-swEACAAJ&source=kp_book_description&redir_esc=y).
<a id="jec"></a>

## Functor jectivity
<a href="#maclane">Above</a> I cited Mac Lane's statement that a functor consists of two _functions_. An important property of function is _jectivity_: in set-theory a function can be [injective](https://en.wikipedia.org/wiki/Injective_function) (one-to-one), [surjective](https://en.wikipedia.org/wiki/Surjective_function) (onto), or [bijective](https://en.wikipedia.org/wiki/Bijection) (one-to-one correspondence).

The jectivity-based classification also makes sense in category theory---and at different abstraction levels. At the category-internal level, arrows are classified into monomorphisms, epimorphisms, and isomorphisms (see [this blog post](https://dkalemis.wordpress.com/2014/08/18/how-jectivity-corresponds-to-morphisms/) for an introduction); and at the functorial level, functors are classified as full, faithful, and so on. Here I won't comment on arrow jectivity but will focus on functor jectivity, because I had only found the latter confusing.

**Since a functor consists of two functions, it can be given a jectivity class in two dimensions---one based on objects and the other based on arrows.** Moreover, the arrow dimension further involves two subdimensions: that of the overall arrow collection of the category and that of the arrow collection between each pair of objects (i.e., the [hom-set]({{ site.baseurl }}{% post_url 2019-08-28-category-theory-notes-5 %}#homsett)).

**A note for beginners:** Textbooks usually focus on the hom-set-based classification, which defines full, faithful, and fully faithful functors. However, since you sooner or later will encounter classifications in other (sub)dimensions, it's better to learn the whole picture from the beginning so that you won't experience unnecessary confusion like I did. As far as I know, Awodey's textbook (p.&nbsp;148) has the most complete introduction of the various jectivity classes for functors.
{: .notice--info}

### 1. Jectivity based on hom-set
A functor is
- [*full*](https://ncatlab.org/nlab/show/full+functor) if its hom-set mapping is surjective,
- [*faithful*](https://ncatlab.org/nlab/show/faithful+functor) if its hom-set mapping is injective, and
- [*full and faithful*](https://ncatlab.org/nlab/show/full+and+faithful+functor) (aka. fully faithful) if its hom-set mapping is bijective.

{% include figure image_path="/assets/images/full-faithful.png" alt="An illustration of hom-set-based functor jectivity" caption="An illustration of full (left), faithful (middle), and fully faithful functors" %}

These full/faithful terms are widely taught mainly because they are closely related to another important categorical concept [_subcategory_](https://ncatlab.org/nlab/show/subcategory). A subcategory is related to its "supercategory" via an [_inclusion functor_](https://en.wikibooks.org/wiki/Category_Theory/Functors#Examples), which is automatically faithful (because the subcategory is just part of the supercategory) and in addition may also be full (when the "part" keeps hom-sets intact); in the latter case we have a [_full subcategory_](https://ncatlab.org/nlab/show/full+subcategory).

### 2. Jectivity based on object collection
A functor is
- [_injective on objects_](https://proofwiki.org/wiki/Definition:Injective_on_Objects) if its object function is injective,
- [_surjective on objects_](https://ncatlab.org/nlab/show/surjective+on+objects+functor) if its object function is surjective, and
- [_bijective on objects_](https://ncatlab.org/nlab/show/bo+functor) (aka. bo) if its object function is bijective.

{% include figure image_path="/assets/images/jectivity-object.png" alt="An illustration of object-collection-based functor jectivity" caption="An illustration of functors injective (left), surjective (middle), and bijective on objects (arrows omitted)" %}

Taking isomorphic objects into account, we can also define the following "essentially" versions of the above terms---a functor is
- _essentially injective on objects_ if its object function is injective up to isomorphism,
- [_essentially surjective on objects_](https://ncatlab.org/nlab/show/essentially+surjective+functor) if its object function is surjective up to isomorphism, and
- [_essentially bijective on objects_](https://ncatlab.org/nlab/show/bo+functor) if its object function is bijective up to isomorphism.

{% include figure image_path="/assets/images/jectivity-object-iso.jpg" alt="An illustration of isomorphism-supported-object-collection-based functor jectivity" caption="An illustration of functors essentially injective (left), surjective (middle), and bijective on objects (non-iso arrows omitted)" %}

Two places I've seen these "essentially" notions<sup><a href="#fn1" id="ref1">1</a></sup> are the definition of [_categorical embedding_](https://en.wikipedia.org/wiki/Subcategory#Embeddings) (full + faithful + essentially injective on objects) and that of [_categorical equivalence_](https://en.wikipedia.org/wiki/Equivalence_of_categories) (full + faithful + essentially surjective on objects). I do have notes on both, but I'll leave them to future posts.

### 3. Jectivity based on arrow collection
I haven't met functor classes in this subdimension in my limited experience but list them anyway for completeness. A functor is
- [_injective on arrows_](https://proofwiki.org/wiki/Definition:Injective_on_Morphisms) if its arrow function is injective,
- [_surjective on arrows_](https://proofwiki.org/wiki/Definition:Surjective_on_Morphisms) if its arrow function is surjective, and
- _bijective on arrows_ if its arrow function is bijective.

I haven't met any "essentially" versions of these terms either. **In my experience when _essentially injective/surjective/bijective_ is used alone the intended reading is always "... on objects."**
<br><br>
In sum, functor jectivity is a lot more complex than arrow jectivity, because a functor is really a bundle of mappings. I use the following picture to illustrate the above-mentioned classes:

{% include figure image_path="/assets/images/jectivity.png" alt="A summary of jectivity-based functor classification" caption="A summary of jectivity-related functor classes" %}

## Takeaway
- A functor consists of two suitably related functions, one on objects and the other on arrows.
- In Haskell the Functor type class merely corresponds to the object part of a categorical functor, while the arrow part is implemented as a method `fmap` on the Functor class.
- Functors can be classified based on jectivity in different (sub)dimensions, but the most useful subclasses for beginners to know are the hom-set-arrow-based "full/faithful" series and the isomorphism-supported-object-based "essentially" series.

<hr>
<div style="font-family: serif; font-size: 0.8em;">
<a id="fn1">1.</a><sup><a href="#ref1" title="Jump back to footnote 1 in the text.">↩</a></sup> Since we can't predict that <em>essentially</em> means &#8220;up to isomorphism&#8221; here, these <em>essentially</em>-terms are essentially idiomatic; see my <a href="{{ site.baseurl }}{% post_url 2019-08-31-category-theory-notes-7 %}">Aug 31 post</a>.
</div>
