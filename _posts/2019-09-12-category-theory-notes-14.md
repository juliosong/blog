---
title: "Category theory notes 14: Yoneda lemma (Part 1)"
categories: [linguistics, mathematics]
tags: [category theory]
header:
  overlay_image: /assets/images/sky.jpg
  show_overlay_excerpt: false
  image_description: "A photo I took from the window of a plane."
  caption: "I took this photo from the window of a plane in 2014."
  teaser: /assets/images/sky.jpg
---

Awodey calls it "the single most used result" of category theory ([_Category Theory_](https://global.oup.com/ukhe/product/category-theory-9780199237180), p.&nbsp;185), Crole regards it as "an indispensable tool which every category theorist should carry in his kit and be able to use" ([_Categories for Types_](https://books.google.co.uk/books/about/Categories_for_Types.html?id=mHptq6sqJRIC&source=kp_book_description&redir_esc=y), p.&nbsp;63), and Leinster says if it were false "the world would look much more complex" ([_Basic Category Theory_](https://books.google.co.uk/books/about/Basic_Category_Theory.html?id=Q3vsAwAAQBAJ&source=kp_book_description&redir_esc=y), p.&nbsp;95). **Yes, that's just how significant the [Yoneda lemma](https://en.wikipedia.org/wiki/Yoneda_lemma) is!** Alongside its unanimous significance, however, is its notorious difficulty for beginners. Almost every textbook I've read has a message at the beginning of the chapter or section on the lemma (or really theorem) warning students that it's a challenging lesson ahead or that the material that follows will be heavy. The comment below from [StackExchange](https://math.stackexchange.com/q/37165) gives a relatable hint of how mind-bending the Yoneda lemma is:
>**Chris Taylor:** I have trouble following the category-theoretic statement and proof of the Yoneda Lemma. Indeed, I followed a category theory course for 4-5 lectures (several years ago now) and felt like I understood everything until we covered the Yoneda Lemma, after which point I lost interest.

So, those who manage to survive the Yoneda lemma can proudly call themselves "true categorists." 🤓

{% include figure image_path="/assets/images/yoneda-mountain.png" alt="An illustration of the difficulty level of the Yoneda lemma" caption="<em>Adventures in The Land of Category Theory</em>" %}

## Two Yonedas
It seems to me that **there are two Yoneda lemmas folded together**---just like there are three Beijings folded together in [Jingfang Hao](https://en.wikipedia.org/wiki/Hao_Jingfang)'s Hugo-award-winning sci-fi [novelette](https://en.wikipedia.org/wiki/Folding_Beijing)---**one is like zen while the other is like an assembly language.**<sup><a href="#fn1" id="ref1">1</a></sup> The zen-like Yoneda is crystal clear in its purpose and ambition, but it's only suitable for spiritual discussion; nothing down-to-earth can be done with its zen in mathematical practice. The assembly-language-like Yoneda, on the other hand, fleshes out the details of the lemma that are glossed over in its zen, but the details are so convoluted and multithreaded that novices will quickly lose direction in its logical and notational juggernaut. So, it'd be way too early for a beginner to feel relieved when meeting the zen-like Yoneda 🧘 and think "well it's not as hard as they say"---wait till you see its other face 🧟‍♀️!

What's my own experience with the Yoneda lemma? It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard. It's hard...😝

And like many other parts of category theory. The way it's taught in textbooks doesn't really help reduce the difficulty. In fact I realize in hindsight that sometimes I got stuck not because of the intrinsic complexity of the lemma (it **is** complex of course!) but because of the ambiguous notation. Notational ambiguity may be easily filtered out by experts, but they can be really frustrating for beginners.

So, in this and the next two posts I'll try to explain the Yoneda lemma in a way that has been helpful to myself. Hopefully it'll also help you if you happen to be puzzled by the same questions. For ease of later reference I'll give the lemma up front. <a id="lemma"></a>The following version is taken from Awodey's textbook:
>**Yoneda lemma:** Let $\mathbb{C}$ be locally small. For any object $C\in\mathbb{C}$ and functor $F\in\mathbf{Sets}^{\mathbb{C}^{op}},$ there is an isomorphism
\\[ Hom(yC, F) \cong FC \\]
which, moreover, is natural in both $F$ and $C.$ (Category Theory, pp.&nbsp;188--189)

<a id="yofun"></a>

The $y$ in this definition is the **Yoneda functor** (aka **Yoneda embedding**), which is defined as follows:
>The Yoneda embedding is the functor $y\colon \mathbb{C}\rightarrow\mathbf{Sets}^{\mathbb{C}^{\mathrm{op}}}$ taking $C\in\mathbb{C}$ to the contravariant representable functor
\\[ yC = \mathrm{Hom}\_\mathbb{C}(-,C)\colon \mathbb{C}^{\mathrm{op}} \rightarrow \mathbf{Sets} \\]
and taking $f\colon C\rightarrow D$ to the natural transformation
\\[ yf = \mathrm{hom}\_\mathbb{C}(-,f)\colon \mathrm{Hom}\_\mathbb{C}(-,C)\rightarrow\mathrm{Hom}\_\mathbb{C}(-,D), \\]
... One should thus think of the Yoneda embedding $y$ as a "representation" of $\mathbb{C}$ in a category of set-valued functors and natural transformations.... (Category Theory, p.&nbsp;187)


## The zen-like Yoneda
First let's see the Yoneda lemma through the "zen lens." (For now ignore the definition above.) Mathematicians like talking of a "Yoneda philosophy," which is sometimes smartly conveyed in the following Dutch proverb:<sup><a href="#fn2" id="ref2">2</a></sup>
>Zeg me wie uw vrienden zijn, dan zeg ik wie u bent.<br>
"Tell me who your friends are, and I will tell you who you are."

Some people also like citing a [particle accelerator analogy](https://mathoverflow.net/a/3223), allegedly due to Ravi Vakil:
>**Theo Johnson-Freyd:** You work at a particle accelerator. You want to understand some particle. All you can do are throw other particles at it and see what happens. If you understand how your mystery particle responds to all possible test particles at all possible test energies, then you know everything there is to know about your mystery particle.

In her [blog post](https://www.math3ma.com/blog/the-yoneda-perspective) Tai-Danae Bradley nicely states the above philosophy as "the Yoneda perspective":
> Mathematical objects are completely determined by their relationships to other objects.

Now the gist of the Yoneda philosophy should be clear. It simply says that we can learn everything about an object by studying its interaction with all other objects in its categorical locality. But exactly how? The philosophy is more spiritual than mathematical and has absolutely no resemblance to the formal definition <a href="#lemma">above</a>.

For the remaining part of this article see my next post "[Category theory notes 15: Yoneda lemma (Part 2)]({{ site.baseurl }}{% post_url 2019-09-13-category-theory-notes-15 %})."

<hr>
<div style="font-family: serif; font-size: 0.8em;">
<a id="fn1">1.</a><sup><a href="#ref1" title="Jump back to footnote 1 in the text.">↩</a></sup> This assembly language analogy is inspired by Milewski's statement that &#8220;set theory [is] the assembly language of mathematics&#8221; (<a href="https://books.google.co.uk/books/about/Category_Theory_for_Programmers.html?id=ZaP-swEACAAJ&redir_esc=y"><em>Category Theory for Programmers</em></a>, p.&nbsp;153).<br>
<a id="fn2">2.</a><sup><a href="#ref2" title="Jump back to footnote 2 in the text.">↩</a></sup> This particular version of the quote is from Boisseau &amp; Gibbons's 2018 article &#8220;<a href="https://www.cs.ox.ac.uk/jeremy.gibbons/publications/proyo.pdf">What you needa know about Yoneda</a>.&#8221;
</div>
