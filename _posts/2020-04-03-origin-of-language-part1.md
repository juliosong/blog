---
title: "Where is language from? (Part 1)"
categories: [linguistics]
tags: [origin of language, evolution, gene]
header:
  overlay_image: /assets/images/evolution.png
  show_overlay_excerpt: false
  image_description: "the evolution path from ape to man"
  caption: "Evolution path of homo sapiens (Image by [LAURENCE ROUAULT](https://pixabay.com/zh/users/laurencerouault-8646167/?utm_source=link-attribution&utm_medium=referral&utm_campaign=image&utm_content=3579185) on [Pixabay](https://pixabay.com/zh/?utm_source=link-attribution&utm_medium=referral&utm_campaign=image&utm_content=3579185))"
  teaser: /assets/images/evolution.png
---

A while ago I came across a website for a [Genetic Literacy Project](https://geneticliteracyproject.org). The slogan of the Project is "science not ideology," and its [goal](https://geneticliteracyproject.org/mission-financials-governorship/) is to promote science literacy and aid people in understanding the societal implications of genetic engineering. I'm not a big fan of genetic engineering, especially given [recent scandals](https://www.nature.com/articles/d41586-019-00673-1). What caught my attention was [a short article](https://geneticliteracyproject.org/2020/01/30/spoken-language-doesnt-leave-fossils-did-humans-ability-to-speak-arise-in-an-instantaneous-hominin-mutation/?fbclid=IwAR2HIBxniFwsePN2bsHiq1Tl1vKGjcG3VHN_vrdWXALWDvAVjJlZWkMEyXM) posted on the website by Ross Pomeroy ([@SteRoPo](https://twitter.com/steropo?lang=en))---who runs the [RealClearScience](https://www.realclearscience.com) website by the way---about [a new paper](https://www.nature.com/articles/s41598-019-57235-8) in _Nature Scientific Reports_ on the origin of language (de Boer, Thompson, Ravignani & Boeckx 2020). The paper argues based on evolutionary dynamics grounds that language has more likely evolved step by step rather than via a single genetic mutation.

>Our results cast doubt on any suggestion that evolutionary reasoning provides an independent rationale for a single-mutant theory of language.<br>
><span style="text-align: right; display: block;"> --- [de Boer et al. (2020)](https://www.nature.com/articles/s41598-019-57235-8)</span>

By "a single-mutant theory" the authors mean the theory of [Noam Chomsky](https://en.wikipedia.org/wiki/Noam_Chomsky), or "the Chomskyan evolutionary conjecture."

## The Chomskyan evolutionary conjecture
This conjecture is based on the assumption that what distinguishes human language from animal communication most fundamentally is hierarchical syntactic structure; that is, the underlying grammatical structures of human language sentences are more about category embedding (often represented by brackets) than about string concatenation. Thus, when a syntactician sees a sentence like _"Colorless green ideas sleep furiously."_ what he sees is (1a) instead of (1b).

(1) a. [ [ [ adj ] [ [ adj ] [ n ] ] ] [ [ v ] [ adv ] ] ]<br>
b. `"Colorless" + " " + "green" + ... + "furiously" + "."`

The essence of hierarchical syntactic structure, according to Chomsky, is a basic combinatorial operation called [_merge_](https://en.wikipedia.org/wiki/Merge_(linguistics)), which creates a set out of two elements.

(2) merge(a, b) => \{a, b\}

Hierarchical structures are built by iterated application of merge.

(3) merge(\{a, b\}, c) => \{\{a, b\}, c\} <br>
👉 _or [ [ [ a ] [ b ] ] [ c ] ] in bracketing format_

The bracketing format can be further converted to [tree](https://en.wikipedia.org/wiki/Parse_tree) format (a type of [graph](https://en.wikipedia.org/wiki/Graph_(discrete_mathematics))), with each pair of brackets corresponding to a [vertex](https://en.wikipedia.org/wiki/Vertex_(graph_theory)) and each instance of the immediate dominance (i.e., set membership) relation corresponding to an [edge](https://en.wikipedia.org/wiki/Glossary_of_graph_theory_terms#edge).

(4) <img style="vertical-align:top" src="/assets/images/syntax-tree.pdf" alt="a syntactic tree">

A basic tenet of Chomsky's syntactic theory is: however complex a natural language sentence is, it ultimately always boils down to this simple operation "merge." This extremely simple way to define human language syntax "greatly eases the explanatory burden for evolutionary analysis" (Bolhuis, Tattersall, Chomsky & Berwick 2014), because once the human mind is equipped with merge, it is syntax-ready.

>Evolutionary analysis can thus be focused on this quite narrowly defined phenotypic property, **merge** itself, as the chief bridge between the ancestral and modern states for language.<br>
><span style="text-align: right; display: block;"> --- [Bolhuis et al. (2014)](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1001934)</span>

As to how merge came about in the first place, Chomsky's position is that it is not a result of the kind of slow, incremental process commonly associated with evolution but rather a recent and rapid emergence; in other words, it is a mutation. For more detail about this conjecture I recommend the recent MIT monograph coauthored by Berwick and Chomsky entitled [_Why Only Us?_](https://mitpress.mit.edu/books/why-only-us)

## Alternative voices
Being a linguistics student means I've had the chance of hearing/reading expert opinions on the origin of language multiple times. Indeed, Cambridge is a nice and tolerant place for open discussions on huge and controversial topics like this one. Sometimes students are too shy to utter their opinions, but the scent of interdisciplinary curiosity is clearly in the air.

I still remember attending a [Philological Society](http://www.philsoc.org.uk/default.asp) talk on the emergence of syntax in my first year of PhD and going to an Evolution of Language reading group in my second year. I got more spiritual galvanization (like "Wow, this is a cool area!") than academic progress from both events---mainly due to my lack of previous knowledge---but they did keep me thinking about language from a biological/evolutionary perspective from time to time throughout my stay at Cambridge.

I also notice an [origin of language section](https://www.darwinproject.ac.uk/commentary/human-nature/origin-language) on the website of the Darwin Correspondence Project (a Cambridge research team), though for some reason linguistics isn't listed as a currently-engaging discipline there...👀

>Debates about the origin of language are still ongoing. ... Such questions, addressed in a variety of scientific disciplines, such as **neurology, paleoanthropology, and animal psychology**, build upon the work of Darwin and his contemporaries, while taking that work in new directions.<br>
><span style="text-align: right; display: block;"> --- [Darwin Correspondence Project](https://www.darwinproject.ac.uk/commentary/human-nature/origin-language)</span>

But anyway, the wide attention the issue of language origin has drawn to itself means that the Chomskyan conjecture can't be the only voice out there---in fact it's not even the mainstream view. According to [Wikipedia](https://en.wikipedia.org/wiki/Origin_of_language) "a majority of linguistic scholars as of 2018 hold continuity-based theories"; that is, pro-_gradual_-evolution (or "gradualist") theories. The following slide from the Institute of Southern Punjab Multan presents an interesting picture.

{% include figure image_path="/assets/images/punjab-slide.png" alt="screenshot of a slide" caption="a slide showing various theories on the origin of language (source: [slideshare.net](https://www.slideshare.net/sabiraqamar1/origin-of-language))" %}

Out of the six postulated sources of human language listed in the slide, only two endorse a sudden-development view---the divine source (as in the Bible) and the genetic source (as in Chomsky's conjecture)---while all the rest are gradualist. Granted, we can't take an ayes-have-it attitude towards scientific debates ("[truth always rests with the minority](https://uncommondescent.com/intelligent-design/truth-rests-with-the-minority/)" as [Søren Kierkegaard](https://en.wikipedia.org/wiki/Søren_Kierkegaard) once said), but suddenists do need to come up with more solid evidence than faith- or conjecture-based argumentation in order to win the wider audience's hearts and to defend themselves against incessant criticisms, not all of which are unreasonable.

><span style="font-style:normal;">
**Pinker & Bloom** in [_Behavioral and Brain Sciences_](https://www.cambridge.org/core/journals/behavioral-and-brain-sciences/article/natural-language-and-natural-selection/CDD84686D58AF70E3D2CB48486D7940B) (1990):</span><br>
><span style="display:inline-block; padding-top:6px; padding-bottom:6px;">If a current theory of language is truly incompatible with the neo-Darwinian theory of evolution, one could hardly blame someone for concluding that it is not the theory of evolution that must be questioned, but the theory of language.</span><br>
><span style="font-style:normal;">ℹ️ [Pinker](https://stevenpinker.com) and [Bloom](https://psychology.yale.edu/people/paul-bloom) argue for a natural selection–based (i.e., gradualist) account of language origin despite their sympathies with Chomsky's generative grammar.</span>

><span style="font-style:normal;">**Ben James** on [The Atlantic](https://www.theatlantic.com/science/archive/2018/06/toolmaking-language-brain/562385/) (2018):</span><br>
><span style="display:inline-block; padding-top:6px; padding-bottom:6px;">Chomsky’s position is such a brazen refutation of known evolutionary processes that Kolodny, Stout, and many of their colleagues aren’t sure how to engage with it. Stout claims that Berwick’s refutation of his research misses the mark entirely. Ultimately ... he expects the positions of Berwick, Chomsky and other formalist linguists to find a sort of synthesis with his own views on language, but he doesn’t see agreement occurring anytime soon.</span><br>
><span style="font-style:normal;">ℹ️ [Stout](http://cmbc.emory.edu/about/cmbc%20faculty%20and%20staff/dietrich-stout.html) endorses the [tool-making](https://www.semanticscholar.org/paper/Stone-tools%2C-language-and-the-brain-in-human-Stout-Chaminade/6af3a07da20b540add5fbd0c1e9b667f06f3498e) or more exactly "[technological pedagogy](https://benjamins.com/catalog/is.17033.sto)" hypothesis and [Kolodny](https://sites.google.com/view/oren-kolodny-homepage/home) further puts forward a "[hijacking](https://royalsocietypublishing.org/doi/full/10.1098/rstb.2017.0052)"- or [exaptation](https://en.wikipedia.org/wiki/Exaptation)-based---though still gradualist---theory of language origin.</span>

But coming up with solid evidence is difficult. As [Ray Jackendoff](https://ase.tufts.edu/cogstud/jackendoff/) writes on the [Linguistic Society of America](https://www.linguisticsociety.org/content/how-did-language-begin) website:
>The basic difficulty with studying the evolution of language is that **the evidence is so sparse**. Spoken languages don't leave fossils, and fossil skulls only tell us the overall shape and size of hominid brains, not what the brains could do.

Without hard evidence, though, the study of language origin is still a game of speculation at the end of the day---not substantially superior to what it was one and a half centuries ago, when speculations became so whimsical that the Linguistic Society of Paris (SLP) decided to ban discussions on the topic altogether.
>La Société n’admet aucune communication concernant, soit l’origine du langage soit la création d’une langue universelle. (The Society does not accept any communication concerning either the origin of language or the creation of a universal language.)<br>
><span style="text-align: right; display: block;"> --- ART. 2, [Status de 1866](http://www.slp-paris.com/spip.php?article5), SLP</span>

See [this](https://thebrain.mcgill.ca/flash/d/d_10/d_10_s/d_10_s_lan/d_10_s_lan.html), [this](https://freelanguage.org/general-language-info/linguistic-hypotheses-on-the-origins-of-language), and [this](https://en.wikipedia.org/wiki/Origin_of_language#Language_origin_hypotheses) page for <a id="wurruri"></a>some imaginative theories as well as [this](https://en.wikipedia.org/wiki/Mythical_origins_of_language) page for some mythical ones (my personal favorite is [the Wurruri story](https://en.wikipedia.org/wiki/Mythical_origins_of_language#Australia)🧟‍♀️). And also don't forget the once ambitious mission of finding the mother tongue of our species (such as [Nostratic](https://en.wikipedia.org/wiki/Nostratic_languages))! Not sure if that quest is still on but sometimes I find the idea cool.

{% include figure image_path="/assets/images/nyt-nostratic.png" alt="part of an old newspaper" caption="an [article](https://www.nytimes.com/1987/11/24/science/linguists-dig-deeper-into-origins-of-language.html) published on Nov 24, 1987, in New York Times (via [NYT time machine](https://timesmachine.nytimes.com/timesmachine/1987/11/24/086587.html?pageNumber=53))" %}

For the remaining content of this article see my next post ["Where is language from? (Part 2)"]({{ site.baseurl }}{% post_url 2020-04-03-origin-of-language-part2 %}).
