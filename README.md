# hasktags emacs

  This library tries to intergrate hasktags into emacs in a more automated way making it easier to navigate through Your code in emacs.

# usage

  To be able to navigate through Your haskell code in emacs faster, You may want to tag Your code and use etags library supplied with emacs to do that.

  One of such tools is hasktags and You can find some information on it on [Haskell Wiki](http://www.haskell.org/haskellwiki/Hasktags#Haskell_tag_generators)
  The program itself can be found in [Hackage](http://hackage.haskell.org/package/hasktags)

  To use the tags automatically, I've created a script for emacs, which would regenerate the TAGS when You save your file.

  So, please install hasktags first:

    cabal install hasktags

  clone the project directory into your preferred location for emacs tools

    git clone git://github.com/Kerestey/hasktags-emacs.git

  and add these two lines into your .emacs file

    (add-to-list 'load-path "<path-to-hasktags-emacs-directory>")
    (load "hasktags")

  
  To help emacs locate Your project correctly, You will have to create TAGS file in Your project root directory.
  Just `echo -n > TAGS` and You are good to go.

  You can now navigate to the function definitions using `M-.` and also use the other functionalities described in [Emacs Wiki - EmacsTags Article](http://www.emacswiki.org/emacs/EmacsTags)