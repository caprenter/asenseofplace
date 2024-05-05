# asenseofplace

This is a jekyll based website for [A Sense Of Place](https://asenseofplace.org.uk/) deployed via GitHub pages.

## Contributing
Clone this repository

Create an issue, then create a development branch that uses the issue number in the branch name. E.g. 23-add-new-feature

Make a pull request.


### Gallery

A gallery can be added by including gallery.html and specifying a directory of images e.g.

  {% include gallery.html directory="keighley" %}

You also need to have a subdirectory of the same name within the thumbnails directory.

    Copy the main image directory to thumbnails

    Run this to thumbnail them:
    find . \( -name '*.jpg' -or -name '*.JPG' \) -print0 |  while read -d $'\0' file ; do convert -define jpeg:size=400x400  "$file" -thumbnail 400x400^ -gravity center -extent 400x400  ../thumbnails/"$file" ; done

The gallery uses a jquery or something similar lightbox thingy as well.