# Statistical network analysis of an Italian crime network

Who works with whom, and why? This project analyses a directed network of 67
members of an Italian criminal organisation operating in the US, with
**exponential random graph models (ERGMs)**, the standard statistical tool for
asking which social mechanisms explain the ties in a network.

## Questions asked

1. **What does the network look like?** Density (0.0165, i.e. very sparse),
   isolates, in- and out-degree, geodesic distances, betweenness,
   eigenvector centrality, clustering and reciprocity.
2. **Which mechanisms explain the ties?** An edges-only baseline ERGM
   (log-odds of a tie: -4.087, which reproduces the density) is compared with
   a model adding reciprocity, reciprocity within the same role, and
   homophily by nationality.
3. **Does the model fit?** Goodness-of-fit diagnostics compare simulated
   networks with the observed one.

## Methods

R with `statnet` / `ergm`: descriptive statistics, several network layouts
(circle, Fruchterman-Reingold, Kamada-Kawai) with node size and colour
mapped to degree, role, nationality and sex, maximum-likelihood ERGM
estimation, AIC comparison and goodness-of-fit checks.

## Files

| File | Contents |
|---|---|
| `Project.Rmd` | Full analysis in R Markdown |
| `Project.pdf` | Rendered report with all plots and model output |

Data: the `gangs` network distributed with the Bergm package. Completed as an
industrial-modelling case study (2020).
