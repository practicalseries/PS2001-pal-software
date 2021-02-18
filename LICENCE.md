<p align="right">LICENCE.md</p>

# The Licence

The software and all its associated documentation is made available under the MIT licence given in full below:

---

__MIT Licence__

© 2020 Michael Gledhill

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

---
<br />
<br />

# Why did I choose the MIT Licence?

Well, it turns out I’m not an expert on software licences. 

I’m used to the sort of software licences that Siemens and Microsoft produce; the ones that say “pay me and you can use my stuff”, they also tend to say “but don’t for a minute think you can copy it and give it to someone else”.

Now, I’m letting you and everyone else use my software and I’m letting you do it for *nowt*. I don’t expect you to pay for the privilege. But I also don’t want to be sued when you screw things up and the plant burns down *(think [Buncefield](https://en.wikipedia.org/wiki/Buncefield_fire))*.

There are software licences that cover this sort of thing, they are generally called *open source* licences and there is an awful lot of them, you can see a list of them [here](https://en.wikipedia.org/wiki/Comparison_of_free_and_open-source_software_licenses).

I ignored most of these licences (after a bit of research), some are just variations of others with silly terms added *“The Software shall be used for Good, not Evil.”* JSON I’m looking at you here (how do you enforce this, who decides what’s Good &mdash; presumably at some point Germany thought it was a *good thing* to invade Poland). Others are not very widely used and consequently have not been tested in court. There seem to be five main ones:

* MIT licence (Massachusetts Institute of Technology)
* Apache (Apache Software Foundation)
* GPL (GNU general public licence)
* LGPL (GNU lesser general public licence)
* BSD licence (Berkley Software Distribution)

> *GNU stands for “Gnu’s Not Unix!” (this sort of stuff just gets on my nerves, it’s the UNIX, LINUX holier-than-thou mob &mdash; I’ll leave you to decide if they’ve missed an apostrophe) Gnu is the word Gnu &mdash; you know the antelope thing with big horns. It is the name of a free operating system called (yes, you guessed it): GNU.*

All of these licences are very commonly used.

These licences broadly fall into two categories, “permissive” licences and “copyleft” licences.

MIT, Apache and BSD licences are all of the permissive variety; GPL and LGPL are of the copyleft variety.

*So what does this all mean?* Well let’s have a look:

<br />

## Permissive licences

Permissive licences are what most people think of when they think about open source software. These licences are easy to comply with; essentially, a person or organisation simply has to reproduce the licence and copyright notice whenever they use the code. If they’ve done this, they may do as they wish with the code, including selling it.

<br />

## Copyleft licence

*Copyleft* (as opposed to copyright), this is a made up word; these licences are sometimes called reciprocal licences. Broadly these licences provide an arrangement where software may be used, modified and distributed freely (just like permissive licences); but only on the condition that anything that uses the software or is derived from it is bound by the same conditions (unlike permissive licences).

The GPL licence is a copyleft licence and it has a whiff of fanaticism about it, it is written and maintained by the [Free Software Foundation](https://www.fsf.org/) (FSF), this in turn was started by [Richard Stallman](https://en.wikipedia.org/wiki/Richard_Stallman) *(er… how to say this politely? A man who can be described as “interesting”)*, this is a foundation that thinks open source software doesn’t go far enough &mdash; I think basically that they are saying all software should be free and no one should make a profit from it (along the lines of *“all property is theft”*).

This is a bit of a problem for me, let me give you an example, let say I produce my software called: “U-Can’t-Bend-It” and license it under the GPL licence. Now let’s say you come along and think U-Can’t-Bend-It is just the thing you need for your software; you take it modify it slightly and you now have your own version: “I-Can’t-Bend-It”. The problem here is that you can’t sell your new product; GPL requires that your software (based on my software) must be licensed under exactly the same licence as the original, i.e. distributed freely.

It’s even worse, if you already have an existing software project (it could be absolutely massive) and you use any of my “U-Can’t-Bend-It” software (perhaps to provide a particular interface), then, under the terms of the GPL licence, your whole programme is considered a derivative work and it must be released under the same GPL licence.
The LGPL (lesser GPL) has been introduce to address this particular problem (although bizarrely, the FSF website seems to discourage its use, see [here](https://www.gnu.org/licenses/why-not-lgpl.en.html)); the LPGL allows the use of library software in proprietary programmes (programmes for which you can charge).

<br />

## Limiting liabilities

The other thing for me to consider, is the question of liability. I do not want to be liable for any problem you may encounter when using this software.
Open source software licences (I’m including the GPL licences in this broad definition &mdash; it will probably annoy them) generally limit the liability of those providing the software to zero; this is exactly the same amount that those providing the software get paid &mdash; NOTHING.

Both the permissive licences and the copyleft licences have terms within them that limit any liability of the provider, terms like this:

>THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

All the above licences provide this type of protection against liability.

<br />

# Which licence to use?

Ok, let’s start with the ones I’m not going to use and why.

I’m not going to use the copyleft (GPL and LGPL) licences. This is because they don’t let you (as in people who download the software) make money from the software provided.

I firmly believe that engineers should be paid for the work they do.

I also just don’t like the FSF; there is a fanatical zeal there that I can’t come to terms with *(bit like Jeremy Corbyn supporters and Linux people &mdash; they seem to me, to be entirely convinced of their own moral superiority and completely dismissive of any other argument. They have a stifling certitude; an implacable self-righteousness and they are always willing to be offended)*.

So I’m not using GPL or LGPL &mdash; sorry Mr Stallman.

That leaves the permissive licences: MIT, Apache and BSD. 

I’m not going to use the BSD licence; this is mainly because it is very similar to the MIT licence, but is not as widely used.

The Apache licence is a more complicated version of the MIT licence, I didn’t understand it. It is not that widely used outside the Apache Software Foundation and I’m not using it.

So now it’s just the MIT licence and that is the one I’m using. You can see it in full at the start of this file.

Basically, you can do what you like with the code, if, and only if, you reproduce the MIT licence somewhere within your application and give credit to me (the copyright bit) as the author.

Oh, yes, the final point: __don’t sue me if it all goes tits up__.

<br />

## A note on spelling: licence or license

Licence or license? I’m English so I think licen**ce** is a noun and licen**se** is a verb: James Bond is licen**se**d to kill, so he has a killing licen**ce**. Americans, use license as both the noun and the verb *(of course they do)*. 

Generally, I use the proper English spelling throughout the documentation in this project; I differ only when I’m using a literal explanation of something on a screen, or something being installed &c. and it’s important to clearly show exactly what the user will see.
