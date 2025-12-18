# 📜 Curriculum Vitae

Welcome to my resume's LaTeX source code repository. This project is built using the stylish [Awesome CV](https://github.com/posquit0/Awesome-CV) template, created by [Byungjin Park](https://github.com/posquit0).

## Getting Started

To compile this CV, ensure you have a TeX distribution installed on your system. Once installed, simply run:

```sh
xelatex resume.tex
```

This will generate the CV as `resume.pdf`.

Alternatively, you can compile it using the provided Dockerfile:

```sh
docker build --tag 'vlad.cuciureanu/xelatex' .
docker run --rm -w /data -v .:/data vlad.cuciureanu/xelatex xelatex resume.tex
```

## License

This source code is distributed under the terms of the MIT License. Free for both commercial and research use.
