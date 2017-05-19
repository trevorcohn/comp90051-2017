# comp90051-2017
Statistical Machine Learning subject materials at the University of Melbourne. All content Copyright 2017, The University of Melbourne.

To serve pages using docker, use the following command:

docker run --rm --label=jekyll --volume=$(pwd):/srv/jekyll   -it -p 127.0.0.1:4000:4000 jekyll/jekyll:pages jekyll serve
