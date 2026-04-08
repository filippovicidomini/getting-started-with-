# Getting Started Guides (LaTeX)

Raccolta di guide pratiche scritte in LaTeX, con uno stile grafico uniforme e versione PDF pronta da consultare.

## Contenuto

| Guida | Sorgente | PDF |
| --- | --- | --- |
| tmux | [tmux/tmux-guide.tex](tmux/tmux-guide.tex) | [tmux/tmux-guide.pdf](tmux/tmux-guide.pdf) |
| GitHub | [github/github-guide.tex](github/github-guide.tex) | [github/github-guide.pdf](github/github-guide.pdf) |

## Obiettivo della repository

- Tenere guide tecniche concise e leggibili.
- Mantenere un template LaTeX coerente tra i documenti.
- Avere sempre sia la versione `.tex` sia la versione `.pdf`.

## Struttura

```text
.
├── github/
│   ├── github-guide.tex
│   └── github-guide.pdf
└── tmux/
    ├── tmux-guide.tex
    └── tmux-guide.pdf
```

## Requisiti

- Distribuzione LaTeX installata (MacTeX/TeX Live).
- `pdflatex` disponibile nel PATH.

Verifica rapida:

```bash
pdflatex --version
```

## Come compilare le guide

Compila una guida (esempio GitHub):

```bash
cd github
pdflatex -interaction=nonstopmode -halt-on-error github-guide.tex
pdflatex -interaction=nonstopmode -halt-on-error github-guide.tex
```

Compila la guida tmux:

```bash
cd tmux
pdflatex -interaction=nonstopmode -halt-on-error tmux-guide.tex
pdflatex -interaction=nonstopmode -halt-on-error tmux-guide.tex
```

Pulizia file temporanei LaTeX (opzionale):

```bash
rm -f *.aux *.log *.out *.toc
```

## Come aggiungere una nuova guida

1. Crea una nuova cartella (es. `docker/`).
2. Copia la struttura di una guida esistente come base.
3. Aggiorna titolo, contenuti e quick reference.
4. Compila il PDF e verifica l'impaginazione.
5. Aggiungi entrambi i file (`.tex` + `.pdf`) al commit.

## Convenzioni consigliate

- Nome file: `<tema>-guide.tex` e `<tema>-guide.pdf`.
- Stile: usare gli stessi colori, box e gerarchia dei titoli gia presenti.
- Linguaggio: italiano tecnico, diretto e orientato all'uso pratico.

## Licenza

Se vuoi, puoi aggiungere qui una licenza esplicita (es. MIT o CC BY 4.0) in base a come intendi distribuire i contenuti.
