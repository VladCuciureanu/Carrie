# Carrie

## Getting Started

The repository includes the exact Inter font files used by the CV, so the build does not depend on fonts installed on the host. With a TeX distribution installed, run:

```sh
lualatex resume.tex
```

This will generate the CV as `resume.pdf`.

Alternatively, you can compile it using Docker:

```sh
docker run --rm -v "$(pwd):/work" -w /work texlive/texlive latexmk -lualatex resume.tex
```

## License

This source code is distributed under the terms of the MIT License. Free for both commercial and research use.
