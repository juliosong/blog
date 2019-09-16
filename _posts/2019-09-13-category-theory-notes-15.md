---
title: "Category theory notes 15: Yoneda lemma (Part 2)"
categories: [linguistics, mathematics]
tags: [category theory]
header:
  overlay_image: /assets/images/sky.jpg
  show_overlay_excerpt: false
  image_description: "A photo I took from the window of a plane."
  caption: "I took this photo from the window of a plane in 2014."
  teaser: /assets/images/sky.jpg
---

In the previous post "[Category theory notes 14: Yoneda lemma (Part 1)]({{ site.baseurl }}{% post_url 2019-09-12-category-theory-notes-14 %})" I began writing about IMHO the most challenging part in basic category theory, the Yoneda lemma. I commented that there seemed to be two Yonedas folded together: one zen-like and the other assembly-language-like. I've already specified that the zen-like Yoneda is. In this post I'll continue to write about my personal feelings about the lemma's [definition]({{ site.baseurl }}{% post_url 2019-09-12-category-theory-notes-14 %}#lemma) as well as set out to decipher the assembly-language-like Yoneda.🏃‍♂️

## How I felt about the lemma
The huge gap between the actual Yoneda lemma and its zen-like philosophy is partly due to the terseness of the mathematical language. The formulation of the lemma is so condensed that outsiders simply don't know where to start... Below is more or less what I thought when I first encountered it.

- Okay I know $\mathbb{C}$ must be a category based on my previous experience with category theory, and I know what "locally small" means (see my [Aug 29 post]({{ site.baseurl }}{% post_url 2019-08-29-category-theory-notes-6 %}#sizes) if you need a reminder), even though I'm not sure why the condition is needed here.
- $C\in\mathbb{C}$ is easy to understand, and $\mathbf{Sets}^{\mathbb{C}^\mathrm{op}}$ looks formidable---because I fear exponentiation and $op$---but thank God it's explicitly declared that $F$ is a functor, which means the formidable chunk must be a category of functors. With this mental aid now I think I'm beginning to see through the notation---it just denotes the category of functors between the opposite category of $\mathbb{C}$ and $\mathbf{Sets}$.
- But what's $\mathrm{Hom}(yC, F)$? I've seen "hom" when learning hom-sets and hom-functors but why is "Hom" here capitalized? And why isn't the ambient category of the hom-thingy given?<a id="presheaves"></a>
- Okay, I'm not afraid. I'll try to understand it. $C$ is an object in $\mathbb{C}$ and $y$ is the [Yoneda functor]({{ site.baseurl }}{% post_url 2019-09-12-category-theory-notes-14 %}#yofun), whose output is a presheaf (a [presheaf](https://en.wikipedia.org/wiki/Presheaf_(category_theory)) is just a fancy name for a $\mathbf{Sets}$-valued contravariant functor), so $yC$, the application of the Yoneda functor on the $\mathbb{C}$-object $C,$ should be a presheaf just like $F$. So the formidable chunk $\mathbf{Sets}^{\mathbb{C}^\mathrm{op}}$ is just the category of presheaves. Thank God I haven't forgotten what a presheaf is...
- But wait, where's the isomorphism from?! It seems to be out of nowhere... How random!
- And the lemma mentions "natural," which seems to suggest the isomorphism is part of a natural isomorphism, but where's the natural transformation? Why isn't it mentioned at all? Does the author think all readers are clever enough to be able to guess stuff he leaves out?
- Okay perhaps I'm not among the author's target audience but that's fine. I'll just guess my way through... Since the isomorphism is natural in $F$ and $C$, these two must be the "blanks" (see my [Sep 9 post]({{ site.baseurl }}{% post_url 2019-09-09-category-theory-notes-13 %}#adjunction-blank) if you don't know what natural transformation blanks are) in the natural transformation, like this: $\mathrm{Hom}(y(-), \bullet)\Rightarrow \bullet(-).$
But the right-hand functor is so embarrassing...
- And additionally $\bullet(-)$ doesn't feel like a functor---it feels more like an object in the target category of the functor. But if I remove $(-)$ from the right-hand side then should I also remove it from the left-hand side? That doesn't feel right.
- And on that note the left-hand side doesn't feel like a functor either... So the isomorphism in the Yoneda lemma, despite its naturality, may not be part of a natural isomorphism after all...
- Ahhhh my mind is gonna explode! I'll go for a nap.

And the above line of thought repeated itself several times over a number of days, all in vain.😔

## Deciphering the assembly-language-like Yoneda
But of course I didn't give in to 米田さん. After many days of attempts, most of which failed, I finally understood the assembly-language face of the Yoneda lemma.

### The background natural transformation  
So, as it turned out, I hadn't been wrong in assuming there was a natural transformation hidden behind the [Yoneda isomorphism]({{ site.baseurl }}{% post_url 2019-09-12-category-theory-notes-14 %}#lemma). I just didn't get it right.🤦‍♂️ The correct way to think about this is: Since the isomorphism is natural in two variables, the natural transformation should have **both variables** reflected in its source category. In other words, its source category should be a **product category,** with each component holding a variable. Now, to get the right source category, we simply need to ask what categories the two variables are respectively objects of.

- The ambient category for $F$ is the category of presheaves on $\mathbb{C},$ namely the formidable chunk $\mathbf{Sets}^{\mathbb{C}^\mathrm{op}}.$
- The ambient category for $C$ is just $\mathbb{C}.$

So, the product category serving as the source of the two functors involved in the desired natural transformation should be $\mathbf{Sets}^{\mathbb{C}^\mathrm{op}} \times \mathbb{C}.$

The next question to ask is, What's the target of the two functors involved in the desired natural transformation? This question can be answered by studying the Yoneda isomorphism again. If it's yielded by a natural transformation---namely, if it's a **component** of some natural transformation---then it should be a morphism (more exactly an isomorphism) living in the desired target category.
- What's the ambient category of $FC$? Since $F$ is a presheaf, it should lift objects to $\mathbf{Sets},$ so the ambient category of $FC$ is just $\mathbf{Sets}.$
- What's the ambient category of $\mathrm{Hom}(yC, F)$? In my failed trials above I had wondered whether this was a hom-set or a hom-functor, but when the two variable blanks in $\mathrm{Hom}(y(-), \bullet)$ are both filled (i.e., by $C$ and $F$) the result can't be a functor anymore but a fully specified **hom-set**. Therefore, the ambient category of $\mathrm{Hom}(yC, F)$ is also $\mathbf{Sets}.$

I'd like to say a few more words on this hom-set (because it had given me a headache). While $\mathrm{Hom}(y(-), \bullet)$ may be a hom-functor (because a functor is like a function, which has unfilled argument slots), $\mathrm{Hom}(yC, F)$ must be a hom-set (because it's the result of applying the hom-functor to two specific arguments). And the hom-set is just the set of arrows between $yC$ and $F.$ Since $yC$ and $F$ are both presheaves, namely functors of a particular kind, arrows between them are just natural transformations. Hence, the hom-set in question is actually **a set of natural transformations**.

To sum up the above results, now we can confirm that the background natural transformation giving rise to the Yoneda isomorphism is the following one:
\\[ \mathbf{Sets}^{\mathbb{C}^\mathrm{op}} \times \mathbb{C} \xrightarrow{\cong} \mathbf{Sets}. \\]
N.b. this is a natural isomorphism (as the specially shaped arrow indicates) just like the natural isomorphism we saw in adjunction (see my [Sep 9 post]({{ site.baseurl }}{% post_url 2019-09-09-category-theory-notes-13 %}#ni) if you want to review what that is).

Have you realized its specialness? For me what hindered me in realizing how special this natural transformation was again was the annoying $op$---but let's temporarily ignore it since it's really just a "mirror" on $\mathbb{C}.$ Abstracting away from the difference between $\mathbb{C}$ and $\mathbb{C}^\mathrm{op},$ the natural transformation is in the format of an evaluation map:
\\[ eval: Z^Y \times Y \rightarrow Z. \\]
This $eval$ map simply means "if you give me a function from $Y$ to $Z$ and a $Y$ I can return a $Z$." In formal logic this is just the famous [_modus ponens_](https://en.wikipedia.org/wiki/Modus_ponens): if both $P \rightarrow Q$ and $P$ are true, then $Q$ is true.

Having realized the specialness of the "Yoneda natural transformation," if I may call it this way, now we can also easily understand the trick of $FC$ and the "embarrassment" of the functor $\bullet(-)$---it's just a plain implementation of $eval,$ and its both variable slots are blank simply because **that's how evaluation works**... The evaluation map applies a function to its argument. When both are blanks, the entire map is also blank.

In sum, the Yoneda natural transformation is just a transformation between two ways to utilize the two arguments of an evaluation function. Of course, only one way is the actual evaluation map, while the other way is just a "creative" exploitation of the two arguments involved in the evaluation map. <a id="yonedasq"></a>Below I display the naturality square (I use subscript square brackets on the left-hand side to indicate argument types in case they become easy to forget):

![naturality square of Yoneda transformation](/assets/images/yoneda-square.pdf)

Now the assembly-language-like Yoneda lemma should be clear, at least on the conceptual level. It just says that the above-displayed natural transformation is a natural isomorphism (which I've indicated by the two-sided arrows). And that's it!😃

For the remaining part of this article see my next post "[Category theory notes 16: Yoneda lemma (Part 3)]({{ site.baseurl }}{% post_url 2019-09-13-category-theory-notes-16 %})."
