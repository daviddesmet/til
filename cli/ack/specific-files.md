# Search only in specific files

```bash
$ ack --type-set=markdown=.md,.mkd,.markdown tofind

cli/ack/ignore-case.md
4:$ ack -t tofind
```

### List supported file types

```bash
$ ack --help=types

    ...
    --[no]asm          .asm .s
    --[no]asp          .asp
    --[no]aspx         .master .ascx .asmx .aspx .svc
    --[no]batch        .bat .cmd
    --[no]cc           .c .h .xs
    --[no]cfmx         .cfc .cfm .cfml
    --[no]clojure      .clj .cljs .edn .cljc
    --[no]cmake        CMakeLists.txt; .cmake
    --[no]coffeescript .coffee
    --[no]cpp          .cpp .cc .cxx .m .hpp .hh .h .hxx
    --[no]csharp       .cs
    --[no]css          .css
    --[no]dart         .dart
    --[no]delphi       .pas .int .dfm .nfm .dof .dpk .dproj .groupproj .bdsgroup .bdsproj
    --[no]elisp        .el
    --[no]elixir       .ex .exs
    --[no]erlang       .erl .hrl
    --[no]fortran      .f .f77 .f90 .f95 .f03 .for .ftn .fpp
    --[no]go           .go
    --[no]groovy       .groovy .gtmpl .gpp .grunit .gradle
    --[no]gsp          .gsp
    --[no]haskell      .hs .lhs
    --[no]hh           .h
    --[no]hpp          .hpp .hh .h .hxx
    --[no]html         .htm .html .xhtml
    --[no]jade         .jade
    --[no]java         .java .properties
    --[no]js           .js
    --[no]json         .json
    --[no]jsp          .jsp .jspx .jspf .jhtm .jhtml
    --[no]kotlin       .kt .kts
    --[no]less         .less
    --[no]lisp         .lisp .lsp
    --[no]lua          .lua; first line matches /^#!.*\blua(jit)?/
    --[no]make         .mk; .mak; makefile; Makefile; Makefile.Debug; Makefile.Release
    --[no]matlab       .m
    --[no]objc         .m .h
    --[no]objcpp       .mm .h
    --[no]ocaml        .ml .mli .mll .mly
    --[no]parrot       .pir .pasm .pmc .ops .pod .pg .tg
    --[no]perl         .pl .pm .pod .t .psgi; first line matches /^#!.*\bperl/
    --[no]perltest     .t
    --[no]php          .php .phpt .php3 .php4 .php5 .phtml; first line matches /^#!.*\bphp/
    --[no]plone        .pt .cpt .metadata .cpy .py
    --[no]python       .py; first line matches /^#!.*\bpython/
    --[no]rake         Rakefile
    --[no]rr           .R
    --[no]rst          .rst
    --[no]ruby         .rb .rhtml .rjs .rxml .erb .rake .spec; Rakefile; first line matches /^#!.*\bruby/
    --[no]rust         .rs
    --[no]sass         .sass .scss
    --[no]scala        .scala
    --[no]scheme       .scm .ss
    --[no]shell        .sh .bash .csh .tcsh .ksh .zsh .fish; first line matches /^#!.*\b(?:ba|t?c|k|z|fi)?sh\b/
    --[no]smalltalk    .st
    --[no]smarty       .tpl
    --[no]sql          .sql .ctl
    --[no]stylus       .styl
    --[no]swift        .swift; first line matches /^#!.*\bswift/
    --[no]tcl          .tcl .itcl .itk
    --[no]tex          .tex .cls .sty
    --[no]ts           .ts .tsx
    --[no]tt           .tt .tt2 .ttml
    --[no]vb           .bas .cls .frm .ctl .vb .resx
    --[no]verilog      .v .vh .sv
    --[no]vhdl         .vhd .vhdl
    --[no]vim          .vim
    --[no]xml          .xml .dtd .xsd .xsl .xslt .ent .wsdl; first line matches /<[?]xml/
    --[no]yaml         .yaml .yml
    ...

$ ack --csharp ToFind
```
