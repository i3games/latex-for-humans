# The Emergency Chapter

_Based on a true story._

Picture yourself like this: You have to submit a paper / paper draft to this fancy conference \(or prestigous journal\) and the deadline is **tonight**. Yes, you had two months time, but for some reason creativity only kicked in last minute. You finally managed to write your thing but now it comes down to "please provide a camera ready version" / "please format in HUMBLEMUMBLE style". The clock is ticking[^1] [^2].

## Pest vs. Cholera

When you submit academic stuff, you usually get a choice between Microsoft Word and LaTeX. You also get a link to download templates and example files to work with. What you see might look like this:

![](/assets/Screen Shot 2017-04-13 at 14.23.14.png)

The choice is obvious: they have given you **one** Word template versus **seven** strange files. You don't even want to know what these bib, bbl, blg, bst... things are. It is also likely that you have written your masterpiece in Word already[^3]. So the sensible thing to do is to open the Word template and copy/paste your content over piece by piece, heading by heading, paragraph by paragraph. Actually this is what you are supposed to do according to the authors of these files[^4]. Sure there are pesky things like foootnotes, tables and images. And the citations and reference list have to be formatted in a certain HUMBLEMUMBLE style. Still easy enough, just keep calm and copy/paste. You start going... until something weird happens.

You have just copied some piece of text when you realize the whole paragraph now looks like the heading. You try to undo it and try again. Some text still looks strange. You look into the formats, but there are 35 of them, labelled "standard", "default text" and "paragraph". Which one? You delete the example image and copy your image in, but is too large and now it is half on the bottom of page 3 and half outside the page. Also some footnotes are suddenly gone. Attempts to fix this result in more chaos. Some text is behind the picture, and trying to delete the table that you don't need also removes some text on another page.

By now your paper looks like this[^5]:

![](/assets/Pablo_Picasso,_1911,_The_Poet_%28Le_poète%29,_Céret,_oil_on_linen,_131.2_×_89.5_cm,_The_Solomon_R._Guggenheim_Foundation,_Peggy_Guggenheim_Collection,_Venice.jpg)

This is not your fault. There is no time for guilt or blame. But by now you are already going through the [five stages of grief](https://en.wikipedia.org/wiki/Kübler-Ross_model): denial, anger, bargaining, depression, acceptance. Probably during the bargaining phase you were tempted to look at the other alternative. You googled "LaTeX" and the results did not look promising. Everything you were giving a quick read was technical and confusing. That stuff seems to have been written by a bunch of greybeards educating people about typesetting practices while celebrating themselves for enabling Umlauts like it's 1999. They assume that you want to spend months learning their noble craft and join an obscure guild in addition to being an overworked student. This won't work.

So you decide to start over with a fresh copy of the Word template. Two hours later the second one looks like the first. You are chasing your single image through the text. Stuff appears and disappears at random. You also realize that you still have to change the appearence and order of the references one by one. And it's only five pages! Suddenly a shrill alarm sounds. Midnight!

**GAME OVER**

## How to do it

Let's rewind the clock for a few hours and try again. This assumes:

1. You are on a \(fairly recent\) Mac[^6]. You have 10 Gigabyte \(GB\) of free space on your harddisk. You should be on a fast internet and you must have the password for your account.
2. You have to submit a formatted paper \(draft, proposal\) and you are on a tight deadline.
3. You have written your paper already, probably in Word, Libre Office, Pages or another editor. 
4. Your work is not too complicated, mainly text, maybe a table, a few images, a handfull of references and stuff.   
5. You have received LaTeX templates / example files from the journal/conference like the ones pictured above. This means you may submit a pdf set in LaTeX.

We will go through a number of steps: first install LaTeX, then update it, check the template, prepare the document, copy the text, format images and tables, and finally do the citations and references. This should take roghly 3 hours if all goes well. The first half of it will be installing and updating LaTeX.

### Step 1: Install LaTeX

Go to [http://www.tug.org/mactex/mactex-download.html](http://www.tug.org/mactex/mactex-download.html). Download the installer [**MacTeX.pkg**](http://tug.org/cgi-bin/mactex-download/MacTeX.pkg). Ignore everything that is written on the page[^7]. The download will take some time. Make tea.

Run the installer. It walks you through the process. The installation will take some time as well. The program might try to scare you:

![](/assets/Screen Shot 2017-04-13 at 21.08.05.png)

\(in practice it is more like 30 minutes\). During the installation it might ask you to install another piece of software named "XQuartz". Follow the instructions and install this as well. After the installation is finished you can delete the files you have downloaded.

### Step 2: Update LaTeX

In your `Applications` you now have a folder named `TeX`. Start the `Tex Live Utility.app` there. It greets you with a window like this:

![](/assets/Screen Shot 2017-04-13 at 18.39.01.png)

First check under Preferences if `Tex Live Utility`  itself wants to be updated. If so, follow the instructions.

Note that the list may be empty, says "No update available" or contains some entries. In any case, click the little circular arrow

![](/assets/Screen Shot 2017-04-13 at 18.43.26.png)

.. and wait. Then there should be entries. The program might tell you it needs to update itself and ask for your password, etc. Confirm everything. Then in the Menu select `Actions -> Update all Packages`.

It can take a significant amount of time to download and update everything. Time to re-read the paper maybe? If the update fails, try again. Try closing Tex Live Utility and starting it again. Check if you are connected to the internet. If you have a hundred programs open on your Mac, you want to close them down, restart your Mac and focus. What you finally want to see is this:

![](/assets/Screen Shot 2017-04-13 at 18.44.25.png)

You can close `Tex Live Utility` for now, consume some sweets maybe and get ready.

### Step 3: Check the Template

I assume you have already a folder with the LaTeX templates / example files from your conference or journal[^8]. If not, get it now. Make a copy of the folder in case things go wrong. You also have your text somewhere, in Word for example.

Let's look at the LaTeX files.

![](/assets/Untitled.png)

Yours will have different names and some different symbols. There might be more or less of them. But you should have in any case[^9]:

1. a file with the ending ".tex". This is **the LaTeX file** we are working with. Your paper will go in there. We will work on this first.
2. a file with the ending ".bib". This is the file for the **bibliography** entries. We will do that next.

Start `TeXShop.app`. It is in the same place as `Tex Live Utility.app`

When it starts, it might jump right in your face and ask to be updated. Follow the instructions.

Then use the menu to open the LaTeX file.

![](/assets/Screen Shot 2017-04-13 at 19.45.41.png)

Yours will look similar but not the same. What you can see is text mixed with commands which look like this one: `\section{GENERAL SPECIFICATIONS}`. In the upper left corner there is a button called `Typeset`, next to it a dropdown which says `LaTeX`. Let's try and click `Typeset`

A yellow window, the **console**,  pops up and spews out lots of text.

Option A:** If all goes well**, another window pops up with a pdf file. This is the LaTeX file converted to pdf. It works! Rejoice! Celebrate the power of LaTeX. Almost feel a grey beard growing[^10]. Jump to the next section.

Option B:** If it goes pretty well**, the pdf window pops up but some parts are empty. Click `Typeset` again and see what happens. If the document looks fine now, jump to the next section.

Option C \(the tricky one\): **If it goes less than half well**, the pdf window does not pop up. The console should be still in front. Press return. Maybe you need to press it a couple of times. The pdf window pops up now. There will be some part\(s\) of the document missing, maybe a figure/image, maybe more[^11]. There will also be one or more mentions of  `LaTeX Error` in the console. This actually happened in my case, as you can see here:

![](/assets/Screen Shot 2017-04-14 at 00.50.17.png)

See the `Goto Error` button? It brings you to the location in the LaTeX file where the error happens. In my case, this is in line 204:

![](/assets/Screen Shot 2017-04-14 at 01.58.07.png)

and the error says "Unknown graphics extension: .ps". It does not recognize the image file 🤔. Now let's say you get this error and you don't even have images in your paper then the best solution is to simply delete this part and try  `Typeset` again. Problem solved. Otherwise, we need to dig deeper. The reason for this error is that the template is quite old, and `.ps`  files are a bit out of fashion. You probably won't have a `.ps`. If you include images, use  `.pdf`, `.png` or `.jpg`. If you feel in the mood for experimentation, and you want to get rid of this error, do the following:

Find the culprit image file with the  `.ps` ending in the directory with your template and double click. It will be opened in Preview. Now if you save the file, it will be saved automagically as a `.pdf` It seems that Apple also thinks that `.ps`  is outdated. Make sure you save it in the same directory with the other files.

Then change the name in the LaTeX file from  `.ps` to  `.pdf`. In my case in line 204: aisb01.pdf. Now try  `Typeset` again. It should work this time and you should see the image in your pdf. Jump to the next section.

Option D: **If it goes terribly bad**, the pdf window does not pop up at all, after pressing return repeatedly. If this is the case, it is legit to contact the editors and demand that they send you a template that works. The worst thing that can happen is that they advise to use Word \(and go back to "Pest vs. Cholera"\). The sensible thing to happen is that they extend the deadline, or allow you to send your draft as-is until they figure out what is wrong.

### Step 4: Prepare the Document

The next thing is to get a feel for the document. The beginning of my pdf looks like this:

![](/assets/Screen Shot 2017-04-13 at 23.10.04.png)

Now a couple of things:

The expample usually contains everything which may possibly be in a paper: abstract, sections with headings at different levels, enumerations, footnotes, tables, formulas, code listings, images, acknowledgement, citations and references. You might not need all of them. Maybe you don't have formulas or tables. Maybe you don't need footnotes. You don't want or need to acknowledge anyone. Then it is just to delete these parts. The rule of thumb is simple: you can always safely delete the complete paragraph, that is the content between two empty lines. This is different from the situation in Word \("Pest vs. Cholera"\).

Study the example file to figure out which parts you will need for your draft. Maybe jot down some notes. A minimal paper[^12] would have:

* a title
* your name and institution somewhere
* sections of text
* citations in the text and a list of references at the end

We focus on these first.

[^1]: Some conferences or journals have friendly editors that accept your late and half-formatted contribution by e-mail but some have automated systems that SHUT. DOWN. AT. MIDNIGHT.  

[^2]: If you are really in a hurry you might skip the next section and head to "How to do it".

[^3]: I am working with a number of assumptions here that might or might not be working for you. 

[^4]:  Else they would have provided actual formatting templates, which exist in Word, and would have given instructions how to use those. I will not go into that here.  

[^5]: [Ah, Picasso!](https://en.wikipedia.org/wiki/File:Pablo_Picasso,_1911,_The_Poet_%28Le_poète%29,_Céret,_oil_on_linen,_131.2_×_89.5_cm,_The_Solomon_R._Guggenheim_Foundation,_Peggy_Guggenheim_Collection,_Venice.jpg "Ah, Picasso!")

[^6]: That's for now. Ping me if you want this written for other choices. 

[^7]: I am aware that this is a dubious instruction but we are on a deadline \(you still have time to read the footnotes here?\) 

[^8]: "What if not?" you might ask. "Then we are in trouble", I answer. Time to contact the chair of your conference and ask for the LaTeX templates.

[^9]: Some people have set up their Finder that they can't see the endings. To fix that, go to `Finder -> Preferences -> Advanced` and change the setting \(forever\).

[^10]: If that joke doesn't make sense, please read the section "Pest vs. Cholera".

[^11]:  Culture studies or theoretical philosophy comes to mind. If you are in an "empirical" field, you probably need tables, illustrations, etc., to make a point. Poor you.

