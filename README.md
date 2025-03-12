# badges
A place to store icons and badges generated by YML actions and Docker actions

In Github, on a main project page, if you have a README.md that links to an image,
it will be rendered when the main project page displays the README.md.  This
is how build badges work.

But I wanted my own, more complicated, build badges. To make that happen
there are two projects
- verbose-waffle: it is some shell scripts that make badges
- this project (badges): which is just storage for badges

The basic workflow is this
1. A YML file makes an SVG using a verbose-waffle script
2. The YML file commits the SVG to the `badges` project under `<project name>/<branch name>`
3. The README.md includes the SVG file
    * As an explicit path ![Build Status](https://raw.githubusercontent.com/spk121/badges/master/<project name>/<branch name>build.svg?sanitize=true)
    * Or when the badges project is a subproject ![Alt text](./badges/<project name>/<branch name>/example.svg)
  
