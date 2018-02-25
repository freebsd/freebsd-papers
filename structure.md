Definitions:
{{name}} is the @freebsd.org username, or surname in case of someone from outside the project
{{conference}} is whatever conference the paper was at
{{blank}} is to be used when a year does not contain a lot of entries 
{{type}} is the type of file, ie: paper or slides

File and directory structure is as follows:
static/_assets/ # Contains old asset files [FIXME]
contents/{{year}}/{{conference|blank}}/{{name}}-{{subject}}.md
contents/{{year}}/{{conference|blank}}/{{name}}-{{subject}}.files/{{name}}-{{subject}}-{{type}}.pdf
README.md # Self-explanatory
structure.md # You are here

Any files or directory not defined by this file should be assumed to belong to the site engine which, at the time of writing, is Hugo - and should therefore ideally not be touched.
