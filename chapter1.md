# The Emergency Chapter

_Based on a true story._

Picture yourself: You have to submit a paper to this conference and the deadline is **tonight**. Yes, you had two months time, but for some reason creativity only kicked in last minute. You finally managed to write your thing but now it comes down to "please provide a camera ready version" / "please format in HUMBLEMUMBLE style". The clock is ticking[^2] [^4].

## Pest vs. Cholera

When you submit some academic stuff, you usually get a choice between Microsoft Word and LaTeX. You also get a link to download templates and example files to work with. What you see might look like this:![](/assets/Screen Shot 2017-04-13 at 14.23.14.png)

The choice here is obvious: they have given you **one** Word template versus **seven** strange files. You don't event want to know what these things are. It is also likely that you have written your masterpiece in Word already[^1]. So the sensible thing to do is to open the Word template and copy/paste your content over piece by piece, heading by heading, paragraph by paragraph. Sure there are pesky things like foootnotes, tables and images. And the citations and reference list have to be formatted in a certain HUMBLEMUMBLE style. Still easy enough, just keep calm and copy/paste. You start going... until something happens.

You have just copied some piece of text when you realize the whole paragraph now looks like the heading. You try to undo it and try again. Some text still looks strange. You look into the formats, but there are 35 of them, labelled "standard", "default text" and "paragraph". Which one? You delete the example image and copy your image in, but is too large and now it is half on the bottom of page 3 and half outside the page. Also some footnotes are suddenly gone. Attempts to fix this result in more chaos. Some text is behind the picture, and trying to delete the table that you don't need also removes some text on another page.

By now your paper looks like this[^3]:

![](/assets/Pablo_Picasso,_1911,_The_Poet_%28Le_poète%29,_Céret,_oil_on_linen,_131.2_×_89.5_cm,_The_Solomon_R._Guggenheim_Foundation,_Peggy_Guggenheim_Collection,_Venice.jpg)

At this point it seems like damage beyond repair. This is not your fault. Maybe you'll have a short glance to the other alternative. You google "LaTeX" and the results does not look promising. Everything you are giving a quick read is technical and confusing. It seems to have been written by a bunch of greybeards educating you about typesetting practices while celebrating themselves about enabling Umlauts like it's 1999. They assume that you want to spend months learning their noble craft and join an obscure typesetting guild in addition to being an overworked student. That won't work.

So you decide to start over with a fresh copy of the Word template. Two hours later the second one looks like the first. You are chasing your image through the text. Stuff appears and disappears at random. You also realize that you still have to change the appearence and order of the references one by one. And it's only five pages! Suddenly a shrill alarm sounds. Midnight!

**Game over**.

## How to do it

Let's turn back the clock for a few hours and try again. This assumes:

1. You are on a \(fairly recent\) Mac[^5]. You have 10 Gigabyte \(GB\) free space on your harddisk. You should be on a fast internet and you must have the password for your account.
2. You have to submit a formatted paper \(proposal\) and you are on a tight deadline.
3. You have written your paper already, probably in Word, Libre Office, Pages or another editor. 
4. Your work is not too complicated, mainly text, maybe a table, a few images, a handfull of references and stuff.   
5. You have got LaTeX templates / example files from the journal/conference like the ones pictured above.

We will go through a number of steps: first install LaTeX, then update it, prepare the document, copy the text, format images and tables, and finally do the citations and references. This should take about 2-3 hours if all goes well, about half of it will be installing software.

### Step 1: Install Software

Go to [http://www.tug.org/mactex/mactex-download.html](http://www.tug.org/mactex/mactex-download.html). Download the installer [**MacTeX.pkg**](http://tug.org/cgi-bin/mactex-download/MacTeX.pkg). Ignore everything that is written on the page[^6]. The download will take some time. Make tea. 

Run the installer. It walks you through the process. The installation will take some time as well. The program might try to scare you:

![](/assets/Screen Shot 2017-04-13 at 21.08.05.png)

 \(in practice more like 30 minutes\). During the installation it might ask you to install another piece of software named "XQuartz". Follow the instructions and install this as well. After the installation is finished you can delete the files you downloaded.

### Step 2: Update LaTeX

In your `Applications` you now have a folder named `TeX`. Start the `Tex Live Utility.app` there. It greets you with a window like this.

![](/assets/Screen Shot 2017-04-13 at 18.39.01.png)

Note that the list may be empty, say "No update available" or contain some entries. In any case click the little circular arrow

![](/assets/Screen Shot 2017-04-13 at 18.43.26.png)

.. and wait. There should be entries. The program might tell you it needs to update itself and ask for your password, etc. Confirm everything. Then in the Menu select `Actions -> Update all Packages`

Again, this will take some time to download and update everything. Time to re-read the paper maybe? If it fails, try again. Try closing Tex Live Utility and starting it again. Check if you are connected to the internet. If you have a hundred programs open on your Mac, you want to close them down, restart your Mac and focus. What you finally want to see is this:

![](/assets/Screen Shot 2017-04-13 at 18.44.25.png)

You can close it for now, get some sweets maybe and get ready.

### Step 3: Prepare the Document

I assume you have already a folder with the LaTeX templates / example files of your conference or journal[^7]. If not, do it now. First make a copy of the folder in case things go wrong. You also have your text somewhere, in Word for example.

Let's look at the LaTeX files.

![](/assets/Untitled.png)

Yours will have different names and some different symbols. There might be more or less of them. But you should have in any case two[^8]:

1. one file with the ending ".tex". This is **the LaTeX file** we are working with. Your paper will go in there. We will work on this first.
2. one file with the ending ".bib". This is the file for the **bibliography** entries. We will do that second.

Start TeXShop. Use the menu to open the the LaTeX file.

It looks similar to this:![](/assets/Screen Shot 2017-04-13 at 19.45.41.png)

[^1]: I am working with a number of assumptions here that might or might not be working for you. 

[^2]: Some conferences or journals have friendly editors that accept your late and half-formatted contribution by e-mail but some have automated systems that SHUT. DOWN. AT. MIDNIGHT.  

[^3]: [Ah, Picasso!](https://en.wikipedia.org/wiki/File:Pablo_Picasso,_1911,_The_Poet_%28Le_poète%29,_Céret,_oil_on_linen,_131.2_×_89.5_cm,_The_Solomon_R._Guggenheim_Foundation,_Peggy_Guggenheim_Collection,_Venice.jpg "Ah, Picasso!")

[^4]: If you are really in a hurry you might skip the next section and head to "How to do it".

[^5]: That's for now. Ping me if you want this written for other choices. 

[^6]: I am aware that this is a dubious instruction but we are on a deadline \(you still have time to read the footnotes here?\) 

[^7]: "What if not?" you might ask. "Then we are in trouble", I answer. Time to contact the chair of your conference and ask for the LaTeX templates.

[^8]: Some people have set up their Finder that they can't see the endings. To fix that, go to `Finder -> Preferences -> Advanced` and change the setting \(forever\).

