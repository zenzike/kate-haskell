Kate Haskell Syntax
===================

This code provides syntax highlighting for Haskell files in Kate.
Here are some features:

* Operators are supported (++, !, >>=, and any other combination of legal operator characters)
* Special symbols are recognised (=>, <-, ->, ::, ..)
* Unicode support for  →, ←, ∷, ‥,⇒, ∀, ∃
* Support for qualified module functions (List.sort, etc)
* Support for qualified module types
* Support for literate code (using > and \begin{code} \end{code})
* Support for literate specifications (using < and \begin{spec} \end{spec})

You can see some examples of its use at [zenzike.com](http://zenzike.com/).

Installation
------------

To install these files simply copy the xml files into the kate configuration directory:

    git clone git://github.com/zenzike/kate-haskell.git
    cd kate-haskell
    cp haskell.xml ~/.kde/share/apps/katepart/syntax/
    cp literate-haskell.xml ~/.kde/share/apps/katepart/syntax/

Testing
-------

These files should be tested against the 
[Kate language DTD](http://gitorious.org/kate/kate/blobs/master/part/syntax/data/language.dtd)
before pushing
[upstream](mailto:kwrite-devel@kde.org):

    xmllint --noout --dtdvalid language.dtd haskell.xml literate-haskell.xml
