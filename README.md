# Trabalho Dieta e Treino - Dashboard Interativo

Arquivos nesta pasta:

- `dashboard.html`: versão interativa pronta para abrir no navegador, sem precisar de R ou Quarto.
- `dashboard.qmd`: versão Quarto do trabalho, com estrutura por páginas e gráficos interativos em `plotly`.
- `dados.csv`: base de dados usada no trabalho.

Para renderizar a versão Quarto em outro computador:

```r
install.packages(c("tidyverse", "plotly", "DT", "scales", "htmltools"))
```

Depois, no terminal ou no RStudio:

```bash
quarto render dashboard.qmd
```

A versão HTML já remove automaticamente a linha vazia do CSV original e recalcula os totais, médias e porcentagens a partir das 53 respostas válidas.
