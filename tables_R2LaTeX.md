When you are preparing a report, presentation or writing your thesis, you may sometimes need to create table based on results obtained in `R`. Obviously, you'd rather not copy manually all values from R to LaTeX.

Here's an easier, quicker and more reliable way to do this:

```
library(xtable)
x = iris[1:6,]
x |> xtable(digits = 2) |> print(include.rownames = F)
```

The output is:
```
% latex table generated in R 4.3.0 by xtable 1.8-4 package
% Fri Mar  8 15:42:07 2024
\begin{table}[ht]
\centering
\begin{tabular}{rrrrl}
  \hline
Sepal.Length & Sepal.Width & Petal.Length & Petal.Width & Species \\ 
  \hline
5.10 & 3.50 & 1.40 & 0.20 & setosa \\ 
  4.90 & 3.00 & 1.40 & 0.20 & setosa \\ 
  4.70 & 3.20 & 1.30 & 0.20 & setosa \\ 
  4.60 & 3.10 & 1.50 & 0.20 & setosa \\ 
  5.00 & 3.60 & 1.40 & 0.20 & setosa \\ 
  5.40 & 3.90 & 1.70 & 0.40 & setosa \\ 
   \hline
\end{tabular}
\end{table}
```

If you need to edit the LaTeX code generated above, you can either exploit the further options offered by [xtable](https://cran.r-project.org/web/packages/xtable/) or edit the given output manually.
