# sudip_resume

***

This repo maintains the resume of Sudip Bhandari.

I have used [David Grant Resume](http://www.davidgrant.ca/latex_resume_template)  as a reference for this tex resume.


While compiling it might show some  \*.sty files as missing which can be resolved as:

	- Compille with latex (latex resume.tex)
- Download package from CTAN ([Installing tex packages from CTAN in linux](http://tex.stackexchange.com/questions/38978/how-can-i-manually-install-a-latex-package-debian-ubuntu-linux) )

use locate to find sty files and add them manually during compilation

*Result will be a resume.dvi file which can be converted to pdf using:*

		 (dvipdfm resume.dvi)
 In order to enable hyperlink generate pdf using the following steps:

	     (dvips resume.dvi)
	     (ps2pdf resume.ps)

*Output will be saved as resume.pdf along with some auxillary and log files*

Tuesday, 08. November 2016 01:50AM 


