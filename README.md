# Trabalho Dieta e Treino - Dashboard Interativo

Arquivos nesta pasta:

- `index.html`: entrada do site. No GitHub Pages, esse arquivo redireciona para o dashboard.
- `dashboard.html`: versão interativa em formato de landing page, pronta para abrir no navegador, sem precisar de R ou Quarto.
- `dashboard.qmd`: versão Quarto do trabalho, com estrutura por páginas e gráficos interativos em `plotly`.
- `dados.csv`: base de dados usada no trabalho.

Publicação no GitHub Pages:

1. Envie `index.html`, `dashboard.html`, `dados.csv`, `dashboard.qmd` e esta `README.md` para o repositório.
2. Em `Settings > Pages`, escolha `Deploy from a branch`.
3. Selecione a branch `main` e a pasta `/root`.
4. Depois de alguns minutos, o site ficará em `https://igorsiqqueira.github.io/dashboard/`.

Para renderizar a versão Quarto em outro computador:

```r
install.packages(c("tidyverse", "plotly", "DT", "scales", "htmltools"))
```

Depois, no terminal ou no RStudio:

```bash
quarto render dashboard.qmd
```

A versão HTML lê o `dados.csv` quando está publicada e também tem um fallback embutido, então abre localmente mesmo sem servidor. Ela recalcula totais, médias e porcentagens a partir das 53 respostas válidas.
