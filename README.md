# CFCD Class Site

This repo contains a [Hugo](https://gohugo.io/) project.
It expects the content to be pushed into its `content` folder from the `developer-training-course` learning path using the `hugo-parser` executable.

## Preparation

1. Install hugo locally
2. Install the theme into this project. Its a git submodule

```sh
git submodule update --init
```

3. Clone the [developer-training-course](https://github.com/cloudfoundry/developer-training-course.git)
4. `Go get` the content parser

```sh
go get github.com/EngineerBetter/hugo-parser
```

If you want to view slides also:

5. Clone the [reveal.js repo](https://github.com/resilientscale/reveal.js.git)

## Running locally

1. start the hugo server

```sh
cd developer-training-class-site
hugo serve -D
```

2. Push in the learning path content from the `developer-training-course` repo using:

```sh
hugo-parser developer-training-course/learning-path/exercise-mappings.yml developer-training-course developer-training-class-site/content
```

*NB. You would need to run this command each time you change a file in developer-training-course*

If you want to view slides also:

3. Run the slides docker container as described on the [reveal.js readme](https://github.com/resilientscale/reveal.js/blob/master/cff-readme.md)
