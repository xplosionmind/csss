# Computer Sciences Are Social Sciences!

[This repository](https://codeberg.org/tommi/csss 'csss repository on Codeberg') hosts [Tommi](https://tommi.space/home#about 'About Tommi')’s [bachelor’s thesis](https://tommi.space/csss.pdf), written between February and June 2023.

Note: unfortunately, I was not considerate enough to keep track of my work through git progressively. This repository has been created later, in April 2024. Hence, the commits up to that date *do not* reflect the actual moment when the content was created. Hopefully, I will be able to create commits step by step in the future.

## What’s inside

- 👾 [Markdown](Computer%20Sciences%20Are%20Social%20Sciences.md) and [LaTeX](Computer%20Sciences%20Are%20Social%20Sciences.tex) source files
- 📚 [Bibliography](Computer%20Sciences%20Are%20Social%20Sciences.bib)
- 📊 [Figures](figures/)
- 📽️ [Presentations](/presentations/) often linked to [*Sewing Our Internet*](https://tommi.space/sewnet 'Sewing Our Internet, tommi.space')
- 🏷️ [YAML metadata](Computer%20Sciences%20Are%20Social%20Sciences.yml) for [Pandoc parsing](#build-process)
- 🖋️ [Tim Berners-Lee’s autograph](TBL%20autograph/) of the front page (yes, I know! 😍)

## Workshop: *Sewing Our Internet*

Since I feel very strongly about the topics of this thesis, I have been thinking hard of ways to inform and involve people.
Out of this effort, a workshop came out, and I had the honour and pleasure to host it in many occasions with diverse crowds of various ages.

The workshop is called [***Sewing Our Internet***](https://tommi.space/sewnet 'Sewing our Internet, tommi.space').

## License

All of the original content inside this repository (therefore excluding the figures and the quotes) is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).

## Feedback and corrections

I am keen to discuss about anything related to this thesis! Get in touch if you’d like!

I wrote my thesis as a young undergraduate student. Even if it is highly unlikely, there might be information that is partly or even fully incorrect. I apologise for this, and I invite you to contact me if you spot any kind of mistake!

### Obsolescence

The text of the thesis **is not being updated**. Please, be aware that there might be information that becomes incorrect or wrong because of obsolescence.

## Build process

I am technically goofy (actually, not only technically) to say the least, and the build process for this thesis is fragmented and messy. I know the right way to parse the final PDF including citations, markup, frontispiece, etc. would be to use a Makefile. I tried. I failed miserably. Therefore, below are the admittedly weird but effective build steps to get to the final thesis in PDF format.

1. Markdown → HTML conversion, using Pandoc: <pre><code>pandoc -s 'Computer Sciences Are Social Sciences.md' --wrap=none --resource-path="$PWD" --metadata-file='Computer Sciences Are Social Sciences.yml' -C -o 'Computer Sciences Are Social Sciences.html'</code></pre>
2. HTML → LaTeX conversion, using Pandoc: <pre><code>pandoc -s 'Computer Sciences Are Social Sciences.html' --wrap=none --resource-path="$PWD" --metadata-file='Computer Sciences Are Social Sciences.yml' -C -o 'Computer Sciences Are Social Sciences.tex'</code></pre>
3. Build the final `.tex` file using `pdflatex`: <pre><code>pdflatex 'Computer Sciences Are Social Sciences.tex'</code></pre>

Please, refer to [my technical notes](https://tommi.space/pandoc-workflow/ 'Academic writing with Pandoc – tommi.space') to try to understand more (good luck with that).

## Table of contents

1. [Introduction](Computer%20Sciences%20Are%20Social%20Sciences.md#introduction)
1. [An Historical Account](Computer%20Sciences%20Are%20Social%20Sciences.md#an-historical-account)
	1. [Paul Baran’s <q>centrifugal</q> network](Computer%20Sciences%20Are%20Social%20Sciences.md#paul-barans-centrifugal-network)
	2. [Licklider and ARPA](Computer%20Sciences%20Are%20Social%20Sciences.md#licklider-and-arpa)
	3. [The Web](Computer%20Sciences%20Are%20Social%20Sciences.md#the-web)
	4. [The Internet’s original sin](Computer%20Sciences%20Are%20Social%20Sciences.md#the-internets-original-sin)
2. [The spread of Surveillance Capitalism](Computer%20Sciences%20Are%20Social%20Sciences.md#the-spread-of-surveillance-capitalism)
	1. [<q>The Unprecedented</q>](Computer%20Sciences%20Are%20Social%20Sciences.md#the-unprecedented)
	2. [Economy and technology: an inseparable duo](Computer%20Sciences%20Are%20Social%20Sciences.md#economy-and-technology-an-inseparable-duo)
	3. [The essence of technology](Computer%20Sciences%20Are%20Social%20Sciences.md#the-essence-of-technology)
3. [Case study: Hong Kong’s Umbrella Movement](Computer%20Sciences%20Are%20Social%20Sciences.md#case-study-hong-kongs-umbrella-movement)
	1. [The political context: Hong Kong’s strive for democracy](Computer%20Sciences%20Are%20Social%20Sciences.md#the-political-context-hong-kongs-strive-for-democracy)
	2. [Puppeting emotions: social media as a political actor](Computer%20Sciences%20Are%20Social%20Sciences.md#puppeting-emotions-social-media-as-a-political-actor)
	3. [Becoming water: protests’ decentralization and repression](Computer%20Sciences%20Are%20Social%20Sciences.md#becoming-water-protests-decentralization-and-repression)
	4. [An interpretation in terms Hannah Arendt’s philosophy](Computer%20Sciences%20Are%20Social%20Sciences.md#an-interpretation-in-terms-hannah-arendts-philosophy)
4. [Where the current Internet fails](Computer%20Sciences%20Are%20Social%20Sciences.md#where-the-current-internet-fails)
	1. [Algorithms as <q>Black-Boxes</q>](Computer%20Sciences%20Are%20Social%20Sciences.md#algorithms-as-black-boxes)
	2. [Proprietary software](Computer%20Sciences%20Are%20Social%20Sciences.md#proprietary-software)
	3. [Surveillance Capitalism, once again](Computer%20Sciences%20Are%20Social%20Sciences.md#surveillance-capitalism-once-again)
	4. [The case of <cite>Truth Social</cite>](Computer%20Sciences%20Are%20Social%20Sciences.md#the-case-of-truth-social)
	5. [Turning the origins upside down](Computer%20Sciences%20Are%20Social%20Sciences.md#turning-the-origins-upside-down)
5. [A better Internet](Computer%20Sciences%20Are%20Social%20Sciences.md#a-better-internet)
	1. [The method: Philosophy *in* Science](Computer%20Sciences%20Are%20Social%20Sciences.md#the-method-philosophy-in-science)
	2. [Using technology to pursue utopias](Computer%20Sciences%20Are%20Social%20Sciences.md#using-technology-to-pursue-utopias)
	3. [Adversarial Interoperability](Computer%20Sciences%20Are%20Social%20Sciences.md#adversarial-interoperability)
	4. [Algorithmic Sovereignty](Computer%20Sciences%20Are%20Social%20Sciences.md#algorithmic-sovereignty)
	5. [Decentralized social media: the Fediverse](Computer%20Sciences%20Are%20Social%20Sciences.md#decentralized-social-media-the-fediverse)
6. [Conclusion](Computer%20Sciences%20Are%20Social%20Sciences.md#conclusion)
7. [Thank you](Computer%20Sciences%20Are%20Social%20Sciences.md#thank-you)
8. [References](Computer%20Sciences%20Are%20Social%20Sciences.md#references)
