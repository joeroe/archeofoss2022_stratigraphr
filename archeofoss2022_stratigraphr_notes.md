* Introduction
* Aside: I'll be talking about these two packages in development
* Handling stratigraphic data in R is easy!
  * If you can export your database to plain text, let's go.
  * [stratigraphr] More complex formats, e.g. LST
* Graph representation
  * A graph is by far the most common formalism; more specifically, per Dye & Buck, a DAG
  * R has a *lot* of functionality for graph data, analysis, and visualisation
  * igraph
* Examples with igraph
  * [stratigraphr] produce harris matrix visualisation
  * [stratigraphr] check validity
* So far so good, but...
  * DSLs in R (like igraph) are all well and good when you're working within that framework (e.g. network analysis)
  * But peek behind the curtain at the structure and... argh
  * How on earth do we start mixing this with other types of data, doing other types of analysis?
  * Which of course is almost always what we want to do with stratigraphic data!
* Enter the tidyverse
  * I think the best attempt to solve this general problem
  * Fundamentally, a set of conventions the make it easier to work with multiple DSLs in R
  * This is why, for stratigraphr, we use tidygraph + ggraph
  * And my general direction with it recently has been to try and develop tidy DSLs for archaeology
* Archaeology in the tidyverse?
  * stratigraphr's sister package c14 provides tidy representation of radiocarbon data
  * We can combine the two (and some friends!) to do, for example, Bayesian calibration:
    * Tidy table -> CQL -> OxCal
  * (Bottleneck here: OxCal! Can we cut it out? Can anyone help me??)
