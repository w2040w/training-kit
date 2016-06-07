# GitHub Training Kit

This is the official courseware for the [GitHub Training Team](http://training.github.com). This repository provides open source materials and slides for teaching GitHub Classes under the [_CC BY 4.0_ license](http://creativecommons.org/licenses/by/4.0/).

We know that part of effectively sharing GitHub and Git with the world goes beyond our team's course offerings. We are pleased to provide you with this training kit that you can use to teach these same concepts at your company, for a user group, or at a conference.

## Download

We know that many of the users of this repository are just focused on getting the materials and teaching from them.  We've made that easy.

1. You can view and teach from the kit, hosted on GitHub, at https://services.github.com/kit/.
2. You can download the source files [here](https://github.com/github/training-kit/archive/master.zip).

#### Packaging for Viewing Behind Your Firewall

Sometimes you can't download the repository at work because of firewall rules, but you'd like to have a copy of the files that would be able to be served from a web server inside of these firewall rules. To do so, we need to use `script/package`.

1. Run `script/package` to create a release tarball. This will be in the format `release-XXXXXXX.tgz` for you to take wherever you want.
2. To test this looks okay, create some folders `mkdir -p test_site/kit`.
3. Untar the release, `tar -xzf release-XXXXXXX.tgz -C test_site/kit`.
4. Switch into the test_site directory, `cd test_site`.
5. View the site, `python -m SimpleHTTPServer`. _Note: Some servers are obviously more advance than others and can handle redirects, smart recognition of `.html` files, etc_

## Contribute

We’re eager to have your help in improving this kit. If you have an idea for a change, start by opening a new [Issue](https://github.com/github/training-kit/issues) so we can discuss and help guide your contribution to the right location. If you have corrections or kit contributions, we'd be glad to receive them via a [Pull Request](https://help.github.com/articles/using-pull-requests). For kit contributions, we ask you to share in our mindset of minimalism.

The slides align with the [Foundations](https://github.com/github/training-kit/tree/master/foundations/index.md), [Intermediate](https://github.com/github/training-kit/blob/master/intermediate/index.md), and [Advanced](https://github.com/github/training-kit/tree/master/advanced/index.md) classes delivered by the GitHub Training team.

The three class' slides reside at top-level directories:

- [`foundations/`](https://github.com/github/training-kit/tree/master/foundations)
- [`intermediate/`](https://github.com/github/training-kit/tree/master/intermediate)
- [`advanced/`](https://github.com/github/training-kit/tree/master/advanced)


## File Format

The class materials are written in [Markdown](http://whatismarkdown.com), a [lightweight markup language](http://en.wikipedia.org/wiki/Lightweight_markup_language) supported in the GitHub web application user interface. There is a syntax guide to the original [Markdown format](http://daringfireball.net/projects/markdown/syntax) and also [GitHub Flavored Markdown](http://github.github.com/github-flavored-markdown/).

The class material content possess two specialized uses of Markdown for slide-like rendering and formatting:

- Full-screen slides are preceded with a `---` and followed by `---`
- Step-by-step *lab* sections are wrapped with `{% capture lab %}` and `{% endcapture %}{% include lab %}`

 This repository is based on [Hydeslides](https://github.com/jordanmccullough/HydeSlides). That project offers additional information on the file and directory structure.

## Build

The build of this repository is fully automated through several shell scripts. To perform a build of the materials identical to that of our continuous integration server, from the top directory of this project, run `script/cibuild` and then inspect the output in the `_site` directory.

The `script/makerelease` script produces a zip bundle for offline use of these materials. Pre-built releases are available at https://github.com/github/training-kit/releases
