<!-- Do not edit this file.  It is generated automatically from
README.template and MANUAL.txt via the command:
pandoc --lua-filter tools/update-readme.lua README.template -o README.md
-->

# Pandoc

[![github
release](https://img.shields.io/github/release/jgm/pandoc.svg?label=current+release)](https://github.com/jgm/pandoc/releases)
[![hackage
release](https://img.shields.io/hackage/v/pandoc.svg?label=hackage)](http://hackage.haskell.org/package/pandoc)
[![homebrew](https://img.shields.io/homebrew/v/pandoc.svg)](http://brewformulas.org/Pandoc)
[![stackage LTS
package](http://stackage.org/package/pandoc/badge/lts)](http://stackage.org/lts/package/pandoc)
[![CI
tests](https://github.com/jgm/pandoc/workflows/CI%20tests/badge.svg)](https://github.com/jgm/pandoc/actions)
[![license](https://img.shields.io/badge/license-GPLv2+-lightgray.svg)](https://www.gnu.org/licenses/gpl.html)
[![pandoc-discuss on google
groups](https://img.shields.io/badge/pandoc-discuss-red.svg?style=social)](https://groups.google.com/forum/#!forum/pandoc-discuss)

## The universal markup converter

Pandoc is a [Haskell](http://haskell.org) library for converting from
one markup format to another, and a command-line tool that uses this
library. It can convert *from*

<div id="input-formats">

-   `bibtex` ([BibTeX](https://ctan.org/pkg/bibtex) bibliography)
-   `biblatex` ([BibLaTeX](https://ctan.org/pkg/biblatex) bibliography)
-   `commonmark` ([CommonMark](https://commonmark.org) Markdown)
-   `commonmark_x` ([CommonMark](https://commonmark.org) Markdown with
    extensions)
-   `creole` ([Creole 1.0](http://www.wikicreole.org/wiki/Creole1.0))
-   `csljson` ([CSL
    JSON](https://citeproc-js.readthedocs.io/en/latest/csl-json/markup.html)
    bibliography)
-   `csv` ([CSV](https://tools.ietf.org/html/rfc4180) table)
-   `docbook` ([DocBook](https://docbook.org))
-   `docx` ([Word docx](https://en.wikipedia.org/wiki/Office_Open_XML))
-   `dokuwiki` ([DokuWiki markup](https://www.dokuwiki.org/dokuwiki))
-   `epub` ([EPUB](http://idpf.org/epub))
-   `fb2`
    ([FictionBook2](http://www.fictionbook.org/index.php/Eng:XML_Schema_Fictionbook_2.1)
    e-book)
-   `gfm` ([GitHub-Flavored
    Markdown](https://help.github.com/articles/github-flavored-markdown/)),
    or the deprecated and less accurate `markdown_github`; use
    [`markdown_github`](https://pandoc.org/MANUAL.html#markdown-variants)
    only if you need extensions not supported in
    [`gfm`](https://pandoc.org/MANUAL.html#markdown-variants).
-   `haddock` ([Haddock
    markup](https://www.haskell.org/haddock/doc/html/ch03s08.html))
-   `html` ([HTML](https://www.w3.org/html/))
-   `ipynb` ([Jupyter
    notebook](https://nbformat.readthedocs.io/en/latest/))
-   `jats` ([JATS](https://jats.nlm.nih.gov) XML)
-   `jira`
    ([Jira](https://jira.atlassian.com/secure/WikiRendererHelpAction.jspa?section=all)/Confluence
    wiki markup)
-   `json` (JSON version of native AST)
-   `latex` ([LaTeX](https://www.latex-project.org/))
-   `markdown` ([Pandoc’s
    Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown))
-   `markdown_mmd`
    ([MultiMarkdown](https://fletcherpenney.net/multimarkdown/))
-   `markdown_phpextra` ([PHP Markdown
    Extra](https://michelf.ca/projects/php-markdown/extra/))
-   `markdown_strict` (original unextended
    [Markdown](https://daringfireball.net/projects/markdown/))
-   `mediawiki` ([MediaWiki
    markup](https://www.mediawiki.org/wiki/Help:Formatting))
-   `man` ([roff man](https://man.cx/groff_man(7)))
-   `muse` ([Muse](https://amusewiki.org/library/manual))
-   `native` (native Haskell)
-   `odt` ([ODT](https://en.wikipedia.org/wiki/OpenDocument))
-   `opml` ([OPML](http://dev.opml.org/spec2.html))
-   `org` ([Emacs Org mode](https://orgmode.org))
-   `rst`
    ([reStructuredText](https://docutils.sourceforge.io/docs/ref/rst/introduction.html))
-   `t2t` ([txt2tags](https://txt2tags.org))
-   `textile` ([Textile](https://www.promptworks.com/textile))
-   `tikiwiki` ([TikiWiki
    markup](https://doc.tiki.org/Wiki-Syntax-Text#The_Markup_Language_Wiki-Syntax))
-   `twiki` ([TWiki
    markup](https://twiki.org/cgi-bin/view/TWiki/TextFormattingRules))
-   `vimwiki` ([Vimwiki](https://vimwiki.github.io))

</div>

It can convert *to*

<div id="output-formats">

-   `asciidoc` ([AsciiDoc](https://www.methods.co.nz/asciidoc/)) or
    `asciidoctor` ([AsciiDoctor](https://asciidoctor.org/))
-   `beamer` ([LaTeX beamer](https://ctan.org/pkg/beamer) slide show)
-   `commonmark` ([CommonMark](https://commonmark.org) Markdown)
-   `commonmark_x` ([CommonMark](https://commonmark.org) Markdown with
    extensions)
-   `context` ([ConTeXt](https://www.contextgarden.net/))
-   `csljson` ([CSL
    JSON](https://citeproc-js.readthedocs.io/en/latest/csl-json/markup.html)
    bibliography)
-   `docbook` or `docbook4` ([DocBook](https://docbook.org) 4)
-   `docbook5` (DocBook 5)
-   `docx` ([Word docx](https://en.wikipedia.org/wiki/Office_Open_XML))
-   `dokuwiki` ([DokuWiki markup](https://www.dokuwiki.org/dokuwiki))
-   `epub` or `epub3` ([EPUB](http://idpf.org/epub) v3 book)
-   `epub2` (EPUB v2)
-   `fb2`
    ([FictionBook2](http://www.fictionbook.org/index.php/Eng:XML_Schema_Fictionbook_2.1)
    e-book)
-   `gfm` ([GitHub-Flavored
    Markdown](https://help.github.com/articles/github-flavored-markdown/)),
    or the deprecated and less accurate `markdown_github`; use
    [`markdown_github`](https://pandoc.org/MANUAL.html#markdown-variants)
    only if you need extensions not supported in
    [`gfm`](https://pandoc.org/MANUAL.html#markdown-variants).
-   `haddock` ([Haddock
    markup](https://www.haskell.org/haddock/doc/html/ch03s08.html))
-   `html` or `html5` ([HTML](https://www.w3.org/html/),
    i.e. [HTML5](https://html.spec.whatwg.org/)/XHTML [polyglot
    markup](https://www.w3.org/TR/html-polyglot/))
-   `html4` ([XHTML](https://www.w3.org/TR/xhtml1/) 1.0 Transitional)
-   `icml` ([InDesign
    ICML](https://wwwimages.adobe.com/www.adobe.com/content/dam/acom/en/devnet/indesign/sdk/cs6/idml/idml-cookbook.pdf))
-   `ipynb` ([Jupyter
    notebook](https://nbformat.readthedocs.io/en/latest/))
-   `jats_archiving` ([JATS](https://jats.nlm.nih.gov) XML, Archiving
    and Interchange Tag Set)
-   `jats_articleauthoring` ([JATS](https://jats.nlm.nih.gov) XML,
    Article Authoring Tag Set)
-   `jats_publishing` ([JATS](https://jats.nlm.nih.gov) XML, Journal
    Publishing Tag Set)
-   `jats` (alias for `jats_archiving`)
-   `jira`
    ([Jira](https://jira.atlassian.com/secure/WikiRendererHelpAction.jspa?section=all)/Confluence
    wiki markup)
-   `json` (JSON version of native AST)
-   `latex` ([LaTeX](https://www.latex-project.org/))
-   `man` ([roff man](https://man.cx/groff_man(7)))
-   `markdown` ([Pandoc’s
    Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown))
-   `markdown_mmd`
    ([MultiMarkdown](https://fletcherpenney.net/multimarkdown/))
-   `markdown_phpextra` ([PHP Markdown
    Extra](https://michelf.ca/projects/php-markdown/extra/))
-   `markdown_strict` (original unextended
    [Markdown](https://daringfireball.net/projects/markdown/))
-   `mediawiki` ([MediaWiki
    markup](https://www.mediawiki.org/wiki/Help:Formatting))
-   `ms` ([roff ms](https://man.cx/groff_ms(7)))
-   `muse` ([Muse](https://amusewiki.org/library/manual)),
-   `native` (native Haskell),
-   `odt` ([OpenOffice text
    document](https://en.wikipedia.org/wiki/OpenDocument))
-   `opml` ([OPML](http://dev.opml.org/spec2.html))
-   `opendocument` ([OpenDocument](http://opendocument.xml.org))
-   `org` ([Emacs Org mode](https://orgmode.org))
-   `pdf` ([PDF](https://www.adobe.com/pdf/))
-   `plain` (plain text),
-   `pptx`
    ([PowerPoint](https://en.wikipedia.org/wiki/Microsoft_PowerPoint)
    slide show)
-   `rst`
    ([reStructuredText](https://docutils.sourceforge.io/docs/ref/rst/introduction.html))
-   `rtf` ([Rich Text
    Format](https://en.wikipedia.org/wiki/Rich_Text_Format))
-   `texinfo` ([GNU Texinfo](https://www.gnu.org/software/texinfo/))
-   `textile` ([Textile](https://www.promptworks.com/textile))
-   `slideous` ([Slideous](https://goessner.net/articles/slideous/) HTML
    and JavaScript slide show)
-   `slidy` ([Slidy](https://www.w3.org/Talks/Tools/Slidy2/) HTML and
    JavaScript slide show)
-   `dzslides` ([DZSlides](http://paulrouget.com/dzslides/) HTML5 +
    JavaScript slide show),
-   `revealjs` ([reveal.js](https://revealjs.com/) HTML5 + JavaScript
    slide show)
-   `s5` ([S5](https://meyerweb.com/eric/tools/s5/) HTML and JavaScript
    slide show)
-   `tei` ([TEI Simple](https://github.com/TEIC/TEI-Simple))
-   `xwiki` ([XWiki
    markup](https://www.xwiki.org/xwiki/bin/view/Documentation/UserGuide/Features/XWikiSyntax/))
-   `zimwiki` ([ZimWiki
    markup](https://zim-wiki.org/manual/Help/Wiki_Syntax.html))
-   the path of a custom Lua writer, see [Custom
    writers](https://pandoc.org/MANUAL.html#custom-writers) below

</div>

Pandoc can also produce PDF output via LaTeX, Groff ms, or HTML.

Pandoc’s enhanced version of Markdown includes syntax for tables,
definition lists, metadata blocks, footnotes, citations, math, and much
more. See the User’s Manual below under [Pandoc’s
Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown).

Pandoc has a modular design: it consists of a set of readers, which
parse text in a given format and produce a native representation of the
document (an *abstract syntax tree* or AST), and a set of writers, which
convert this native representation into a target format. Thus, adding an
input or output format requires only adding a reader or writer. Users
can also run custom pandoc filters to modify the intermediate AST (see
the documentation for [filters](https://pandoc.org/filters.html) and
[Lua filters](https://pandoc.org/lua-filters.html)).

Because pandoc’s intermediate representation of a document is less
expressive than many of the formats it converts between, one should not
expect perfect conversions between every format and every other. Pandoc
attempts to preserve the structural elements of a document, but not
formatting details such as margin size. And some document elements, such
as complex tables, may not fit into pandoc’s simple document model.
While conversions from pandoc’s Markdown to all formats aspire to be
perfect, conversions from formats more expressive than pandoc’s Markdown
can be expected to be lossy.

## Installing

Here’s [how to install pandoc](INSTALL.md).

## Documentation

Pandoc’s website contains a full [User’s
Guide](https://pandoc.org/MANUAL.html). It is also available
[here](MANUAL.txt) as pandoc-flavored Markdown. The website also
contains some [examples of the use of
pandoc](https://pandoc.org/demos.html) and a limited [online
demo](https://pandoc.org/try).

## Contributing

Pull requests, bug reports, and feature requests are welcome. Please
make sure to read [the contributor guidelines](CONTRIBUTING.md) before
opening a new issue.

## License

© 2006-2020 John MacFarlane (jgm@berkeley.edu). Released under the
[GPL](http://www.gnu.org/copyleft/gpl.html "GNU General Public License"),
version 2 or greater. This software carries no warranty of any kind.
(See COPYRIGHT for full copyright and warranty notices.)

## Running with Docker

The official Docker images for pandoc can be found at
<https://github.com/pandoc/dockerfiles> and at
[dockerhub](https://hub.docker.com/).

The [pandoc/core](https://hub.docker.com/r/pandoc/core)
image contains `pandoc`.

The [pandoc/latex](https://hub.docker.com/r/pandoc/latex)
image also contains the minimal LaTeX installation needed
to produce PDFs using pandoc.

To run pandoc using Docker, converting `README.md` to `README.pdf`:

    docker run --rm --volume "`pwd`:/data" --user `id -u`:`id -g` mjschmidt/pandoc README.md -o README.pdf

