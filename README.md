godepgrah
=========

godepgraph is a program for generating a dependency graph of Go packages.

Install
-------

    go get github.com/kisielk/godepgraph

Use
---

For basic usage, just give the package path of interest as the first
argument:

    godepgraph github.com/kisielk/godepgraph

The output is a graph in [Graphviz][graphviz] dot format. If you have the
graphviz tools installed you can render it by piping the output to dot:

    godepgraph github.com/kisielk/godepgraph | dot -Tpng -o godepgraph.png

By default godepgraph will display packages in the standard library in the
graph, though it will not delve in to their dependencies.

If you want to ignore standard library packages entirely, use the -s flag:

    godepgraph -s github.com/kisielk/godepgraph

[graphviz]: http://graphviz.org