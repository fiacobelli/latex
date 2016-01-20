#Installing the Themes#

##In MikTex##
   - Copy the .sty files of the theme to the respective subdirectories under the $(MIKTEX_ROOT)\tex\latex\beamer\base\themes\ directory. For example, beamerthemeuno.sty goes into the theme subdirectory, beamercolorthemeuno.sty goes into the color subdirectory and so on.
   - Refresh the MikTeX file name database. You may need to close all applications that use LaTeX for this operation to complete successfully.

##In MacOS/Unix?##
First, obtain the path to your global or local latex directory (You can install it either for everyone or just for you).
The command
   
    kpsexpand \$TEXMFLOCAL

will show you the path to the local system-wide tree which will not be modifed by updates of TL; it will usually be "next" to the texmf tree, as @sigur says.

    kpsexpand \$TEXMFHOME

will show you the path to your user-specific tree, probably /home/(username)/texmf. (For more information, see TeXlive docs on user texmf trees, in particular the statement-by-omission that you don't need to refresh filename databases for new files in TEXMFHOME.

    - Now, from there, navigate to `tex/latex/beamer` directory. You can create it if it is not there (i.e. you don't have it in your local directory).
    - Then make a directory for your theme and put the `.sty` files in there.
