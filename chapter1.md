# The Emergency Chapter

_Based on a true story._

Picture yourself in this situation: You have to submit a paper or draft to this fancy conference \(or prestigous journal\) and the deadline is **tonight**. Yes, you had three months time, but for some reason creativity has only kicked in last minute. You finally managed to write your thing but now it comes down to "please provide a camera ready version" / "please format in HUMBLEMUMBLE style". The clock is ticking[^1] [^2].

## Pest or Cholera?

When you submit some academic stuff, you usually get a choice between Microsoft Word and LaTeX. You also get a link to download templates and example files to work with. What you see might look like this:

![](/assets/Screen Shot 2017-04-13 at 14.23.14.png)

The choice is obvious: they have given you **one** Word template versus **seven** strangely named files. You don't even want to know what these bib, bbl, blg, bst... things are. It is also likely that you have laid down your thoroughly crafted thoughts in Word already[^3]. So the sensible thing to do is to open the Word template and copy/paste your content over piece by piece, heading by heading, paragraph by paragraph. Actually this is what you are supposed to do according to the authors of these files[^4]. Sure there are pesky looking things like foootnotes, tables and images. And the citations and reference list have to be formatted in a certain HUMBLEMUMBLE style. Still easy enough, just keep calm and copy/paste. You start going... until something weird happens.

You have just copied some piece of text when you realize the whole paragraph now looks like the heading. You try to undo it and try again. Some text still looks strange. You look into the formats, but there are 35 of them, labelled "standard", "default text" and "paragraph". Which one? You delete the example image and copy your image in, but is too large and now it is half on the bottom of page 3 and half outside the page. Also, some of your footnotes are suddenly gone. Attempts to fix this results in more chaos. Some text is behind the picture, and trying to delete the table that you don't need also removes a paragraph on another page.

By now your paper looks like this[^5]:

![](/assets/Pablo_Picasso,_1911,_The_Poet_%28Le_poète%29,_Céret,_oil_on_linen,_131.2_×_89.5_cm,_The_Solomon_R._Guggenheim_Foundation,_Peggy_Guggenheim_Collection,_Venice.jpg)

Rest assured: This is not your fault. Also, there is no time for guilt or blame. You need to submit your paper, nothing else. Yet by now you are already going through the [five stages of grief](https://en.wikipedia.org/wiki/Kübler-Ross_model): denial, anger, bargaining, depression, acceptance. Probably during the bargaining phase, you were tempted to look at the other alternative. You googled "LaTeX", however the results did not look promising. Everything you gave a quick read sounded technical and confusing. That stuff seemed to have been written by a bunch of greybeards educating people about typesetting practices while celebrating themselves for enabling Umlauts like it's 1999. They apparently assumed that you want to spend months learning their noble craft and join the obscure guild of Ligaturists[^6] in addition to being an overworked student. This won't work.

So you decide to start over with a fresh copy of the Word template. Two hours later the second one looks like the first. You are chasing your single image through the text. Stuff appears and disappears at random. You also realize that you still have to change the appearence and order of the references one by one. Suddenly a shrill alarm sounds. Midnight!

**GAME OVER**

## How to do it

Let's rewind the clock for a few hours and try again. This assumes:

1. You are on a \(fairly recent\) Mac[^7]. You have 10 Gigabyte \(GB\) of free space on your harddisk. You should be on a fast internet and you must have the password for your account.
2. You have to submit a formatted paper \(draft, proposal\) and you are on a tight deadline.
3. You have written your paper already, probably in Word, Libre Office, Pages or another editor. You also should have prepared your bibliography, either in Word, a reference manager, or on a piece of paper. 
4. Your work is not too complicated, mainly text, maybe a table, a few images, a handful of references and stuff. Also, no formulas[^15].
5. **You have received LaTeX templates / example files from the journal or conference like the ones pictured above. If you don't, now is the time to get them / look for them on their website. This guide assumes that you have them !1!! **

Our goal is to submit a PDF which is typeset in LaTeX. We will go through a number of steps: first install LaTeX, update it, check the template files, prepare the document, copy the text, format images and tables, and finally do the citations and bibliography. We will do the same copy-and-paste approach as with Word, so you don't have to grow a grey beard and learn LaTeX. It should take 3-5 hours for a 6-10 page paper if all goes well. Roughly 1 1/2 hour will be spent installing and updating LaTeX \(while you can do other things in between, like proofreading your paper once again\).

### Step 1: Install LaTeX

Go to [http://www.tug.org/mactex/mactex-download.html](http://www.tug.org/mactex/mactex-download.html). Download the installer [**MacTeX.pkg**](http://tug.org/cgi-bin/mactex-download/MacTeX.pkg). Ignore everything that is written on the page[^8]. The download will take some time. Make tea.

Run the installer. It walks you through the process. The installation will take some time as well. The program might try to scare you:

![](/assets/Screen Shot 2017-04-13 at 21.08.05.png)

\(in practice it is more like 30 minutes\). During the installation it might ask you to install another piece of software named "XQuartz". Follow the instructions and install this as well. After the installation is finished you can delete the files you have downloaded.

### Step 2: Update LaTeX

In your `Applications` you now have a folder named `TeX`. Start the `Tex Live Utility.app` from there. It greets you with a window like this:

![](/assets/Screen Shot 2017-04-13 at 18.39.01.png)

First check under Preferences if `Tex Live Utility`  itself wants to be updated. If so, follow the instructions.

Note that the list it displays may be empty, says "No update available" or contains some entries. In these cases, click the little circular arrow

![](/assets/Screen Shot 2017-04-13 at 18.43.26.png)

.. and wait. Then there should be a list of entries. The program might tell you again that it needs to update itself and ask for your password, etc. Confirm everything. Then in the Menu select `Actions -> Update all Packages`.

It will take a significant amount of time to download and update everything. Up to an hour, maybe. Time to re-read your paper?

If the update fails: try again. Try closing Tex Live Utility and starting it again. Check if you are connected to the internet. If you have a hundred programs open on your Mac, you want to close them down, restart your Mac and focus. What you finally want to see is this:

![](/assets/Screen Shot 2017-04-13 at 18.44.25.png)

You can close `Tex Live Utility` for now, consume some sweets and get ready.

### Step 3: Check your Templates

I assume you have already a folder with the LaTeX templates / example files from your conference or journal[^9]. If not, do that  now. Make a copy of the folder in case things go wrong. You also have your text somewhere, in Word for example.

Let's look at the LaTeX files.

![](/assets/Untitled.png)

Yours will have different names and some different symbols. There might be more or less of them. But you should have in any case[^10]:

1. a file with the extension ".tex". This is **the LaTeX file** we will work with. Your paper will go in there. We will focus on this first.
2. a file with the extension ".bib". This is the **BibTeX file** for the bibliography entries. We will do that later.

Start `TeXShop.app`. It is in the same place as `Tex Live Utility.app`

When it starts, it might jump right in your face and ask to be updated. Follow the instructions.

Then use the menu to open the LaTeX file.

![](/assets/Screen Shot 2017-04-13 at 19.45.41.png)

Yours will look similar but not the same. What you can see is text mixed with commands, which look like this one: `\section{GENERAL SPECIFICATIONS}`. In the upper left corner there is a button called `Typeset`, next to it a dropdown which says `LaTeX`. Let's try and click `Typeset`.

A yellow window, the **console**,  pops up and spews out lots of text.

Option A:** If all goes well**, another window pops up with a PDF file. This is the LaTeX file converted to PDF. It works! Rejoice! Celebrate the power of LaTeX. Almost feel a grey beard growing[^11]. Jump to the next section.

Option B:** If it goes pretty well**, the PDF window pops up but some parts are empty. Click `Typeset` again and see what happens. If the document looks fine now, jump to the next section.

Option C \(the tricky one\): **If it goes not so well**, the PDF window does not pop up. Click on the console, then press return. Maybe you need to press return a couple of times. The PDF window finally opens. There will be some part\(s\) of the document missing, maybe a figure/image, maybe more[^12]. There will also be one or more mentions of  `LaTeX Error` in the console. This actually happened in my case, as you can see here:

![](/assets/Screen Shot 2017-04-14 at 00.50.17.png)

See the `Goto Error` button? It brings you to the location in the LaTeX file where the error happens. In my case, this was in line 204:

![](/assets/Screen Shot 2017-04-14 at 01.58.07.png)

and the error says "Unknown graphics extension: .ps". It does not recognize the image file 🤔. Now let's say you have this error and you don't even have images in your paper then the best solution is to simply delete this part and try  `Typeset` again. Problem solved. Otherwise, we need to dig deeper. The reason for this error is that the template is quite old, and `.ps`  files are a bit out of fashion. You probably won't use a `.ps`. If you include images, use  `.pdf`, `.png` or `.jpg`. If you do have this error in your template, feel in the mood for experimentation, and you want to get rid of this error, do the following:

Find the culprit image file with the  `.ps` ending in the directory with your template and double click. It will be opened in Preview. Now if you save the file, it will be saved automagically as a `.pdf` It seems that Apple also thinks that `.ps`  is outdated. Make sure you save the PDF in the same directory with the other files.

Then change the name in the LaTeX file from  `.ps` to  `.pdf`. In my case in line 204: `aisb01.pdf`. Now try  `Typeset` again. It should work this time and you should see the image in your PDF. Jump to the next section.

Option D: **If it goes terribly bad**, the PDF window does not pop up at all, even after pressing return repeatedly. If this is the case, it is legit to contact the editors and demand that they send you a template that works. The worst thing that can happen is that they advise to use Word \(and go back to [Pest vs. Cholera](#pest-vs-cholera)\). The sensible thing to happen is that they extend the deadline, or allow you to send your draft as-is until they figure out what is wrong with their template.

### Step 4: Prepare the Document

The next step is to take 10 minutes and get a feel for the document. The beginning of my PDF looks like this:

![](/assets/Screen Shot 2017-04-13 at 23.10.04.png)

Now a couple of things:

When you look at the LaTeX source file in TexShop and you look at the PDF, you are looking at the **same document**. The first one is the source and the second one the result of the layout process. So you can see in my example that there is a title in the PDF and placeholders for the authors' names, followed by an abstract. In the source file these elements are:

```latex
\title{Guidelines for Preparing a Paper for the \\ 
European Conference on Artificial Intelligence}
```

```latex
\author{Name1 Surname1 \and Name2 Surname2 \and Name3 Surname3\institute{University of Leipzig,
Germany, email: somename@informatik.uni-leipzig.de} }
```

```latex
\begin{abstract}
The purpose of this paper is to show a contributor the required
style for a paper for AISB 2008. The specifications
for layout are described so that non-\LaTeX\ users can create their
own style sheet to achieve the same layout. The source for the
sample file is available for \LaTeX\ users. The PostScript and the
PDF file is available for all.
\end{abstract}
```

You will find the same or similar elements. You can see some text, commands that begin with a backslash `\` , and parameters to those commands that are between curly braces `{ }`. There will be a `\begin{document}` near the top and a `\end{document}` at the end. Notice also how the coloring in TexShop \(which might have slightly different colors than the ones shown here\) helps to spot the commands.

Study your LaTeX source and the PDF it generated to identify these elements. The people who prepared the example usually want to demonstrate everything which may possibly appear in a paper: title, author\(s\), abstract, sections with headings at different levels, enumerations, footnotes, tables, formulas, code listings, images, acknowledgement, citations and references. You might not need all of them. Maybe you don't have formulas or tables. Maybe you don't need footnotes. Or you don't want to acknowledge anyone.

For now just ignore the parts you don't need. We will delete them later. The rule of thumb is: you can always safely delete a complete paragraph, that is the content between two empty lines, if you don't need it. This is different from the situation in Word \(see [Pest or Cholera?](#pest-vs-cholera)\). Just don't delete anything now.

Instead check your paper to figure out the parts you do need for your draft. A minimal paper[^13] usually would have:

1. a title
2. your name\(s\) and institution\(s\) somewhere
3. an abstract
4. sections of text
5. a bibliography with citations in the text and list of references at the end

We focus on the first four for now.

#### Title

You already located the title element in TexShop. Replace the text between curly braces `{ }` with your actual title and run `Typeset` again. At the beginning I would recommend to do this after each change. You can see if the results are as expected and spot potential problems. Use Edit -&gt; Undo \(`cmd-Z`\) to undo a change and save the LaTeX file with Edit-&gt;Save \(`cmd-S`\).

Does it work? Do you see your title in the PDF? Congratulations.

_A journey of a thousand miles begins with a single step _\(Lao-Tse\). You just have taken that step. Let's move on.

#### Name\(s\) and Institution\(s\)

Now replace the names and institutions of the author\(s\). Check carefully what to replace. In my paper the names are put below the title and the institutions and e-mail adresses are set in a footnote. This is done automatically by the template. I did not have to say "put them in the footnote". When we work with a template that has been provided to us, we only need to replace the content, we do not need to layout the paper. This has been done for us already[^15]

#### Abstract

The abstract of your paper goes between

```latex
\begin{abstract}
```

and

```latex
\end{abstract}
```

If you don't need an abstract \(for example when you are submitting an extended abstract, you won't need an abstract of the abstract\), just delete the whole paragraph including the `\begin{abstract}` and `\end{abstract}` commands.

#### Text

Now to the main text. It will have a number of sections with headings. For a section, replace the text between the curly braces with your heading:

```latex
\section{HEADING TEXT}
```

Then, starting immediately on the next line, add the paragraph\(s\) of text that go into the section. Leave an empty line between paragraphs and one before the nect section. Go through your paper like this, section by section. Run `Typeset` after each section, look at the PDF,  and save the file if it looks good. If you have subsections, put in `\subsection`  commands and if you have even more deeper levels of headings,  `\subsubsection`.

If you encounter problems after inserting a block of text, look at the content. It is likely that your text contains

* special characters, described below in [Special Characters](#special-characters), or
* characters in a international language, see [International Languages](#international-languages).

If you cannot locate the problem, divide the text that you insert in half, see which part triggers an error and repeat.

Another potential source for problems is that LaTeX creates some additional files during the whole process. We normally do not care about them but they might disturb the machinery. In [Step 3: Check the Template](#step-3-check-the-template) we saw the console window. It has a button in the upper right corner that says: `Trash Aux Files`. Click it and try to `Typeset` again.

When you are done and without errors, you have the complete text of your paper in the LaTeX file, still followed by the example stuff.

If you have any of the elements: acknowledgement, crossreferences, emphasized text, enumerations, figures, footnotes, international languages, line breaks, special characters, or tables, please continue below. Just pick the ones that you need. When finished, head to [Clean up](#clean-up).

#### Acknowledgement

The acknowledgement comes at the end of the paper and contains heartfelt a thank you to supervisors, referees, editors or partners \(who kept being friendly and supportive during the breakdown mentioned above\). Also shoutouts to your funding, which is sometimes required. Thankfully this is straightforward: `\ack` command, followed by the text on the next line. Note that the acknowlegement is usually not numbered, even if your other headings are.

#### Crossreferences

In order for crossreferences to work, you must run `Typeset` **twice**[^14].

You might want to reference a table \(like: see section [Tables](#tables)\), image or section in your paper. There are three parts to a reference. First, you must give it a **name**. Then you put a **label** with that name `\label{name}` right after the element you want to reference. Finally you put the **reference** `\ref{name}` or page reference `\pageref{name}` where the reference should appear in your text.

Example 1: You want to mention your conclusion section. Place the label right after the section command like this:

```latex
\section{Conclusion}\label{conclusion}
```

Then somewhere else in your text:

```latex
See also Section \ref{conclusion} on page \pageref{conclusion}.
```

The result will be \(assumed the conclusion is your fifth section on page 4\):

See also Section 5 on page 4.

Example 2: You want to reference a table or figure. Let's look again at the figure example from [Images](#images). The label is inside the table or figure, right after the caption command:

```latex
\begin{figure}
\centerline{\includegraphics[height=3.5in]{aisbf01.pdf}}
\caption{Network of transputers and the structure of individual
processes } \label{procstructfig}
\end{figure}
```

Then, somewhere else in the text:

```latex
See Figure \ref{procstructfig}.
```

will produce:

See Figure 1.

The same approach will work with a [table](#tables). LaTeX will take care about the numbering of these items automatically.

#### Emphasized Text

Use `\emph{text}`.

#### Enumerations

Follow the same approach with enumerations, that is is numbered lists or bulletpoints. Find them in the example LaTeX file and replace the content, then copy/paste the result. When you are done delete the original section.

Numbered lists begin with `\begin{enumerate}` and end with `\end{enumerate}`. Bullertpoint lists begin with `\begin{itemize}` and end with `\end{itemize}`. Each of the list items starts with `\item` followed by the text.

This replace-content-then-copy-then-delete-the original-section has become our workflow, but you can just as well write the commands yourself if you prefer by now. Each time you run `Typeset,`the console window will tell you if you made errors and the PDF that pops up will show if everything is as planned.

#### Figures

Including images and illustrations in a paper sounds daunting and it can be a bit more complicated in LaTeX if you do it from scratch. Fortunately this does not apply here. First find the location of an image in the LaTeX example file. Often there are different examples of figures given, full-sized ones, and smaller ones that span one column in a two column layout for example. In my paper it looks like this:

```latex
\begin{figure}
\centerline{\includegraphics[height=3.5in]{aisbf01.pdf}}
\caption{Network of transputers and the structure of individual
processes } \label{procstructfig}
\end{figure}
```

As mentioned in [Step 3: Check the Template](#step-3-check-the-template), LaTeX wants images in either  `.pdf`, `.png` or `.jpg` formats. Your template may accept different ones as well, but these three are usually safe to use. If you haven't done it yet, prepare your image and copy the image file into the directory with the other files. Give it a simple file name without spaces or fancy characters in it.

Then replace the example filename with your image filename. Here this is within the command  `\includegraphics[height=3.5in]{aisbf01.pdf}}`. In your case this might be a different command but there will be a filename of the image to be included. Run `Typeset` and if the image doesn't show up, run it again. If it still does not show up, check the console for errors like I did in [Step 3: Check the Template](#step-3-check-the-template). The error might tell you something, maybe it just didn't find the image. In this case double check that the image file is actually in the directory and that the filenames match. If it appears that there are other problems, try the following. Find a `.jpg`file on the internet and try to include this one. If that works then maybe something is wrong with your image. Try to open it in another program and export/save a new version. If all this doesn't help, consult some of the resources in chapter [Where to Get Help](/where-to-get-help.md).

If all went well, edit the `\caption` by replacing the text between the curly braces. By now this process should be familiar. Finally move the whole block to the position where you want the image to appear. You might have to experiment a little, and LaTeX will re-position your image if you attempt something frivoulous, like putting an image at the bottom of a page. But you can see that text and image will live in harmony, the text flowing nicely around the image. Just keep an empty line above and below the `figure` command block.

Do this with your other images and don't forget to delete leftovers of the example content when you are done.

#### Footnotes

You will find at least one footnote in your example LaTeX file, and it looks like this  `\footnote{Text of the footnote.}` Insert this command right after the word or sente nce where the footnote sign should appear. Write the text of your footnote between the curly braces. LaTeX will automatically enumerate, layout and place your footnotes, and it will work.

#### International Languages

#### Line Breaks

Unlike Word, LaTeX does not create a linebreak where it finds one in the input file. So you have to say explicitely if you want a linebreak with: `\\`. Separate paragraphs with a empty line.

#### Special Characters

Some characters are part of LaTeX, others have to be input via special commands. If you copy them directlz from your Word text, LaTeX will either throw errors at you, do silly things, or passiv-aggressively refuse to display the character in the PDF.

Consult the table and replace the item on the left side with the one on the right. Often you just need to put a backslash `\` in front of it.

| To display this character in the PDF... | ...insert this into your LaTeX file: |
| :--- | :--- |
| \# | \\# |
| $ | $ |
| % | \% |
| ^ | \^ |
| & | \& |
| \_ | \\_ |
| { | { |
| } | } |
| ~ | $\sim$ |
| \ | \textbackslash |

#### Tables

Brace yourself. If working with images looked a bit intimidating, tables can be really frightening. There are two reasons. First, academics need to produce the most weird and convoluted tables out there. You won't get a PhD if you include a table which just consists of rows and columns. Also, the example table in your LaTeX file will be proof of that. Then, because a table in LaTeX has to be constructed by commands, it will look horrible. This is the code for the table in my example file:

```latex
\begin{table}
\begin{center}
{\caption{The table caption is centered on the table measure. If it
extends to two lines each is centered.}\label{table1}}
\begin{tabular}{lccccccc}
\hline
\rule{0pt}{12pt}
&\multicolumn{7}{c}{Processors}\\
&1&\multicolumn{3}{c}{2}&\multicolumn{3}{c}{4}\\
\cline{2-8}
\rule{0pt}{12pt}
Window&$\Diamond$&$\Diamond$&$\Box$&$\bigtriangleup$&$\Diamond$&$\Box$&$\bigtriangleup$
\\
\hline
\\[-6pt]
\quad1&1273&110&21.79&89\%&6717&22.42&61\%\\
\quad2&2145&116&10.99&50\%&5386&10.77&19\%\\
\quad3&3014&117&41.77&89\%&7783&42.31&58\%\\
\quad4&4753&151&71.55&77\%&7477&61.97&49\%\\
\quad5&5576&148&61.60&80\%&7551&91.80&45\%
\\
\hline
\\[-6pt]
\multicolumn{8}{l}{$\Diamond$ execution time in ticks\ \
$\Box$ speed-up values\ \
$\bigtriangleup$ efficiency values}
\end{tabular}
\end{center}
\end{table}
```

And it produces a table like this:

![](/assets/Screen Shot 2017-04-22 at 02.03.54.png)

I assume you don't have a master's degree in table-making. At I least I don't. I know that tables are made of cells that are arranged in rows and columns. There might be special looking row and column headers, and sometimes the  content spans multiple cells. Cells can, but don't have to be separated by lines. A table in a publication normally has a caption.

In the light of this, the code above LaTeX snippet looks terribly complicated. Our goal is to include a table in the paper and we have a more complicated one as an example. What to to do?

Let's analyze the thing first. The whole table is between `\begin{table}` and `\end{table}`. Then what is inside the table is centered with `\begin{center}` and `\end{center}`. The next thing is the caption:

```latex
{\caption{The table caption is centered on the table measure. If it 
extends to two lines each is centered.}\label{table1}}
```

There you just replace the caption text. It has a label which is invisible in the paper but used for crossreferencing, explained in the next section. No harm in leaving it in. The actual table content is between `\begin{tabular}{lccccccc}` and `\end{tabular}`. The `lccccccc` parameter says: make a table with 8 columns, the first one where the content is left justified and 7 more where the text is centered. You might also see `r` which means the text is right justified, and there might be vertical dashes`|`which tell LaTeX to draw a vertical lines between the columns.

* `&` starts the next cell / column
* `\\` starts a new line and
* `\hline` inserts a horizontal line

Ok, now we can build our table \(I used the part with the numbers from the table above\).

```latex
\begin{table}
\begin{center}
\caption{The table caption is centered on the table measure. If it
extends to two lines each is centered.} \label{table1}
\bigskip
\begin{tabular}{|l|c|c|c|c|c|c|c|}
\hline
\multicolumn{8}{|c|}{Lots of numbers}\\
\hline
1&1273&110&21.79&89\%&6717&22.42&61\%\\
\hline
2&2145&116&10.99&50\%&5386&10.77&19\%\\
\hline
3&3014&117&41.77&89\%&7783&42.31&58\%\\
\hline
4&4753&151&71.55&77\%&7477&61.97&49\%\\
\hline
5&5576&148&61.60&80\%&7551&91.80&45\%\\
\hline
\end{tabular}
\end{center}
\end{table}
```

which now looks like:

![](/assets/Screen Shot 2017-04-23 at 00.48.06.png)

I used `\bigskip` to create a space between the label and the table. In your template there might be a different command located between `\caption` and `\begin{tabular}` to achieve the same goal. The line `\multicolumn{8}{|c|}{Lots of numbers}\\`shows the text "Lots of numbers" spanning 8 columns, centered and with vertical lines like the rest of our table.

Note that in LaTeX a percentage sign must be written as `\%`. To learn about this and other special characters, check out [Special Characters](#special-characters).

### Step 5: Clean up

At this point your complete paper, possibly including illustrations, tables, footnotes etc. should be typeset in LaTeX. Congratulations. If it isn't yet, go back to the sections above and finish the work. At the end you might still have some of the example content in the paper. Now it is time to delete it, except for the bibliography. Be careful - **don't just delete the rest of the file**. At the end there are some lines you must keep. Those usually start with the `\bibliography` command. In my file the ones to keep look like this:

```latex
\bibliography{aisb}

\end{document}
```

Remember the rule of thumb about deleting sample content in LaTeX: you can always safely delete a complete paragraph, that is the content between two empty lines. Then run `Typeset` and check the results. Repeat until done.

Time for a coffee break. One more to go.

### Step 6: Bibliography

Everyone in academia loves bibliography. Without it, nobody would be able to trust what you write. It could be your own ideas! Ok, back to work. A bibliography consists of:

1. a list of references at the end of your paper
2. citations in the text which point to references
3. a style which is applied to citations and references. The style determines for example if the citations are numbers or name and year, if first names are abbreviated and in which order the elements of the reference appear. You may have heard about APA, Chicago, ACM, or Harvard referencing style. Truth is there are a few thousand styles out there, "Harvard style" can mean anything under the sun, and formatting the bibliography can be a pain. The good news: you don't need to care. LaTeX does this for you.    

Let's take a look at the bibliography in my example:![](/assets/Screen Shot 2017-05-04 at 21.50.54.png)

Now, in your PDF file you should still see the example bibliograpy that came with your template. Maybe you have wondered where those entries come from. You can't find them in your LaTeX file. Where are they 🤔?

Let's look at the bibliography command again, in my case  `\bibliography{aisb}`. You will have a similar entry. The parameter `aisb` means that there is a file with the name `aisb.bib` \(called a "BibTeX file"\)** **that has the bibliographical entries. Let's open the BibTeX file in TeXShop with `File -> Open`. Ok, here are the entries \(I left most of them out\):

```bibtex
@book{kn:Golub89,
    author = "Golub, G.H. and {Van Loan}, C.F.",
    title = "Matrix Computations",
    edition = "2nd",
    publisher = "Johns Hopkins University Press",
    address = "Baltimore",
    year = "1989",
    kwds = "la"
}

@inbook{kn:daCunha92a,
    author = "{da Cunha}, R.D. and Hopkins, T.R.",
    title = "The Parallel Solution of Systems of Linear Equations using
              Iterative Methods on Transputer Networks",
    series = "Transputing for Numerical and Neural Network Applications",
    pages = "1-13",
    publisher = "IOS Press",
    address = "Amsterdam",
    year = "1992",
    note = "Also as Report No. 16/92, Computing Laboratory, University of Kent at Canterbury, U.K.",
    kwds = "par, iter"
}

@misc{kn:Atkin,
    author = "Atkin, P.",
    title = "Performance Maximisation",
    howpublished = "INMOS Technical Note 17",
    kwds = "perf, trans, loop"
}

@article{kn:Saad85,
    author = "Saad, Y.",
    title = "Practical use of polynomial preconditionings for the
              {Conjugate Gradient} method",
    journal = "SIAM Journal of Scientific and Statistical Computing",
    volume = "6",
    pages = "865-881",
    year = "1985",
    kwds = "cg, precon, poly"
}
```

Take a deep breath and get familiar with your entries. They will have different information but the structure is similar to mine. The type of the reference, like `@article` is followed by a structure inside curly braces `{}`, with a citation key \(`kn:Saad85`[^16]\) and a number of fields like \( `author = "Saad, Y."`\). Field entries are between quotation marks, or alternatively between curly braces. Some fields are optional like `kwds` above, which is a list of keywords that does not show up in the output.

You can probably see types like `@book`, `@inbook` \(a book chapter\) and `@article` \(a journal article\). If you do not find the ones that you need in your example, there is an overwiew [at Wikipedia](https://en.wikipedia.org/wiki/BibTeX#Entry_types) that also lists required and optional fields for each type of entry.

The next step depends on this: Are you already using a reference manager software such as [Zotero](https://www.zotero.org/), [Mendeley](https://www.mendeley.com/), or [Endnote](http://endnote.com/)? If you do, this will make things easier; please skip to [Bibliography with a Reference Manager](#bibliography-with-a-reference-manager). If you don't, I would recommend to do so in the future \(chapter [How to Write a Thesis](/how-to-write-a-thesis.md) will describe this\), but for now let's stay with the manual option.

#### Bibliography the Manual Way

Ok, time to do the bibliography. Make a list of your references \(let's say you have 2 books, 2 chapters in a collection, 5 journal articles, 2 conference talks that are published in proceedings and a phd thesis\). Prepare the respective number of empty entries \(you can copy them from here or remove content from the examples in your templates\)[^18]. Check the [Wikipedia](https://en.wikipedia.org/wiki/BibTeX#Entry_types) entry for different  entry types and possible fields. Finally delete the example entries that are still in the file and save it. You should have exactly one empty template for each ouf your references at this point.

```bibtex
@book{,
    author = "",
    title = "",
    edition = "",
    publisher = "",
    address = "",
    year = ""
}

@incollection{,
    author = "",
    title = "",
    booktitle = "",
    editor = "",
    series = "",
    pages = "",
    publisher = "",
    address = "",
    year = ""
}

@article{,
    author = "",
    title = "",
    journal = "",
    volume = "",
    number = "",
    pages = "",
    year = ""
}

@inproceedings{,
    author = "",
    title = "",
    booktitle = "",
    volume = "",
    pages = "",
    year = ""
}

@phdthesis{,
    author = "",
    title = "",
    school = "",
    year = ""
}
```

Now insert information for one of your references[^17]. First the citation key. You can name the key as you like. I recommend going with something like first author in lowercase and year, which helps to stay consistent. For example this would be `golub1989` and it comes between the opening curly brace and the first comma. Fill in the field values between the quotation marks. Finally you have something like this:

```bibtex
@book{golub89,
    author = "Golub, G.H. and {Van Loan}, C.F.",
    title = "Matrix Computations",
    edition = "2nd",
    publisher = "Johns Hopkins University Press",
    address = "Baltimore",
    year = "1989",
}
```

Save the BibTeX file. Now head over to your LaTeX file and insert the citation at the location where you want the mark to appear. In my case this is  `\cite{golub1989}`.

Just a quick reminder for orientation. At this point you have 4 different windows open in `TexShop`. The one with the LaTeX file, the one with the BibTeX file we are working on , one console window for messages and the one with the PDF output. Sometimes these windows overlap or are minimized.



#### Bibliography with a Reference Manager

### Step 7: Proofread and Submit

[^1]: Some conferences or journals have friendly editors that accept your late and half-formatted contribution by e-mail but some have automated systems that SHUT. DOWN. AT. MIDNIGHT.  

[^2]: If you are really in a hurry you might skip the next section and head to "How to do it". Also, ignore the footnotes from now on. They contain non-critical information.

[^3]: I am working with a number of assumptions here that might or might not be working for you. 

[^4]:  If this was not the case, they would have provided actual formatting templates, which exist in Word, and would have given instructions how to use those. I will not go into that here.  

[^5]: [Ah, Picasso!](https://en.wikipedia.org/wiki/File:Pablo_Picasso,_1911,_The_Poet_%28Le_poète%29,_Céret,_oil_on_linen,_131.2_×_89.5_cm,_The_Solomon_R._Guggenheim_Foundation,_Peggy_Guggenheim_Collection,_Venice.jpg "Ah, Picasso!")

[^6]: I made this up, there are no "Ligaturists". But it feels like there could be.

[^7]: That's for now. Ping me if you want this written for other choices. 

[^8]: I am aware that this is a dubious instruction but we are on a deadline \(you still have time to read the footnotes here?\) 

[^9]: "What if not?" you might ask. "Then we are in trouble", I answer. Time to contact the chair of your conference and ask for the LaTeX templates.

[^10]:  Some people have set up their Finder that they can't see the endings. To fix that, go to `Finder -> Preferences -> Advanced` and change the setting \(forever\).

[^11]:  If that joke doesn't make sense, please read the section [Pest or Cholera?](#pest-vs-cholera).

[^12]:  Culture studies or theoretical philosophy comes to mind. If you are in an "empirical" field, you probably need tables, illustrations, etc., to make a point. Poor you.

[^13]:  If you wonder how LaTeX knows about the style of your paper, this is in one of the files mentioned in [Pest vs. Cholera](#pest-vs-cholera), namely the file with the ending `.cls`. You don't need to touch this file, but if you had to change how things look, it would be there.

[^15]:  This goes for other things as well like a table of contents. LaTeX must run twice through the source to create these things and the greybeards haven't figured out yet how to automate this.

[^15]:  My \(crude\) reasoning is that if you would have formulas in your paper, you would know LaTeX already. I willl cover formulas in [How to Write a Thesis](/how-to-write-a-thesis.md)

[^16]:  There is a joke in the choice of this key, but I can't tell it here.

[^17]:  The order in which you in the .bib file doesn't matter, BibTeX will figure that out and put the references in the right order .

[^18]:  You are more like to make a mistake if you copy your information directly into the example entries. That's why we use empty ones.  

