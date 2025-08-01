# super-tool-scripts

A cople super-tool scripts I wrote and that I found useful for my workflow.

Super-Tool is an Isotammi addons for [Gramps](https://gramps-project.org/).
See:
* https://www.gramps-project.org/wiki/index.php/Addon:Isotammi_addons#SuperTool
* https://github.com/Taapeli/isotammi-addons/blob/master/source/SuperTool/README.md

## Link scripts

A lot of those scripts have the purpose to make links shorter as Geneanet has a
bug in its gedcom import feature as it add a space in the link (thus breaking
it) if the link happens to be on multiple lines in the gedcom file.
Eg:
1 WWW https://gw.geneanet.org/alsen?lang=fr&pz=josephine&nz=seneterre&p=michel
2 CONC &n=meylheuc

would result in the following link in genenanet:
"https://gw.geneanet.org/alsen?lang=fr&pz=josephine&nz=seneterre&p=michel &n=meylheuc"

### remove-lang=fr.script

This script removes the lang=fr parameter from links, thus making them shorter.

### remove-pz-nz.script

This script removes the pz=<fist_name> & nz=<given_name> parameters from links,
thus making them shorter.

### remove-type=.script

This script removes the type=fche parameter from links, thus making them shorter.

### set-link-private.script

This script was a one shot script that I used once to make all links from a
particular Geneanet tree be private as the whole tree was removed and thus all
those links were invalid.

## Name normalization scripts

Those scripts are about normalize names regarding "Le" prefix which is used eg
in Britanny.
They are usefull after importing some Geneanet subtrees in my own tree.

### split-Le+Roux-in-Le-Roux.script

It splits names such as "Le Roux" into "Le" prefix and "Roux" name.
One could fork it in order to do same for gentlement & ladies ("De …").

### split-Roux-Le-in-Le-Roux.script

It splits names such as "Roux (Le)" into "Le" prefix and "Roux" name.
One could fork it in order to do same for gentlement & ladies ("De …").


