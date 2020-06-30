---
title: "A new application of category theory in linguistics  (part 2)"
categories: [linguistics, mathematics]
tags: [category theory, generative grammar]
header:
  overlay_image: /assets/images/act2020.jpg
  show_overlay_excerpt: false
  image_description: "a sketch of a light bulb on a note pad"
  caption: "credit: [AbsolutVision](https://unsplash.com/@freegraphictoday?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/idea?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText))"
  teaser: /assets/images/act2020.jpg
toc: true
---

In the [previous post]({{ site.baseurl }}{% post_url 2020-06-28-a-new-application-of-category-theory-in-linguistics-part-1 %}) I laid out the disciplinary background of my application of category theory in linguistics in more detail (than I had done in my [explainer video](https://www.youtube.com/watch?v=dzEPH8K4CaQ)). In this post I continue to introduce my category-theoretic modeling of the human language grammatical type system. And as in the previous post, I will still abstract away from technical details (which you can find either in my [extended abstract](https://www.juliosong.com/doc/Song2020ACTabstract.pdf) or, in fuller forms, in my [dissertation](https://www.repository.cam.ac.uk/handle/1810/297789)) and focus on my motivation and source of inspiration instead.

## Layered abstraction
In my discussion so far we have met three concepts about grammatical types: (i) the types themselves, (ii) the extended projections building on individual types, and (iii) the various abstract relations building on extended projections. The three concepts present us with a scenario of layered abstraction, which is also what has inspired my application of category theory in my research. As Fong & Spivak point out in their recent textbook on applied category theory---[*Seven Sketches in Compositionality*](https://www.goodreads.com/book/show/39681351-seven-sketches-in-compositionality)---category theory is "unmatched in its ability to organize and layer abstractions."

In fact, the layered-abstraction line of thought can go further. We can think about the human language grammatical type system at **five levels of abstraction** instead of three:

1. The level of an individual type (e.g., V[erb], T[ense], or D[eterminer])
2. The level of a certain structured set of types (e.g., an extended projection)
3. The level of a certain structured set of extended projections (e.g., a language's grammatical type system may have a verbal extended projection, a nominal one, and an adjectival one, with some connections between them)
4. The level of a structured set of all possible versions of the set from Level 3 (e.g., some languages may not have an adjectival extended projection, and some may have different verbal or nominal types)
5. The level of all grammatical types, including both types inside the structures of Levels 1–4 and types outside them, such as [logical connectives](https://en.wikipedia.org/wiki/Logical_connective) and syntactic "[roots](https://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780199665266.001.0001/acprof-9780199665266)," both of which are essentially "[syncategorematic](https://en.wikipedia.org/wiki/Syncategorematic_term)."

That may sound like a mouthful, but the main point is simple enough to state in one sentence: **From Level 1 to Level 4, the "output" at each level is the "input" at the next level.** So, I am basically just wrapping individual grammatical types with three extra layers of structure. Level 5, on the other hand, is somewhat different and strictly speaking does not belong to the same continuum of abstraction. I will discuss this below.

## Ontological vs. derivational structure
The five abstraction levels above essentially represent **two ways to structure the grammatical type inventory**. Levels 1–4 together form an *ontological* structure, while Level 5 is the basis of a *derivational* structure. The derivational structure is absent from Levels 1–4, because the inventory referenced by syntactic derivation is not yet complete at those levels---remember that some grammatical types fall outside the extended projection–based structures. Likewise, the ontological structure is absent from Level 5. Well, strictly speaking they are still there in the background, but I have chosen to abstract away from them. The abstraction process does not destroy or lose information but merely encapsulates some information and hides it from our field of vision, depending on what the design purpose of the abstraction level is.

Despite the discontinuity, I have put Level 5 at the top of my ladder of abstraction for two reasons. First, it is the most abstract level in the sense that the ontological structures from Levels 1–4 are all hidden in the background by design. Second, it is a superset of the set of grammatical types from Levels 1–4 because it also contains types that fall outside the extended projection–based structures.

What I mean by the ontological vs. derivational distinction is, for example, when we say that there is an order relation among grammatical types, we are talking about the organization of grammatical types within the lexicon, whereas when we say that if we combine V and DP as input we get VP as output, or that if we apply the type $e\rightarrow t$ to the type $e$ we get the type $t$, we are talking about things that happen to grammatical types when we feed them to syntactic computation. As such, this distinction is in accord with the lexicon vs. syntax distinction mentioned in the previous post.

Under my layered-abstraction perspective, previous applications of category theory in linguistics have all targeted Level 5, because they are essentially all building derivation systems with category-theoretic tools (such as monoidal categories). By comparison, **the gist of my own application is that category theory can actually help us model the human language grammatical type system in a more complete fashion, encompassing both its derivational side and its ontological side.** That is also the reason why I have chosen to marry category theory and Chomskyan syntax (apart from the fact that I happen to be trained in the latter area)---because it is more or less the only grammatical theory on the market that is both suitably formal in nature and has actively engaged with the multifarious grammatical types attested in world languages. So, if we want to use category theory to model the grammatical type inventory, results from the Chomskyan framework provide a decently assembled inventory (equipped with some preliminary structuring, such as the extended projections) for us to begin with.

That being said, I am not saying that we should exclusively rely on the Chomskyan framework. Integrating ideas from different frameworks is perfectly feasible in the layered-abstraction context. For example, categorial grammar and its current category-theoretic development is a valid alternative to Chomskyan syntax at Level 5, at least in principle---which theory is superior or more adequate is a separate issue. Similarly, the feature theory from head-driven phrase structure grammar provides useful insights for Level 1 (i.e., concerning how to formally define individual grammatical types).

## A sketch of the modeling
My category-theoretic modeling of the human language grammatical type system is basically a straightforward "categorification" of three out of five levels of abstraction mentioned above (there is no category-theoretic structure at the first level, and I have nothing new to say about the fifth level). I briefly describe the categorification below. There is no advanced mathematical notions involved---at least in my work progress so far---but even the most basic category-theoretic ideas prove to be very useful.

### Level 2: a poset category
An extended projection, with its order relation, can be conceived as an ordered set. More specifically, it can be conceived as a **partially ordered set**, since there may be "incomparable" grammatical types in human language; namely, types that are closely related in syntactic function and compete for the same position on the syntactic tree. Such mathematically incomparable types are sometimes referred to as "flavored" in linguistics.

Since a poset can be viewed as a category, here we obtain our first category-theoretic structure for the grammatical type inventory right away. Its objects are the individual grammatical types in an extended projection, and its morphisms are instances of the partial order relation among those types. For example:

(1) {V$_1$, V$_2$, V$_3$} $\rightarrow$ Appl $\rightarrow$ v $\rightarrow$ Voice $\rightarrow$ Asp $\rightarrow$ Mod $\rightarrow$ T $\rightarrow$ C $\rightarrow$ {Foc$_1$, Foc$_2$} $\rightarrow$ Top

(I use curly brackets to hold incomparable types, and note that this example is merely meant to illustrate the shape of an extended projection poset---I have no theoretical commitment to the concrete types or ordering in it.)

**A caveat on the incomparability issue:** Certain positions in the extended projection are incompatible with incomparable elements. This is the theme in [my submission to ACT2020](https://www.juliosong.com/doc/Song2020ACTabstract.pdf), where I used the [adjoint functor theorem](https://ncatlab.org/nlab/show/adjoint+functor+theorem) to prove that there is no way to have "flavored phase heads" (a particular kind of grammatical type) in human language if we subscribe to the extended projection–based structure of the grammatical type inventory. I will return to this point below.

### Level 3: a category of posets
Since each extended projection can be viewed as a poset, a set of extended projections, such as the one in (2), can be viewed as a category of posets (more exactly a subcategory of the category of posets).

(2) {EP-N, EP-V, EP-A}

The objects of such a category are the individual extended projections (here represented by their major-part-of-speech labels), and its morphisms are functions---or functors if we keep viewing each extended projection as a category---that formalize some of the higher-order concepts about extended projections (i.e., those pertaining to the third level of abstraction).

In particular, if we subscribe to the "universal spine" or some equivalent thereof mentioned in the previous post, which postulates an abstract hierarchy of concepts (i.e., a blueprint) that underlies each and every extended projection, then each category of extended projections at Level 3 should also have an additional object. Thus, (2) should more exactly be (3), where I use EP$_0$ to represent the universal spine, which is mathematically a very short chain, such as the one in (4).

(3) {EP-N, EP-V, EP-A, EP$_0$}

(4) EP$_0$ := classification $\rightarrow$ point-of-view $\rightarrow$ anchoring $\rightarrow$ linking (Wiltschko 2014)

Among the higher-order concepts that can be formalized at Level 3, so far I have only explored the cross-major-part-of-speech parallelism in detail. Specifically, my exploration has been inspired by the category-theoretic idea of **graded levels of similarity** between categories (see [this paper](https://www.sciencedirect.com/science/article/pii/S0168010215002989) for a previous application of this idea in neuroscience).

As it turns out, once we take into account all linguistic factors that need to be considered, the degree of similarity between any two extended projections is not very high, though it is definitely there. And if we want to model this similarity in category-theoretic terms at all, it can only be via an **adjoint situation**. After showing that there can be no direct adjunction between any two extended projections that is linguistically interesting or meaningful---by "linguistically meaningful" I mean it doesn't violate linguistic principles or lead to counterintuitive consequences---I concluded in my dissertation that the best and only category-theoretic representation of the cross-major-part-of-speech we could get was a mediated adjoint situation (mediated by the universal spine). That is, any two extended projections have a conceptual parallelism in that they both form an adjunction with the same universal spine. This mathematical situation is in line with linguists' intuition, since the universal spine hypothesis was proposed to account for the observed parallelism in the first place.

In addition, if we want to maintain the mediated adjunction and hence the parallelism at all, the two extended projections in question cannot be of any random shape. The adjoint functor theorem dictates that certain positions (which coincide with the "phase positions" in Chomskyan syntax) cannot accommodate incomparable grammatical types. This is how I reached the conclusion in my submission to ACT2020 that category theory helps linguists rule out flavored phase heads---especially the flavored little v's, which have been in regular use but are subject to much dispute.

In short, my reasoning is that if we want to have a *linguistically meaningful* adjunction between any extended projection and the universal spine (or some equivalent thereof) at all, then no flavored phase heads can exist. Of course, there is also the possibility that my entire layered-abstraction theory about the grammatical type system and its categorification are wrong. My point here is merely that if my modeling is on the right track, then one of the predictions it makes is that phase heads cannot be flavored (I called this **the uniqueness of phase heads theorem** in my ACT2020 submission).

### Level 4: a category of language varieties
At the fourth level of abstraction, the set of extended projections at the third level becomes a ground unit. Since the major parts of speech in a language variety together with all the grammatical types they subsume essentially cover all the structured grammatical types of the language variety, each ground unit at Level 4 effectively picks out a particular language variety. Correspondingly, one way to categorify this level of abstraction is to view its objects as language varieties and its morphisms as various functional connections between the language varieties.

The particular kind of connection I investigated in my dissertation was that of the inheritance/subsumption relation based on how fine-grained the extended projections of the relevant language varieties were---a notion I referred to as "granularity level." I will refrain from going into the detail here because Level 4 has nothing to do with my submission to ACT2020 and also because this post is already long enough. [Here](https://www.juliosong.com/doc/Song2019SynLabOct.pdf) is a previous presentation of mine on the notion of granularity level, which is not couched in category-theoretic terms but includes sufficient background information on the presence and significance of granularity in linguistics.

## Final remark
A main takeaway message of my study is that the category-theoretic perspective on the (ontological side of) human language grammatical type system is not complex at all. In fact, it only uses the most basic category-theoretic concepts. Nevertheless, the extent to which linguistics can benefit from those concepts and their implications cannot be downplayed. For example, the various extended projection–based ideas I mentioned have been around in the field for long, but they have largely remained informal ideas, mostly mentioned in passing independently of one another. With the category-theoretic perspective, however, we can now begin to integrate them in the same theoretical context and in a formally explicit way. Besides, since the category-theoretic perspective and the layered-abstraction perspective are both about the entire grammatical type system, the potential benefits they may bring to theoretical linguistics are not limited to my immediate concerns in this study. The category-theoretic exploration of the grammatical type system (including both its ontological side and its derivational side) has the potential to become an enterprise of its own.

-- The End --

([Here](https://www.juliosong.com/doc/Song2020ACTabstract.pdf) is my extended abstract for ACT2020 if you are curious about my particular case study on phase heads, which is a specific result at the third level of abstraction.)
