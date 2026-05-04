# Carrie

## Getting Started

To compile this CV, ensure you have a TeX distribution installed on your system. Once installed, simply run:

```sh
xelatex resume.tex
```

This will generate the CV as `resume.pdf`.

Alternatively, you can compile it using Docker:

```sh
docker run --rm -v "$(pwd):/work" -w /work texlive/texlive latexmk -xelatex resume.tex
```

## License

This source code is distributed under the terms of the MIT License. Free for both commercial and research use.
