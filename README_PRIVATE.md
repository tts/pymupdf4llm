# pymupdf4llm, my edition

Trying to fix newline issues in my original two column PDF file. As of now, all end-of-line hyphens are replaced by space which splits words. To prevent that from happening, removing the replace clause as discussed [here](https://github.com/pymupdf/PyMuPDF-Utilities/discussions/141#discussioncomment-10477020)

That was a wrong path. The problem is the soft hyphen which is silently replaced by a space when the string is written out in the file. The solution is either to remove the hyphen, or replace it with some other char for later processing.