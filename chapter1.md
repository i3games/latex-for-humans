# The Emergency Chapter

_Based on a true story._

Picture yourself: You have to submit a paper to this conference and the deadline is **tonight**. Yes, you had two months time, but for some reason creativity only kicked in last minute. You finally managed to write your thing but now it comes down to "please provide a camera ready version" / "please format in HUMBLEMUMBLE style". The clock is ticking[^2] [^4].

## Pest vs. Cholera

When you submit some academic stuff, you usually get a choice between Microsoft Word and LaTeX. You also get a link to download templates and example files to work with. What you see might look like this:![](/assets/Screen Shot 2017-04-13 at 14.23.14.png)

The choice here is obvious: they have given you **one** Word template versus **seven** strange files. You don't event want to know what these things are. It is also likely that you have written your masterpiece in Word already[^1]. So the sensible thing to do is to open the Word template and copy/paste your content over piece by piece, heading by heading, paragraph by paragraph. Sure there are pesky things like foootnotes, tables and images. And the citations and reference list have to be formatted in a certain HUMBLEMUMBLE style. Still easy enough, just keep calm and copy/paste. You start going... until something happens.

You have just copied some piece of text when you realize the whole paragraph now looks like the heading. You try to undo it and try again. Some text still looks strange. You look into the formats, but there are 35 of them, labelled "standard", "default text" and "paragraph". Which one? You delete the example image and copy your image in, but is too large and now it is half on the bottom of page 3 and half outside the page. Also some footnotes are suddenly gone. Attempts to fix this result in more chaos. Some text is behind the picture, and trying to delete the table that you don't need also removes some text on another page.

By now your paper looks like this[^3]:

![](/assets/Pablo_Picasso,_1911,_The_Poet_%28Le_poète%29,_Céret,_oil_on_linen,_131.2_×_89.5_cm,_The_Solomon_R._Guggenheim_Foundation,_Peggy_Guggenheim_Collection,_Venice.jpg)

At this point it seems like damage beyond repair. Maybe a short glance to the other alternative. You google "LaTeX" and the results does not look promising. Everything you are giving a quick read is technical and confusing. It seems to have been written by a bunch of greybeards educating you about obscure typesetting practices while celebrating themselves about enabling Umlauts like it's 1999. They assume that you want to spend months learning this noble craft and join their typesetting guild in addition to being an overworked student. That won't work.

So you decide to start over with a fresh copy of the Word template. Two hours later the second one looks like the first. You are chasing your image through the text. Stuff appears and disappears at random. You also realize that you still have to change the appearence and order of the references one by one. And it's only five pages! Suddenly a shrill alarm sounds. Midnight!

**Game over**.

## How to do it

Let's turn back the clock for a few hours and try again. This assumes:

1. You are on a \(fairly recent\) Mac[^5]. You need to be on the internet and you must have the password for your account.
2. You have to submit a formatted paper \(proposal\) and you are on a deadline.
3. You have written your paper, probably in Word, Libre Office, Pages or another editor. 
4. Your paper is not too complicated, mainly text, maybe a table, a few images, references and stuff.   
5. You have got LaTeX templates / example files from the journal/conference like the ones pictured above.

We will go through a number of steps: first install software, set up LaTeX, then prepare the document, copy the text, format images and tables, and finally do the citations and references. This should take about 2 hours if all goes well.

### Step 1: Install Software

Go to [http://www.tug.org/mactex/morepackages.html. ](http://www.tug.org/mactex/morepackages.html)The page is labelled "\*\* Smaller Download \*\*". Download the installer  [**BasicTeX.pkg**](http://tug.org/cgi-bin/mactex-download/BasicTeX.pkg) and run it. Ignore everything that is written on the page[^6].

Scroll down and klick the link that says [**TeXShop**](http://pages.uoregon.edu/koch/texshop/obtaining.html). This will take you to another page. If your Mac is quite new, download the file [Latest TeXShop Version 3](http://pages.uoregon.edu/koch/texshop/texshop-64/texshop.zip) there. \(If you are in doubt, klick the Apple symbol in top left corner on your Menu, then `About this Mac`. It will tell you the version of your Mac. Download the appropriate version of TeXShop.\) Unpack the zip file and drag the App into your Applications folder.

Back on the original page klick the link that says [**TeX Live Utility**](http://amaxwell.github.io/tlutility/). This will take you to yet another page. "Latest release" brings you to another page. There you see something named similar to this: [**TeX.Live.Utility.app-1.26.tar.gz**](https://github.com/amaxwell/tlutility/releases/download/1.26/TeX.Live.Utility.app-1.26.tar.gz) Download and unpack. Inside is ... an App! Drag this App into your Applications folder as well.

### Step 2: Set Up LaTeX

Start the Tex Live Utility. It greets you with a window like this.

![](/assets/Screen Shot 2017-04-13 at 18.39.01.png)

Note that the list may be empty, say "No update available" or contain some entries. In any case click the little circular arrow

![](/assets/Screen Shot 2017-04-13 at 18.43.26.png)

.. and wait. There should be entries. The program might tell you it needs to update itself etc. Confirm everything. Then in the Menu select `Actions -> Update all Packages`

It might take some time time to download and ask you things in between. If it fails, try again. Close down Tex Live Utility and start it again. Check if you are connected to the internet. If you have a hundred programs open on your Mac, you want to close them down, restart your Mac and focus. What you finally want to see is this:

![](/assets/Screen Shot 2017-04-13 at 18.44.25.png)

You can close it for now and get some tea.

### Step 3: Prepare the Document

You have already downloaded a folder with the LaTeX templates / example files of your conference or journal[^7]. First make a copy of the folder in case things go wrong. You also have your text somewhere, in Word for example.

Let's look at the LaTeX files.

![](/assets/Untitled.png)

Yours will have different names and some different symbols. There might be more or less of them. But you should have in any case[^8]:

1. one file with the ending ".tex". This is **the LaTeX file** we are working with. Your paper will go in there. We will work on this first.
2. one file with the ending ".bib". This is the file for the **bibliography** entries. We will do that later.

Start TeXShop. Use the menu to open the the LaTeX file.

It looks like this.

[^1]: I am working with a number of assumptions here that might or might not be working for you. 

[^2]: Some conferences or journals have friendly editors that accept your late and half-formatted contribution by e-mail but some have automated systems that SHUT. DOWN. AT. MIDNIGHT.  

[^3]: [Ah, Picasso!](https://en.wikipedia.org/wiki/File:Pablo_Picasso,_1911,_The_Poet_%28Le_poète%29,_Céret,_oil_on_linen,_131.2_×_89.5_cm,_The_Solomon_R._Guggenheim_Foundation,_Peggy_Guggenheim_Collection,_Venice.jpg "Ah, Picasso!")

[^4]: If you are really in a hurry you might skip the next section and head to "How to do it".

[^5]: That's for now. Ping me if you want this written for other choices. 

[^6]: I am aware that this is a dubious instruction but we are on a deadline \(you still have time to read the footnotes here?\) 

[^7]: "What if not?" you might ask. "Then we are in trouble", I answer. Time to contact the chair of your conference and ask for the LaTeX templates.

[^8]: Some people have set up their Finder that they can't see the endings. To fix that, go to `Finder -> Preferences -> Advanced` and change the setting \(forever\).

