# sudip_resume

***

This repo maintains the resume of Sudip Bhandari.

I have used [David Grant Resume](http://www.davidgrant.ca/latex_resume_template)  as a reference for this tex resume.


While compiling it might show some  \*.sty files as missing which can be resolved as:

	- Compille with latex (latex resume.tex)
	Install tex: 

	(sudo apt install texlive-latex-base)

- Download package from CTAN ([Installing tex packages from CTAN in linux](http://tex.stackexchange.com/questions/38978/how-can-i-manually-install-a-latex-package-debian-ubuntu-linux) )  [shading package CTAN](https://ctan.org/tex-archive/macros/latex209/contrib/shading)

use locate to find sty files and add them manually during compilation

*Result will be a resume.dvi file which can be converted to pdf using:*

		 (dvipdfm resume.dvi)
 In order to enable hyperlink generate pdf using the following steps:

	     (dvips resume.dvi)
	     (ps2pdf resume.ps)

*Output will be saved as resume.pdf along with some auxillary and log files*


## Git hook to automate above stuffs

Create a file named: 

`.git/hooks/pre-commit`

Make it executable: `sudo chmod +x .git/hooks/pre-commit`

Populate with following content:

```sh
latex resume.tex #latex compilation
dvipdfm resume.dvi #dvi conversion
dvips resume.dvi #enabling hyperlinks
ps2pdf resume.ps
git add -A #adding to staging area for commit
```


Tuesday, 08. November 2016 01:50AM 


