---
layout: post
title: Why Book Reviews Suck And How We Can Fix Them
author: David
date: "2012-08-31T06:30:18-04:00"
tags:
  - NLP
  - book reviews
  - technology
  - thoughts
  - news
tumblr_url: http://tumblr.davidlday.com/post/30579650629/why-book-reviews-suck-and-how-we-can-fix-them
---

**Disclaimer**: This post comes from me as a technologist and a reader, not as a
writer. As a writer, I keep my opinions on reviews and reviewers to myself.

All the
[recent](http://www.nytimes.com/2012/08/26/business/book-reviewers-for-hire-meet-a-demand-for-online-raves.html)
[exposure](http://www.theatlantic.com/technology/archive/2012/08/will-paid-reviews-bite-amazon-back/261582/)
on GettingBookReviews.com and
[John Locke’s](http://janefriedman.com/2012/08/28/extra-ether-buying-book-reviews-still-admire-john-locke/)
lack of disclosure on using the service prompted me to finally put up a post on
something I’ve been thinking about for a while.

Paying someone to review your book is like asking your mom what she thought of
the card you made her for Mother’s Day in the third grade. Wait. No. It’s more
like going to The Moonlight Bunny Ranch, getting the all-you-can-@#$% special,
and asking each of your escorts if you’re well endowed.

Don’t expect any honesty.

It’s clear we the readers have a problem. You see, people are also doing this
without money changing hands. With the overwhelming number of people getting
into self publishing, each trying to clamour for attention and sales, we’re also
seeing a rise in highly-biased reviews from a variety of sources. The bottom
line is you just can’t trust reviews the way originally intended. Now I’m not
saying all self-published authors engage in this behavior, or that this behavior
is isolated to only self-publishing, but the review landscape is tainted such
that it’s often difficult to distinguish honesty from marketing.

Even Amazon’s own recommendations are questionable. Check out what this 2010
post from
[The Boston Review](http://www.bostonreview.net/BR35.6/roychoudhuri.php) had to
say (emphasis mine):

> Jeffrey Lependorf, Executive Director of the Council of Literary Magazines and
> Presses and of Small Press Distribution, suggests that the difference between
> Amazon and brick-and-mortar bookstores is most evident in how they market
> books: “I think even people at Amazon would say that it’s essentially a widget
> seller that happens to have begun by focusing on books. Many people, like me,
> will say you can’t sell a book the same way you sell a can of soup.”

> At the heart of the soup-can analogy are the algorithms that Amazon uses to
> “recommend” books to customers. Most customers aren’t aware that the
> **personalized book recommendations they receive are a result of paid
> promotions, not just purchase-derived data.** This is frustrating for
> publishers who want their books to be judged on their merits. “I think their
> twisted algorithms that point you toward bestsellers instead of books that you
> might actually like [are] a shame,” Gavin Grant, cofounder of Small Beer
> Press, laments.

As a reader, reviews don’t do shit for helping me find a book to read.
Personally, I tend to ignore consumer book reviews (and some professional
reviews as well) when looking for something to read. I have a few trusted
sources, but I also rely heavily on scanning the first few pages—or sometimes a
random spot in the middle—to get a sense of whether the book is right for me at
the time.

Even that takes a lot of time, and I sometimes make bad picks. What I want is a
more reliable way of knowing a book’s quality relative to other books I’ve read
and enjoyed.

If only there were a way to measure a text’s relevance and quality. Some sort of
classifier, let’s say, that weeds out undesirable text and narrows my choices
down for me. After all,
[making a decision in the face of too many choices](http://en.wikipedia.org/wiki/The_Paradox_of_Choice:_Why_More_Is_Less)
is overwhelming. And in today’s book market we have a lot of choices.

We’re at a unique point in history. More text today is being published in
electronic format than ever before. We shouldn’t have to rely solely on other
people’s opinions (although we shouldn’t ignore them wholesale either) when it
comes to finding a good book.

Right now, there’s a little magic at work for you helping you decide which
emails are worth reading and which are probably junk. It’s a
[spam filter](http://en.wikipedia.org/wiki/Bayesian_spam_filtering), and nearly
every hosted email service and every email client has on.

With so many books in electronic format, why on earth aren’t we using a similar
approach for classifying? I won’t get into technical details (cause this ain’t a
technical post), but trust me when I say this is not only possible, but is also
now practical. With so many modern works available as e-books, implementing a
preference filter is well within reach. In fact, I wouldn’t be surprised if
Google Books was headed this way. After all, what’s Google doing with all those
scanned books? Textual analysis.

There’s a post up at the
[Wall Street Journal](http://online.wsj.com/article/SB10000872396390444375104577591304277229534.html)
that speaks to the use of algorithms to sort and classify creative works. It
briefly touches on applying algorithms to text but focuses more on using those
algorithms to generate writing and only mentions using algorithms to grade text.
I think it misses a huge potential for Natural Language Processing (NLP).

Using algorithms such as Naive Bayes (typical SPAM filter), we can let a
consumer categorize books they’ve read and use NLP to classify unread books
based on those categories. For instance, say I enjoy reading Science Fiction,
Horror, and Romance. I could create a list for each genre, and my bookseller
(say, Amazon) could then let me search their collection for books that fit into
my personalized categories.

The WSJ article also mentions the use of NLP for grading papers, and claims the
current systems can grade as well as any human. So we also have tools at hand to
help us find not only books that fit into our categories, but books that are
written well. This ranges from simple grammar and spell checking (which
self-publishers may either fail to do or do poorly) to
[Readability formulas](http://en.wikipedia.org/wiki/Readability#The_popular_readability_formulas).

Here’s where you say, “What? Books are an art form! There’s no way a computer
could understand art well enough to distinguish the good from the bad.”

Yeah, okay. True, a computer may never fully understand the nuances of an art
form, but all art is based on fundamental rules. Music, movies, books,
painting—all have basic elements the artist uses in composition, and those basic
elements can be quantified.

And you know what? We already use algorithms to help pick music (Pandora, Ping)
and movies (Netflix, Clicker). And as mentioned above, Amazon uses algorithms
(although allegedly inappropriately) to recommend books.

I could drag on for hours about this, in part because it blends two things I’m
passionate about (books and technology).

I’m thinking about using Kickstarter to fund a book recommendation service based
on a combination of NLP algorithms, with initial focus on genre fiction. The
service wouldn’t take the place of human reviews, but could provide a sort of
litmus test by which reviews could be tempered. Setting this up would take a lot
of work, and there’s no way I could do this on my own. So before I go any
farther, I’d like to ask a few questions to help me gauge if this is worth my
time:

1. As a reader, would you use a service for book recommendations (likely for
   free) knowing the service used only algorithms?

2. As a gatekeeper (agent / editor / publisher), would you be interested in a
   service to classify your slush pile, comparing submissions to works you’ve
   previously published (or works you select) and scoring them for grammar,
   spelling, and readability? Would you be willing to pay a small fee?

3. As a writer, would you be interested in an automated service to help you
   locate potential markets for your work? Would you be willing to pay a small
   fee?

Have at it. Don’t feel the need to answer the questions. General comments are
more than welcome, too.
