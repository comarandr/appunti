# LATEX BASE

## Creare un documento

Per creare un documento, basta scrivere:

```tex
\documentclass{article} %tipo di documento
\usepackage{nome_pacchetto} %per i pacchetti
\title{titolo}
\author{autore}
\date{data}
\begin{document} % inizio del documento
\maketitle % per mostrare titolo, autore, data
\tableofcontents % per mostrare la tabella dei contenuti
...
\newpage % per cambiare pagina
...
\end{document}
```

La sintassi minima è la seguente

```tex
\documentclass{article}
\begin{document}
...
\end{document}
```

## Suddividere un testo

La suddivisione viene enumerata automaticamente

- **Parte**: `\part{part_name}`
- **Sezione**: `\section{section_name}`
- **Sottosezione**: `\subsection{subsection_name}`
- **Paragrafo**: `\paragraph{paragraph_name}`
- **Sottoparagrafo**: `\subparagraph{subparagraph_name}`
- **nuova pagina**: `\newpage`

## Comandi di scrittura

- **non compilazione**: `\verbatim{testo non compilato}` per esempio posso usarlo per scrivere `\verbatim{\part \\}` &rarr; `\part \\`
- **tabulazione**:

```tex
\begin{tabbing} 
col1 \ col2 \ col3 
\end{tabbing}
``` 