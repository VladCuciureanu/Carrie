# Carrie

Vlad Cuciureanu's CV, typeset in LaTeX and set in Inter.

The output is a US Letter, two-column CV: a name and contact header, then experience, personal projects and open source contributions on the left, and skills, references, education and interests on the right.

## Requirements

- A TeX distribution with LuaLaTeX (TeX Live or MiKTeX).
- The packages `fontspec`, `geometry`, `xcolor`, `enumitem`, `hyperref`, `paracol` and `microtype`. A full TeX Live install has all of them.

`resume.tex` uses `fontspec`, so pdfLaTeX will not work, and it declares `% !TEX program = lualatex`. The Inter fonts are bundled in `fonts/inter/`, so nothing needs to be installed system-wide.

## Build

From the repository root (the font path is relative to it):

```sh
lualatex resume.tex
```

This writes `resume.pdf` next to `resume.tex`.

Or with Docker, without a local TeX install:

```sh
docker run --rm -v "$(pwd):/work" -w /work texlive/texlive latexmk -lualatex -output-directory=dist resume.tex
```

This writes `dist/resume.pdf`. `dist/` is git-ignored.

## Layout

`resume.tex` holds the page geometry, font setup, colours, spacing and the layout macros (`\jobentry`, `\projectentry`, `\rsidebarsection` and so on). It pulls in the content from `sections/`:

| File | Content | Position |
| --- | --- | --- |
| `header.tex` | Name, tagline and contact links | Top |
| `experience.tex` | Relevant Experience | Left column |
| `projects.tex` | Personal Projects | Left column |
| `contributions.tex` | Open Source Contributions | Left column |
| `skills.tex` | Skills | Right column |
| `references.tex` | References | Right column |
| `education.tex` | Education | Right column |
| `interests.tex` | Philosophy, Currently Exploring, Spoken Languages | Right column |

To change the order of sections, edit the `\input` lines inside the `paracol` environment in `resume.tex`.

The MIT license covers the template and code, the CV content itself is personal, and the bundled Inter fonts keep their own license (`fonts/inter/LICENSE.txt`).

## License

MIT. See [LICENSE](LICENSE).
