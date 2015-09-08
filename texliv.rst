0) install texlive
 o get texlive install packet(installed from network)
   wget http://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz

 o uncompress install-tl-unx.tar.gz then 
   sh install-tl

 o set enviroment
   add "/usr/local/texlive/2014/bin/x86_64-linux" to PATH
   or edit /etc/enviroment or edit /etc/sudoers

 o update emcas's org-mode
   M-x packet-install RET org

 o edit .emacs file
   add follows:
   (setq org-latex-pdf-process '("xelatex -interaction nonstopmode %f"
                                "xelatex -interaction nonstopmode %f"))

 o install xecjk

 o add new fonts
   mv *.otf to /usr/share/fonts/truetype/adobe
   fc-cache -r -v 
   fc-list 

 o usepackage/xecjk
   \usepackage{xeCJK}
   \setCJKmainfont[BoldFont=Adobe Heiti Std,ItalicFont=Adobe Kaiti Std]{Adobe Song Std}

1) install pgf/tikz 3.0.0
   o get pgf_3.0.0.tds.zip
     wget http://liquidtelecom.dl.sourceforge.net/project/pgf/pgf/version%203.0.0/pgf_3.0.0.tds.zip
   o uncompress 
     uncompress the .zip file to /usr/share/texmf/
   o texhash
