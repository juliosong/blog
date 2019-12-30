---
title: "Learning programming languages like natural languages: Is it a good idea?"
categories: [programming, linguistics, review]
tags: [education, efficiency, medium language]
header:
  overlay_image: /assets/images/code-screen.jpg
  show_overlay_excerpt: false
  image_description: "part of a dark computer screen with HTML code"
  caption: "A screen of code (Photo by [Florian Olivo](https://unsplash.com/@rxspawn?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/programming-language?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText))"
  teaser: /assets/images/code-screen.jpg
---

Recently I came across a short article in _Trends in Cognitive Sciences_ entitled "[The language of programming: a cognitive perspective](https://www.cell.com/trends/cognitive-sciences/fulltext/S1364-6613(19)30102-0)" (Fedorenko et al. 2019). The authors argue in it for a linguistically oriented path of programming education in schools---which is currently grouped with [STEM](https://en.wikipedia.org/wiki/Science,_technology,_engineering,_and_mathematics) disciplines---based on observed parallelisms between natural and programming languages. As they put it, "When you learn a programming language, you acquire a symbolic system that can be used to creatively express yourself and communicate with others." Indeed, if something's called a language and behaves like one, why not treat it like one?

## Programming language viewed linguistically
Now what's that supposed to mean? What is it that allows us to view programming languages linguistically? Take the familiar `hello world` program for example (the implementation below is in Python 3).

```python
print("Hello, world!")
```

The conventional way to understand this line of code is: `print()` is a function that takes a `string` argument and prints it to the terminal screen, and the line is a call to this function.

As we can see, this perspective, largely mathematical, is pretty neat, as it makes use of formal notions like "function" and "argument." From a communicative perspective, however, no such terminology is necessary, because the function call is just a command (in the everyday sense of the word) or order---or in linguistic terms, an [imperative clause](https://dictionary.cambridge.org/grammar/british-grammar/imperative-clauses-be-quiet). Natural languages have loads of imperative clauses, such as
- *Put on your shoes!*
- *Gimme five!*

So the above `print` statement can be translated into English as
- *Print "Hello, World!" to the screen!*

Every imperative clause presupposes a listener or addressee. So does the `print` clause. In this case the listener is just the computer, hence the conception that a programming language is a medium of human-computer interaction. Actually this idea has long been exploited, to varied degrees of success, as evidenced by the invention of programming-language-like artificial natural languages (such as [Lojban](https://en.wikipedia.org/wiki/Lojban)) and that of natural-language-like programming languages (such as [Shakespeare](https://en.wikipedia.org/wiki/Shakespeare_Programming_Language)). There's even a whole field called [natural-language programming](https://en.wikipedia.org/wiki/Natural-language_programming), though apparently its justifiability [isn't unanimous](https://www.cs.utexas.edu/users/EWD/transcriptions/EWD06xx/EWD667.html).

## Programming languages are limited languages
Needless to say, the human-computer interaction enabled by programming languages is much more limited than the human-human interaction enabled by natural languages. For example, programming instructions like `print` can only tell computers what to do, while imperative clauses in natural languages can also tell people what *not* to do, e.g.,
- *Don't be late!*

how to behave, e.g.,
- *Be quiet!*

or in certain languages, what a person *wishes* another person to do, e.g.,
- (Hungarian) *János kérte, hogy menjek.* 'John asked that I (should) go.'<br> (*menjek* is the imperative form of the verb *menni* 'to go')

None of the above meanings can be conveyed by quasi-imperative instructions in programming languages. We normally don't tell computers not to do something (which is pointless) or how to behave (computers usually behave themselves anyway), let alone make wishes to them. Therefore, these aspects of communication, while absolutely necessary in human-human interaction, are simply out of the question for human-computer interaction.

**Teaching or learning programming languages from a linguistic or communicative perspective is completely feasible, if no overkill.** That's because the inventory of grammatical phenomena one would come across in the most sophisticated programming language is still just a tiny subset of that in any natural language on Earth. To get a picture of this let's go over some of the grammatical layers in the verbal/clausal domain of one variety of human language: English.
- Predicate-argument core, e.g., *have lunch*
- Voice, e.g., *be fed*
- Aspect, e.g., *be having lunch*
- Tense, e.g., *had lunch*
- Modality, e.g., *would have lunch*
- etc.

Apparently none of the above categories except the first one (i.e., the predicate-argument core) exists in programming languages---and even that first category is a lot more simplified compared to the various predicate-argument relations in natural languages. For instance, many natural languages make [case](https://en.wikipedia.org/wiki/Grammatical_case) distinctions based on the particular types of structural or semantic relations between the predicate and the argument. The example below is from German, another variety of human language.
- *<span style="color:red">Der Lehrer</span> erklärt <span style="color:green">dem Schüler</span> <span style="color:brown">die Regel</span>.* 'The teacher explains the rule to the student.'

There are three noun phrases in the above German sentence, which are in three different cases corresponding to three linguistic functions:
- *der Lehrer* 'the teacher' - nominative - subject
- *dem Schüler* '(to) the student' - dative - indirect object
- *die Regel* 'the rule' - accusative - direct object

Programming languages don't make the direct object vs. indirect object distinction, and they arguably also don't need to highlight the subject, which in most cases is just the programmer anyway. Thus, in the above `print` clause we see no subject, just as we don't need to express the subject in an English imperative clause (e.g., *Sit down!*).

That all being said, I think we should give those interested in programming vs. natural language comparison a chance rather than simply tell them it's futile. Whether or not a research project can yield useful results (a scientific issue) is a separate question from whether or not it should be banned to begin with (an ethical issue), not to mention that great ideas have often risen from unorthodox experiments in human history. Therefore, I'm not impressed by a user's suggestion to close the StackExchange–Linguistics question "[Any difference between natural and programming languages?](https://linguistics.stackexchange.com/questions/8612/any-difference-between-natural-and-programming-languages)" as off-topic based on the argument that "programming languages are outside the scope of linguistics." Who died and made us boss?

Back to the short paper I mentioned in the beginning of this post, its cognitive comparison of natural and programming languages draws insights from both knowledge representation and computation, and it takes into account both language comprehension and generation. Below I briefly explain what these terms mean in the domain of language (click each term for further information).

- [Knowledge representation](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=18&ved=2ahUKEwj8oej1tdrmAhXTy4sBHRgTAowQFjARegQICBAC&url=http%3A%2F%2Fwww-isl.ece.arizona.edu%2Fisl_presentations%2FScott3.ppt&usg=AOvVaw0Zxk1o_14NGUvvXSQJLaDa): the mental representation of words, phrases, and rules
- [Computation](https://en.wikipedia.org/wiki/Computation): the mental processes involved in language use
- [Comprehension](https://www.encyclopedia.com/education/encyclopedias-almanacs-transcripts-and-maps/language-comprehension): what happens in the mind when a person understands speech
- [Generation](https://www.ijcai.org/Proceedings/77-1/Papers/023D.pdf): what happens in the mind when a person produces speech

These all sound very scientific. And interestingly, all four terms have found their ways into AI, where researchers attempt to let computers emulate human intelligence. We are still far far away from humanlike AI ("nowhere near close" according to [Forbes](https://www.forbes.com/sites/forbestechcouncil/2018/08/28/how-far-are-we-from-truly-human-like-ai/#4ee5850331ac)), but the terminological loaning suggests that a language component will be [key to it](https://techcrunch.com/2016/03/12/artificial-intelligence-and-language/) whenever (or if) that eventually comes.

{% include figure image_path="/assets/images/zhizi.png" alt="An illustration of the Trisolarian robot Sophon" caption="The alien-made robot Sophon in *The Three-Body Problem* (see my [Aug 15 post]({{ site.baseurl }}{% post_url 2019-08-15-linguistics-in-three-body-part-1 %})) (illustration by ASK from [commons.moegirl.org](https://commons.moegirl.org/File:52520072_p0.png))" %}

## Beyond the programming vs. natural language comparison
The above-mentioned paper isn't the only place where programming and natural languages have been put in comparison, but it **is** one of the very few places where a positive tone has been conveyed. Most other discussions on the issue I've found online are more focused on the design differences between the two types of language. For example:
1. This Quora question: "[What's the difference between natural languages and programming languages?](https://www.quora.com/Whats-the-difference-between-natural-languages-and-programming-languages)" (I find [Daniel Ross' answer](https://www.quora.com/Whats-the-difference-between-natural-languages-and-programming-languages/answer/Daniel-Ross-71?ch=10&share=9efbe800&srid=ZQjU) especially informative.)
2. This blog post: "[Natural vs programming languages](http://meetrajesh.com/posts/natural-vs-programming-languages.html)" (This one is **for** a similarity-based perspective.)
3. This StackOverflow question: "[What's the difference between natural languages and programming languages in the context of their grammars?](https://stackoverflow.com/questions/45605231/whats-the-difference-between-natural-languages-and-programming-languages-in-the)" (There's only one response under this question but it's a neat one.)
4. This e-book chapter: "[Formal and Natural Languages](https://runestone.academy/runestone/books/published/thinkcspy/GeneralIntro/FormalandNaturalLanguages.html)" (This one is from a textbook, so the style is pretty scholarly.)
5. This Medium article: "[Human languages vs. Programming languages](https://medium.com/@anaharris/human-languages-vs-programming-languages-c89410f13252)" (This one is written by a linguist-turned-programmer and therefore both more comprehensive and more balanced.)

I support Fedorenko et al.'s (2019) proposal of a linguistically oriented path of programming language education and firmly stand with those who want to experiment new ideas (as long as they aren't against the law). But that doesn't mean I think such a new path would make CS education in school any more efficient than the "old-fashioned," mathematically oriented path. This is because **mastering a programming language isn't equal to mastering programming.** There's much more to the art of programming than just a bunch of function words and syntactic rules. According to many experienced programmers, what really makes programming difficult has never been the linguistic part but has always been the problem-solving (or "personality") part. For example, I'm sympathetic to the following answers under the Quora question "[What makes programming hard?](https://www.quora.com/What-makes-programming-hard)":

>[Steve Eng](https://qr.ae/TSkwJR): Programming is hard because ... solving problems from a programming perspective is a combination of art and talent.
>[Al Klein](https://qr.ae/TSkbJx): Learning a programming language without first learning programming is like learning “chain saw” without first learning carpentry - then complaining that cutting scroll work into a wood block is hard.
>[Jussi Hämäläinen](https://qr.ae/TSkgwE): Programming is hard simply because thinking is hard.
>[Baris Baser](https://qr.ae/TSkUcm): What makes playing chess hard? ...learning how to play chess can be considered relatively easy. Becoming a competent or great chess player, however, will not be easy.

See [this](https://www.codeconquest.com/programming-help/why-is-programming-so-hard/) and [this](https://makemeaprogrammer.com/is-programming-hard/) post for similar views, and see [this post](https://www.thinkful.com/blog/why-learning-to-code-is-so-damn-hard/) for a step-by-step guide on how to really master programming *after* crossing the linguistic threshold.

## Takeaway
- It is okay if you want to compare programming languages and natural languages, whether you are a linguist or a programmer. Fear not!
- While a linguistically oriented path of programming language education may be helpful in some way, it probably can't resolve the real obstacle in learning to program: the art of problem-solving.
- So, perhaps a joint (i.e., half-mathematical-half-linguistic) path would prove more efficient in the long run.
