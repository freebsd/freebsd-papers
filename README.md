# freebsd-papers
The base for Papers.FreeBSD.org, a collection of conference talks, papers, slides, and videos from conferences related to FreeBSD


To add a paper or talk:
* Create `lastname-title.md` (based on `template.md`) in the corresponding year directory
* If there are many talks from the same conference, create a subdirectory
* create a `lastname-title.files/` directory beside the `.md` file to store the attachments

The site is built with [Hugo](https://gohugo.io/).

To install the requirement for building the site:
```
# pkg install gohugo
$ git submodule init
$ git submodule update
```

To build the site locally:
```
$ hugo
```

To check it locally:
```
$ hugo server
```

To check it locally when `hugo server` arbitrarily refuses to serve files with
long names:
```
$ (cd public_html && python -m SimpleHTTPServer)
