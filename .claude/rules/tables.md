# Tables: No Embedded Titles

- **Never embed titles in generated `.tex` table files** — no `\caption{}` inside the output from R/Stata
- **Table information goes in two places:**
  1. **File name** — descriptive, e.g., `table2_enrollment_ascm.tex`
  2. **LaTeX `\caption{}`** — added in the paper where the table is `\input{}`'d, not in the generated file
- **Generated `.tex` files contain only the tabular content** — the wrapping `\begin{table}`, `\caption`, and `\label` live in the paper
- **Use `threeparttable`** — wrap tables with `\begin{threeparttable}` for proper alignment of notes via `\begin{tablenotes}`
- **Use `booktabs`** — `\toprule`, `\midrule`, `\bottomrule` only. No vertical lines.
- **Notes live in the paper, not in R output** — `\begin{tablenotes}` content (sample descriptions, variable definitions, significance stars) is written in the paper alongside `\caption` and `\label`
