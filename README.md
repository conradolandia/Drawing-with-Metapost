# Drawing-with-Metapost

Some intermediate examples of how to draw technical diagrams with John Hobby's Metapost language.
See http://www.tug.org/metapost.html for more about Metapost.  

Start with "Drawing-with-Metapost.pdf" in this directory.

The `src` directory contains 
- the TeX source for the main document
- the style file used for marking up Metapost source code
- the Metapost source for each illustration used in the main document
- the corresponding PDF file created from the MP source

You might like to read the main document first, but you might also like to 
browse through the PDFs in the src directory, and when you find one that is interesting, 
have a look at the corresponding MP source file.  There is a one-to-one match between the PDF 
names and the MP source names, so "apollonius.pdf" is created from "apollonius.mp"

To build the main PDF document I follow these steps

- build any new or updated Metapost source files with `lualatex` to create a PDF in the src directory
- build the main tex file with `lualatex -output-directory=.. -recorder Drawing-with-Metapost`
- run a Python script to read the .fls and `git add` all the files used

Toby Thurston -- 05 Apr 2023
