---
title: "Category theory notes 18: Reflective subcategory (Part 2)"
categories: [linguistics, mathematics]
tags: [category theory]
header:
  overlay_image: /assets/images/sky.jpg
  show_overlay_excerpt: false
  image_description: "A photo I took from the window of a plane."
  caption: "I took this photo from the window of a plane in 2014."
  teaser: /assets/images/sky.jpg
---

In my previous post "[Category theory notes 17: Reflective subcategory (Part 1)]({{ site.baseurl }}{% post_url 2019-09-14-category-theory-notes-17 %})" I discussed the similarity and distinction between linguistic and mathematical "subcategories" and began commenting on a particular type of mathematical subcategory named "reflective subcategory." In this post I'll continue writing about reflective subcategories and, in particular, relate them to a special type of adjoint situation.

## Reflectivity and co-unit
Now that we know what a reflective subcategory is, I'd like to present a nice result about reflectivity in relation to the adjunction co-unit. In short, in a reflective subcategory situation---or more precisely in an adjunction where the right adjoint is fully faithful---the co-unit is a natural isomorphism. (Dually if the left adjoint of an adjunction is fully faithful, then the unit is a natural isomorphism.)

I have to admit that this result had confused me for quite a while, mainly because textbooks usually leave its proof as an exercise, and (outrageously) without providing the key! I honestly think textbooks without exercise keys had better not include exercises at all, for they'd be more confusing than helpful to self-studying students...

I had tried to search the proof online, but unfortunately it's not a widely discussed issue, and the few answers I found in forum discussions (e.g., [this](https://math.stackexchange.com/questions/1994963/let-c-d-be-categories-and-fc-to-d-and-gd-to-c-be-adjoint-functors-then?noredirect=1&lq=1), [this](https://math.stackexchange.com/questions/2726117/f-dashv-g-and-g-fully-faithful-implies-counit-is-natural-isomorphism?rq=1), and [this](https://math.stackexchange.com/questions/3236275/how-to-use-yonedas-lemma-in-proving-f-fully-faithful-iff-unit-is-an-isomorph)) are either too cursory or too poorly presented (to the extent that the letters being used are not even declared). Apparently there're **two ways** to prove the result, one using the Yoneda lemma and the other not. Below I'll just go over the proof without Yoneda, because I haven't really understood the Yoneda-based proof myself. **Please leave a comment if you can help!** The following proof is basically based on the explanation in [this video](https://youtu.be/0AV7vg-16y0), which IMHO is the most easy-to-follow resource online on this issue.
<a id="lemma1"></a>

The proof consists of two parts, and it essentially relies on the following independent result (call it Lemma 1):
>**Lemma 1:** A split monomorphism and epimorphism is an isomorphism.

Why should we use this lemma? Because it works... I've noticed a couple of times in my category-theory-learning process that there's often no deeper motivation as to why something is used. The reasoning is usually just that that something makes the proof work, which is actually an impeccable motivation...

I think here lies a huge methodological difference between mathematics and linguistics. We linguisticians are always curious about and keen to find out deeper motivations behind working solutions and available theories. For example, it has long been known that human beings are equipped with some sort of language-learning mental device (or "[universal grammar](https://en.wikipedia.org/wiki/Universal_grammar)," without reading too literally into the term), and a lot has been learned about this "[language faculty](https://www.oxfordhandbooks.com/view/10.1093/oxfordhb/9780195309799.001.0001/oxfordhb-9780195309799-e-15)" in the past decades. Nevertheless, against this background, Chomsky further initiated a "[beyond explanatory adequacy](https://eclass.uoa.gr/modules/document/file.php/GS327/Materialien/Chomsky%20%282001%29%20-%20Beyond%20explanatory%20adequacy.pdf)" agenda in the [minimalist program](https://en.wikipedia.org/wiki/Minimalist_program):
>[W]e can seek a level of explanation deeper than explanatory adequacy, asking not only **what** the properties of language are, but **why** they are that way. (Chomsky 2001, "[Beyond explanatory adequacy](https://eclass.uoa.gr/modules/document/file.php/GS327/Materialien/Chomsky%20(2001)%20-%20Beyond%20explanatory%20adequacy.pdf)")

"Deeper motivation" questions like this (though not necessarily as deep as this one) are often brought up in linguistics, even in undergraduate courses. By contrast, deeper motivations are seldom bothered with in daily contexts of mathematics, at least to my very limited knowledge.

Anyway, for our current purpose let's just accept it that Lemma 1 is an ingredient we need and be satisfied with that, without being concerned about why we need it (other than that it makes the proof work). With this psychological acceptance, we need to show two things:
1. In an adjunction with a faithful right adjoint, the co-unit components are all split monomorphisms.
2. In an adjunction with a full right adjoint, the co-unit components are all epimorphisms.

Now consider the adjunction below

![an adjunction with a fully faithful right adjoint](/assets/images/adjunction-co-iso.svg)  

where $F$ is the left adjoint and $G$ is the right adjoint. We start with an arrow $f\colon X\rightarrow Y$ in $\mathbb{D}$ and **lift** it via $G$ into $\mathbb{C}$ (i.e., mapping it to $Gf\colon GX\rightarrow GY$). Next, we use the adjunction isomorphism to **flip** $Gf$ into $\mathbb{D}$ (i.e., mapping it to $FGX\rightarrow Y$). Notice that by arrow composition in $\mathbb{D}$ this new arrow $FGX\rightarrow Y$ is just $f\circ\varepsilon\_X.$ As such, we've successfully established a "tight relationship" among three arrows:
\\[ (X\rightarrow Y) \xrightarrow{G} (GX\rightarrow GY) \cong (FGX\rightarrow Y). \\]
Considering this relationship doesn't depend on the particular choice of $f$---that is, any arrow from $X$ to $Y$ would work---we can reformulate it in terms of hom-sets:

![a particular hom-set-based commutative diagram of an adjunction](/assets/images/adjunction-co-tri.svg)

N.b. the upper asterisk on ${\varepsilon\_X}^\*$ is just the upper asterisk in my [Sep 13 post]({{ site.baseurl }}{% post_url 2019-09-13-category-theory-notes-16 %}#astr). It means that the function symbol and the argument symbol should be syntactically swapped in the result of the function application; so ${\varepsilon\_X}^\*(f)=f\circ{\varepsilon\_X}.$
<a id="question2"></a>

Now, with the above configuration at hand, we can ask the following questions in turn:
1. What if the right adjoint $G$ is faithful?
2. What if the right adjoint $G$ is full?

Below I answer them one by one.

### What if the right adjoint $G$ is faithful?
If $G$ is faithful, then its arrow function is one-to-one, which means it maps hom-sets in an injective fashion; namely, $G_{X,Y}\colon \mathbb{D}(X,Y)\rightarrow\mathbb{C}(GX,GY)$ is injective. But since isomorphic objects are indistinguishable in category theory, we can safely replace $\mathbb{C}(GX,GY)$ by $\mathbb{D}(FGX,Y)$, whence ${\varepsilon\_X}^\*\colon\mathbb{D}(X,Y)\rightarrow\mathbb{D}(FGX,Y)$ is injective.

But what does the injectivity of ${\varepsilon\_X}^\*$ mean? It means for any two elements in $\mathbb{D}(X,Y)$---namely, for any two $\mathbb{D}$-arrows $f,g\colon X\rightarrow Y$---we have the following implication (by the definition of [injection](https://en.wikipedia.org/wiki/Injective_function)):
\\[ {\varepsilon\_X}^\*(f) = {\varepsilon\_X}^\*(g) \Rightarrow f=g. \\]
But this implication is just the following one:
\\[ f\circ\varepsilon\_X = g\circ\varepsilon\_X \Rightarrow f=g, \\]
which is just the implication in the definition of an [epimorphism](https://en.wikipedia.org/wiki/Epimorphism). Therefore, starting from the assumption that $G$ is faithful, we have arrived at the conclusion that $\varepsilon\_X$ (i.e., the $X$-component of the co-unit) is an epimorphism. Since our $X$ was randomly chosen in $\mathbb{D},$ we can further extend the conclusion to the entire co-unit:

**The right adjoint of an adjunction is faithful iff every component of the co-unit is an epimorphism.**
{: .text-center .notice--info}

### What if the right adjoint $G$ is full?
Now I turn to answer the second question raised <a href="#question2">above</a>, What if the right adjoint of the adjunction is a full functor? Well, following the same line of thought as above, it means the hom-set mapping $G_{X,Y}\colon\mathbb{D}(X,Y)\rightarrow\mathbb{C}(GX,GY)$ is surjective. And by the adjunction-induced hom-set isomorphism we have that the upper-asterisk-decorated co-unit component ${\varepsilon\_X}^\*$ is surjective. Up to this point we have just repeated what we did above, but from now on things begin to differ!

This part is a bit tricky because it involves some tedious calculation, so pay close attention!👉Since our $Y$ was randomly chosen in $\mathbb{D}$---or more exactly since the hom-set isomorphism induced by the adjunction is **natural** in $X, Y$---we can safely choose another $Y.$ Let's replace $Y$ by $FGX.$ Why this one? Because it's what makes the proof work---it's again one of those mathematical situations where no deep motivation is involved...😝 (though isn't "making things work" itself a valid motivation? the result justifies the action!)

Anyway, after replacing $Y$ with $FGX,$ we need to make some updates to the adjunction configuration, as follows:

![an adjunction with a fully faithful right adjoint - modified](/assets/images/adjunction-co-iso2.svg)

So we've replaced all occurrences of $Y$ with $FGX$ in the diagram, and everything still works. Accordingly, we also need to update our hom-set-based commutative diagram (i.e., the hom-set triangle).

![a particular hom-set-based commutative diagram of an adjunction - modified](/assets/images/adjunction-co-tri2.svg)

Observe what has just happened: the hom-set $\mathbb{D}(FGX,FGX)$ is just the set of endomorphisms on $FGX$! Now we can ask what the surjectivity of ${\varepsilon\_X}^\*$ means in this situation. Well, it by [definition](https://en.wikipedia.org/wiki/Surjective_function) means that **all** elements in $\mathbb{D}(FGX,FGX)$ are hit by the function ${\varepsilon\_X}^\*$; namely, for every arrow from $FGX$ to itself there must be a corresponding arrow from $X$ to $FGX.$ In particular, this means that the identity arrow on $FGX$ is also hit, whence
\\[ \exists g\colon X\rightarrow FGX, {\varepsilon\_X^\*}(g) = 1\_{FGX}. \\]
After getting rid of the upper asterisk we have
\\[ \exists g\colon X\rightarrow FGX, g\circ\varepsilon\_X = 1\_{FGX}. \\]
But this equation just means $\varepsilon\_X$ is a split monomorphism (i.e., section)!---because of the following diagram:

![co-unit split mono](/assets/images/adjunction-co-split-mono.svg)

Therefore, we have started with the assumption that $G$ is full and arrived at the conclusion that $\varepsilon\_X$ is a split monomorphism. Since we have randomly picked $X,$ we can extend the conclusion from the $X$-component to the entire co-unit:

**The right adjoint of an adjunction is full iff every component of the co-unit is a split monomorphism.**
{: .text-center .notice--info}

### What if the right adjoint $G$ is fully faithful?
Now that we've answered the two question <a href="#question2">above</a>, we're ready to combine them into a third and final result: The right adjoint of an adjunction is fully faithful iff every component of the co-unit is an epimorphism **and** a split monomorphism. But by <a href="#lemma1">Lemma 1</a> that just amounts to saying that every component of the co-unit is an **isomorphism**, which in turn amounts to saying that the co-unit natural transformation itself is a **natural isomorphism**! So, below is our desired theorem, now proved:☺️

**The right adjoint of an adjunction is fully faithful iff the co-unit is a natural isomorphism.**
{: .text-center .notice--info}

What does this theorem have to do with reflective subcategory again? Oh yes, the right adjoint in a reflective subcategory situation is precisely a fully faithful functor! This means that the adjunction co-unit yielded by a reflective subcategory is necessarily a natural isomorphism.
<a id="epia"></a>

## Epi-adjunction
Finally, recall from my [Sep 8 post]({{ site.baseurl }}{% post_url 2019-09-08-category-theory-notes-12 %}) that two categories can be compared for similarity if they are correlated by a pair of back-and-forth functors. In that post I mentioned **three graded levels of similarity** between categories: isomorphism (**strongest**), equivalence (**second best**), and adjunction (**weakest**). And recall that a useful method to check which level of similarity two categories enjoy is the **round-trip method**. That is,
- if any object in either of the two categories goes back to **itself** after a functorial round trip, then the two categories are isomorphic;
- if any object in either of the two categories goes back to **somewhere isomorphic to itself**, then the two categories are equivalent; and
- if any object in either of the two categories goes back to **its (co-)unit-based counterpart**, then the two categories are connected by adjunction.

In the above round-trip method we've treated both categories equally, in that we've consistently said "if any object in **either of the two categories** blah blah blah..." But does that cover all possible round-trip scenarios? Apparently not. For example, what if any object in one of the two categories goes back to itself while any object in the other category goes back to its (co-)unit-based counterpart? Or what if any object in one of the two categories goes back to its (co-)unit-based counterpart while any object in the other category goes back to somewhere isomorphic to itself?

Considering additional scenarios like the above, we actually have several more graded levels of similarity between categories. In particular, in relation to the reflective subcategory situation we have the following scenario:
- Any object in the reflective subcategory goes back to somewhere isomorphic to itself after the functorial round trip, while any object in the other category goes back to its (co-)unit-based counterpart.

This is a level of similarity worse than an equivalence of categories but better than a plain adjunction. It's called an **epi-adjunction** (see Marcel Erné 2004, "[Adjunctions and Galois Connections](https://link.springer.com/chapter/10.1007/978-1-4020-1898-5_1)") because when the scenario occurs between two poset categories the left adjoint is epic. In my dissertation this epi-adjunction scenario was **the** most important category-theoretic result that I had used.

## Takeaway
- A subcategory is a special type of category formed by removing some data from its parent category.
- The term subcategory is used similarly in linguistics and in mathematics, though the two disciplines define "subcategory" in different directions, one by adding data (linguistics) while the other by removing data (mathematics).
- Full and lluf subcategories respectively describe special jectivity situations on arrows and on objects.
- A reflective subcategory is a subcategory that is connected to its parent category via an adjunction, where the right adjoint is an inclusion functor.
- In an adjunction involving a reflective subcategory (or a category isomorphic to a reflective subcategory) the co-unit is a natural isomorphism.
- When an adjunction is a reflective subcategory situation (called an epi-adunction, especially in the context of posets), the two categories involved enjoy a level of similarity inferior to an equivalence of categories but superior to a plain adjunction.
