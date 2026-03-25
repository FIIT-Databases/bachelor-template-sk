# Šablóna bakalárskej práce — FIIT STU

LaTeX šablóna pre bakalársku prácu na Fakulte informatiky a informačných technológií, Slovenskej technickej univerzity v Bratislave.

## Štruktúra projektu

```
.
├── main.tex                 # Hlavný súbor dokumentu
├── constants.tex            # Konfigurácia (meno autora, názov práce, vedúci, ...)
├── packages.tex             # Importované LaTeX balíčky
├── references.bib           # Zoznam bibliografických záznamov
├── chapters/                # Kapitoly práce
│   ├── 01_Technical_Abstract.tex
│   ├── 02_Lay_Summary.tex
│   ├── 03_Introduction.tex
│   ├── 04_00_Problem_Statement_and_Solution.tex
│   ├── 04_01_Problem_statement.tex
│   ├── 04_02_Technical_Literature_overview.tex
│   ├── 04_03_Solution_Overview.tex
│   ├── 04_04_Risk_assesment.tex
│   ├── 04_05_Experimental_Reproducibility_and_Impact.tex
│   ├── 04_06_Sustainability_and_environmental_impact.tex
│   ├── 04_07_Employability.tex
│   ├── 04_08_Teamwork.tex
│   ├── 05_Conclusions.tex
│   ├── 06_Resume.tex
│   └── 07_Scientific_part.tex
├── templates/               # Šablóny pre úvodné strany
│   ├── title.tex            # Titulná strana
│   ├── assignment.tex       # Zadanie práce
│   ├── declaration.tex      # Čestné vyhlásenie
│   ├── acknowledgment.tex   # Poďakovanie
│   ├── annotation.tex       # Anotácia
│   ├── content.tex          # Obsah
│   └── header.tex           # Hlavička
└── attachments/             # Prílohy
    ├── appendix_B_Work_plan.tex
    ├── appendix_C_technical_documentation.tex
    └── attachment_D_digital_explain.tex
```

## Ako začať

### 1. Vyplňte údaje v `constants.tex`

Nahraďte zástupné hodnoty svojimi údajmi:

- `\FIITtitle` — názov práce v angličtine
- `\FIITtitleSlovak` — názov práce v slovenčine
- `\FIITauthor` — meno autora
- `\FIITsupervisor` — meno vedúceho práce
- `\FIITevidenceNumber` — evidenčné číslo
- `\FIITdate` — dátum odovzdania
- a ďalšie...

### 2. Píšte kapitoly

Obsah jednotlivých kapitol upravujte v priečinku `chapters/`. Každá kapitola je v samostatnom `.tex` súbore.

### 3. Spravujte referencie

Bibliografické záznamy pridávajte do súboru `references.bib` vo formáte BibTeX.

## Kompilácia

Na kompiláciu dokumentu je potrebný LaTeX distribúcia (napr. [TeX Live](https://www.tug.org/texlive/) alebo [MiKTeX](https://miktex.org/)).

```bash
# Kompilácia s biblatex (bibtex backend)
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

Alternatívne je možné použiť `latexmk`:

```bash
latexmk -pdf main.tex
```

Odporúčame tiež použiť editor s integrovanou podporou LaTeX, napr. [Overleaf](https://www.overleaf.com/), [TeXstudio](https://www.texstudio.org/) alebo VS Code s rozšírením [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop).

## Požiadavky

- LaTeX distribúcia s podporou `biblatex`, `bibtex` a slovenských znakových sád
- Balíčky uvedené v `packages.tex` (väčšina je súčasťou štandardnej TeX Live inštalácie)