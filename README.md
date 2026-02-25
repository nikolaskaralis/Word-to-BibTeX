# Word-to-BibTeX
An easy approach to convert text with citations to LaTeX/BibTeX format

**The problem**
Writing in Word and in LaTeX have distinct sets of advantages and disadvantages.

LaTeX excels in typesetting and producing beautiful, programmaticaly controlled pdf outputs. It is thus a natural solution for long-form, structured manuscripts.
However, writing the text is typically not very user friendly, and you are left looking at ugly inline text decorations like `\citep{bibtex_key}`, `\textbf{}`, etc...
Collaborating on such text is not really preferable (at least for me).

In contrast, Word excels at all these, including collaboration, clean looking text during writing etc.
But making a final beautiful text can be a strugle.

**Importantly**, adding citations in Word is easy and convenient, using various integrations such as the Zotero integration that allows you to quickly search and insert citations with a shortcut.
However, this doesn't really exist in the LaTeX world.

The solution for me to get the best of both worlds is to use Word for writing and adding the citations, but then at the final stage, move the text over to LaTeX for typesetting.

However, the main difficulty is how to deal with the citations.
Citations in word are typically added using a metadata format, that is incompatible with the BibTeX format for LaTeX.

**The solution**
Here, I have implemented an easy and generic solution to the problem.

1. In Zotero, install the [Better BibTex](https://retorque.re/zotero-better-bibtex/index.html) plugin.

2. Select all your papers, right-click -> `Better BibTeX` -> `Generate missing BibTeX key`. This needs to be done only the first time.
<p align="center">   
  <img src="https://github.com/user-attachments/assets/cbad84bd-e40d-4685-88bc-b6d9c72a425b" width="400">
</p>


3. In the Zotero preferences, in the tab _Better BibTeX_, define a desired Citation Key formula. I prefer: `auth + '_' + journal + '_' +year`

4. In the Zotero preferences, in the tab _Cite_, click _Add from File_ and add the `Word2BibTeX.csl` file from this repository.

5. Then select it from the list. It has the name: **Word2BibTeX**

6. Make sure you have installed the _Zotero Word Processor Plugin_.
   
7. Now, in Word, you can type your text as usual and add citations with your prefered citation style and shortcut (`Cmd + Shift + C` for me).
In the end, you can add your References section as usual.
<p align="center">   
  <img src="https://github.com/user-attachments/assets/553f4f0a-a4ee-41dd-8e55-df6898f09334" width="400">
</p>
Note: This is the style you prefer to look during writing, not the style for the final document in LaTeX.

8. When you are ready to move to LaTeX, just go to the Document Preferences in the Zotero tab of Word, and select **Word2BibTeX**.
<p align="center">   
  <img src="https://github.com/user-attachments/assets/1a04bf63-da0e-42eb-9caf-0ffa6fe04d32" width="400">
</p>

9. This will convert the citations in a BibTeX format and the References list in a matching format.
Now, you can copy your text to your LaTeX document and you can copy the References lists inside your _Bibliography.bib_ file so that it is processed by BibTeX.
<p align="center">   
  <img src="https://github.com/user-attachments/assets/ef126a15-1961-4a0a-a4d9-f6d813283edd" width="400">
</p>

Note: Importantly, this process is reversible, so as long as you save your Word file, you can always revert back to your prefered citation style for viewing, modify the text and then convert again to BibTeX style. However, this wouldn't work if you just copy the text from a pure LaTeX file, since it will be missing all the xml metadata.

10. Enjoy the best of both worlds! 🥳

