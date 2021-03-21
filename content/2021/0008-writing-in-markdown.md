---
title: Writing in Markdown
author: Ed Vielmetti
date: 2021-03-21
---
One of the themes of this newsletter is tools that give you
superpowers. I'd like to convince you that the Markdown markup
language, wielded carefully, can be one of those super tools.
[Markdown] lets you edit text that looks good when you're writing it
as well as when you've published it, and by its relative simplicity
also empowers you to turn your text into data to published or
analyzed effectively.

[Markdown]:https://daringfireball.net/projects/markdown/

I'm writing this in Markdown, but you'll be reading it in beautifully
formatted web pages (if I have my way; there's some tooling involved). By
doing original authoring in a portable markup language I'm hoping to get
maximum flexibility in my choice of platforms, both for sending these
out [in newsletter format] as well as [a blog-style publication]. It's
a bet I'm comfortable making, and it should if all goes well prevent
the words I'm writing from being locked in to the platform that they're
being written on.

[in newsletter format]:https://groups.io/g/vacuum
[a blog-style publication]:https://vacuum-group.netlify.app

The Markdown ecosystem has some great tools in it for keeping
your words in order as well as making them pretty on screen
and on paper. Markdown was created in 2004 by [John Gruber]
and the late [Aaron Swartz], and has evolved but kept its essential
simplicity.

[John Gruber]:https://daringfireball.net/
[Aaron Swartz]:https://www.rollingstone.com/movies/movie-news/life-and-death-of-internet-pioneer-aaron-swartz-examined-in-new-doc-243958/

## Pandoc for document conversion

[pandoc] is a multi-purpose document conversion tool written in
[Haskell]. It is perhaps the best reason that a complete software
distribution for a new platform needs to have a good and working
Haskell. Pandoc takes files in a wide variety of word processing
formats and converts them with good fidelity into a wide variety of
other word processing formats. Practically speaking, this means that your
Markdown files have an easy path to PDF for print or to HTML for browser
viewing. All of this has a fast and happy path with just a few things
to learn, or a complete and very detailed use with nearly everything
customizable - depending on your needs.  Pandoc is free software,
released under the GPL. Copyright 2006–2020 [John MacFarlane].

[pandoc]:https://pandoc.org
[Haskell]:https://www.haskell.org/
[John MacFarlane]:https://www.johnmacfarlane.net/

## Markdownlint to check your work

[markdownlint] is a document checking tool (a "linter") that
operates on Markdown files. You use it to make sure that
your writing meets consistent styles, so that you can catch
formatting and style errors before they surprise you in print.
This linter can run standalone, or it can be integrated into
your favorite text editor or continuous integration tool.
I use the [markdownlint-cli2-action] Github action to check
files for sanity before publication. markdownlint is from [David Anson].

[markdownlint]:https://github.com/DavidAnson/markdownlint
[markdownlint-cli2-action]:https://github.com/DavidAnson/markdownlint-cli2-action
[David Anson]:https://dlaa.me/

## Hugo to publish it all to web pages

[Hugo] is a static site generator that in its common use
takes a set of Markdown files that have a little bit of
structure to them and turns them into a weblog or documentation
site. There's a lot more to be said about Hugo in the long
run, so I'll be brief here. Hugo has a powerful template
language so that you can make a site just so, or if you're
not a designer, you can use a pre-made theme to ease your
steps. The Hugo team is led by Bjørn Erik Pedersen ([bep]),
and the [tale] theme I'm using is from [Emiel Hollander].

[hugo]:https://gohugo.io
[bep]:https://bep.is/
[tale]:https://github.com/EmielH/tale-hugo
[Emiel Hollander]:https://github.com/EmielH

## Knowledge base or wiki powered by Markdown

If you have a directory full of Markdown files, there
are a variety of tools that will help you stitch them
together into a single navigable knowledge base. Similarly,
a small tweak to the Markdown syntax gives you a powerful
plain text wiki notation.

For a Markdown-powered wiki, I have been using the [Github wiki],
which is based on an earlier version of [Gollum]. The Github wiki is
remarkably weak, and just barely has the features you would expect,
but there is a hidden gem: you can download the whole thing via Git,
and sync and edit it with your favorite shell-based tools.

Gollum itself has matured a lot since I looked at it last,
turning into a wiki that can handle lots of different
flavors of markup language.

[Github wiki]:https://docs.github.com/en/github/building-a-strong-community/about-wikis
[Gollum]:https://github.com/gollum/gollum

If shell-based tools are not your thing and you would like
a nice GUI to navigate through, it's possible to take the
exact same text collection and drop it into one of the new
crowd of knowledge management tools that natively speak
Markdown. The one I tried was [Obsidian], which was nice
looking, and worked immediately out of the box on my
Github wiki word-hoard. I don't have enough time in front
of it to know that I'd want to use it day in and day out,
but ooh shiny, and I know some people like ooh shiny.

[Obsidian]:https://obsidian.md/

If for instance you've been living your life inside Evernote,
and are unhappy with that system's trajectory over time,
you might find this story by Anne Urai on
[From Evernote to Obsidian] to be of interest.
She writes about transforming 7 gigabytes of
notes (whew) into Markdown, and shows what they look like
in the new system.

[From Evernote to Obsidian]:https://anneurai.net/2021/03/16/note-taking-101-from-evernote-to-obsidian/

## Coding with Markdown libraries

A lot of programming languages have well-tested libraries
that help you write code based on data formated in Markdown.

In Go, use [Blackfriday] or [Goldmark]. Both are quite
capable, but differ some in internal design, and of course
programmers are expected to have strongly held opinions
about tools. One or the other might be better for you.
Hugo switched from Blackfriday to Goldmark in its 0.60 release.

[Blackfriday]:https://github.com/russross/blackfriday
[Goldmark]:https://github.com/yuin/goldmark/

If for whatever reason you are going to parse Markdown
with code of your own design, see [CommonMark].
This collaborative effort provides a strong specification
for the language and its extensions, as well as a
rigorous test suite to help you know that you're
doing it right.

A [list of CommonMark implementations] includes libraries in C, C#,
Crystal, D, Dart, Elixir, elisp, Go, Haskell, Haxe, Java, Scala,
Javascript, Julia, Lua, Perl, PHP, Python, Ruby, R, Rust, Swift, Tcl,
Typescript, and Zig. One of those might be right for you!

[CommonMark]:https://commonmark.org/
[list of CommonMark implementations]:https://github.com/commonmark/commonmark-spec/wiki/List-of-CommonMark-Implementations

## Markdown to book or ebook

[Casey Watts writes about self-publishing] with a full account
of taking a bunch of Markdown files and producing a Kindle
ebook with them. The steps are reasonably straightforward
and (mostly) automated, and he was satisfied with the results.
David Grophland's [From Markdown to Kindle] has much the
same journey.

[Casey Watts writes about self-publishing]:http://caseywatts.com/selfpublish
[From Markdown to Kindle]:https://medium.com/@davidgrophland/making-an-ebook-from-markdown-to-kindle-cf224326b1a2

If you want to self-publish and also get royalties from your
works, [Leanpub] is one option. It has the unusual feature
of supporting sales of not only finished works but drafts
in progress, letting you advertise your work and attract
readers before you're really done. The markup language
used is [Markua], which is an extension to Markdown with
some added features to support the sorts of things that
books need. Follow [Peter Armstrong] for more details.

[Leanpub]:https://leanpub.com/
[Markua]:https://leanpub.com/markua/read
[Peter Armstrong]:https://twitter.com/peterarmstrong

[R Markdown] is an extension to Markdown with the needs
of scientific publishing in mind - extensions that support
things like equations and graphs. [Bookdown] is a book
publishing system based on R Markdown, and there's a whole
book - [bookdown: Authoring Books and Technical Documents with R Markdown] -
which is a guide to that system.

[R Markdown]:https://rmarkdown.rstudio.com/
[Bookdown]:https://bookdown.org/
[bookdown: Authoring Books and Technical Documents with R Markdown]:https://bookdown.org/yihui/bookdown/

## For portable writing tools

The full discussion of Markdown actually goes a bit
longer than this, and might get into the weeds as far as
subtle differences between variants, how to make a page
look "just so" on paper, what the limits are and the like.
There are limits which are easy to overcome and some other
limits that require careful thought.

What's important is this: I can write text in my editor of choice, in a
style that's easy to understand, that will look nice when it finally gets
on your screen or page. This lets me write in a portable and reusable way
and not have my words trapped inside another system. That's an unfair
advantage over most closed proprietary systems and one worth
spending some effort on!
