Definitions:
<name> is the @freebsd.org username, or surname in case of someone from outside the project
<convention> is whatever convention the paper was at
<other> is if it wasn't presented at a convention, but the paper is from a year where other conventions have taken place
<blank> is to be used when a year does not contain a lot of entries 
<type> is the type of file, ie: paper or slides

File and directory structure is as follows:
static/_assets/ # Contains old asset files [FIXME]
contents/<year>/<convention|other|blank>/<name>_<subject>.md
contents/<year>/<convention|other|blank>/<name>_<subject>.files/<name>_<subject>_<type>.pdf
README.md # Self-explanatory
structure.md # You are here. If in doubt, check where your towel is.

Any files or directory not defined by this file should be assumed to belong to the site engine which, at the time of writing, is Hugo - and should therefore ideally 
nt be touched.
