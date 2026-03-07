# Figures: No Embedded Titles

- **Never add titles or subtitles inside ggplot** — use `labs(title = NULL, subtitle = NULL)`
- **Figure information goes in two places:**
  1. **File name** — descriptive, e.g., `fig1_hispanic_enrollment_ascm.pdf`
  2. **LaTeX `\caption{}`** — the authoritative title, numbered and editable without re-running R
- **Panel labels are the exception** — "Panel A: Employment" inside multi-panel figures (via `patchwork`, `cowplot`, etc.) is fine since they identify sub-panels, not the whole figure
- **Axis labels must be publication-quality** — "Employment Rate" not "emp_rate". Clean labels stay in the figure; titles and context go in the caption
- **Use serif fonts** — figures should match the paper's body text. In ggplot, set `theme(text = element_text(family = "serif"))` or use `theme_minimal(base_family = "serif")`
- **Show all years on the x-axis** when the panel spans ~20 years or fewer — use `scale_x_continuous(breaks = min_year:max_year)`. Only thin out labels when they overlap (roughly >20 ticks)
