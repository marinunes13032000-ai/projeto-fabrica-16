# ✅ Jogadores em Números — o perfil da galera do servidor

Uma **lan house** quer entender quem são seus jogadores e o que eles mais jogam.

Você foi convidado(a) por uma **lan house da sua cidade** para investigar os hábitos de jogo de 200 jogadores e transformar números em **decisões**.

A missão é direta e útil: **importar**, **limpar**, **analisar** e **visualizar** um dataset — tudo em **Google Colab**, usando **NumPy, Pandas, Matplotlib e Seaborn**.

Projeto pensado para **jovens de 14 a 18 anos**: linguagem técnica, mas acessível, e um toque de design para ficar gostoso de ler. ✨

> 🎯 **Nível:** conclusão do curso *Ciência de Dados com Python* (40h) — Aula 10, Projeto Integrador.
> 🚫 **Não usar:** machine learning, Scikit-learn, web ou banco de dados. Só as 4 bibliotecas do curso.

---

## 🎬 Enunciado — A missão do(a) cientista de dados

A dona da lan house quer **tomar decisões com dados**: qual jogo promover, em qual plataforma investir e que horários são de pico. Ela disponibilizou um CSV com o cadastro e o histórico de jogo dos clientes.

Sua missão: descobrir **padrões de jogo** (horas, pontuação, plataforma, nível) e entregar um relatório visual que responda: *quem são os jogadores do servidor?*

### 📊 O dataset

Arquivo `jogadores.csv` (200 linhas × 7 colunas) com os seguintes campos:

| Coluna | Tipo | Significado |
|---|---|---|
| `id_jogador` | int | código do jogador |
| `apelido` | str | nome no jogo |
| `jogo` | str | jogo principal (ex.: Minecraft, FIFA, Fortnite) |
| `plataforma` | str | PC, Console ou Mobile |
| `horas_jogadas` | float | total de horas no mês |
| `pontuacao` | int | pontuação média por partida |
| `nivel` | int | nível alcançado (1 a 100) |

> **Obs. didática:** os dados são **ilustrativos/simulados** para fins de estudo. Se quiser, troque por um dataset público do mesmo tema.

### O que o projeto deve conter (as 14 etapas)

1. **Importar** o CSV com `pd.read_csv`
2. **Explorar** com `head`, `shape`, `info` e `describe`
3. **Identificar** o que cada coluna significa
4. **Conferir os tipos** de cada coluna (`dtypes`) — estão certos?
5. **Tratar valores ausentes** — `dropna` ou `fillna` (justifique)
6. **Remover duplicados** — `duplicated()` e `drop_duplicates()`
7. **Responder 2 perguntas com filtros** — `df[df['col'] > x]`
8. **Criar 1 coluna nova** — calculada ou com `apply`
9. **Agrupar** com `groupby` por pelo menos 1 categoria
10. **Calcular medidas** com NumPy — `np.array`, `mean`, `max`, `min`, filtros booleanos
11. **Criar 4 gráficos** — Matplotlib e Seaborn, cada um com uma pergunta
12. **Interpretar** cada gráfico com 1 frase
13. **Escrever 3 descobertas** — frases completas, com números
14. **Apresentar 1 conclusão** — o que você recomendaria com base nos dados?

---

## 🔎 Perguntas-guia do projeto

| # | Pergunta | Pista de código |
|---|---|---|
| 1 | Qual jogo tem mais jogadores? | `value_counts()` |
| 2 | Qual plataforma concentra mais horas de jogo? | `groupby('plataforma')['horas_jogadas'].sum()` |
| 3 | Existe relação entre horas jogadas e pontuação? | `sns.scatterplot` |
| 4 | Quem são os jogadores acima do nível 50? | filtro booleano `df[df['nivel'] > 50]` |
| 5 | Há jogadores "fora da curva"? | `sns.boxplot` de `pontuacao` |

---

## 💻 Como rodar

**Pré-requisito:** uma conta Google (para o Colab) — nada mais.

```
1) Acesse colab.research.google.com
2) Envie o arquivo jogadores.csv pela aba de arquivos (📁)
3) Abra um novo notebook e siga as 14 etapas
4) Rode tudo com Shift + Enter e confira se não há erros
5) Exporte: Arquivo → Fazer download → .ipynb
```

Checklist antes de subir no GitHub:

- [ ] notebook roda do início ao fim **sem erros**
- [ ] dataset (`jogadores.csv`) na pasta `data/`
- [ ] pelo menos **4 gráficos** com título e eixos nomeados
- [ ] **3 descobertas** com números + **1 conclusão** final
- [ ] README preenchido com o que você descobriu

---

## 🧠 Conceitos trabalhados

- **NumPy:** arrays, `mean`/`max`/`min`, filtros booleanos
- **Pandas:** `read_csv`, `head`/`info`/`describe`, `loc`/`iloc`, filtros, `dropna`/`fillna`, `drop_duplicates`, colunas calculadas, `apply`, `groupby` + `agg`
- **Matplotlib:** linha, barras, histograma, dispersão (`plt.plot`, `plt.bar`, `plt.hist`, `plt.scatter`)
- **Seaborn:** `countplot`, `barplot`, `histplot`, `boxplot`, `scatterplot`, `heatmap` (correlação)
- **Boas práticas:** explorar antes de analisar · gráfico certo para cada pergunta · correlação não é causa

---

## 🚀 Próximos passos

- Recalcular tudo com um dataset público de games (Kaggle)
- Criar a coluna `categoria_nivel` com `apply` (iniciante, intermediário, veterano)
- Investigar: Mobile gera mais pontuação média que PC?
- Montar um `heatmap` de correlação entre as colunas numéricas

---

## 📂 Estrutura

```
projeto-jogadores-em-numeros/
├─ README.md            ← este arquivo
├─ notebooks/
│  └─ analise.ipynb     ← seu notebook no Colab
├─ data/
│  └─ jogadores.csv         ← o dataset
├─ img/                 ← prints dos gráficos
│  └─ grafico1.png
└─ LICENSE              ← MIT
```

---

## 📋 Rubrica de avaliação (0 a 10)

| Critério | Pontos |
|---|---|
| Importação e organização dos dados | 1,0 |
| Exploração inicial (`head`, `shape`, `info`, `describe`) | 1,0 |
| Limpeza (ausentes e duplicados) | 1,5 |
| Manipulação com Pandas (filtros, colunas, `groupby`) | 2,0 |
| Uso de NumPy | 1,0 |
| Visualizações (4 gráficos com propósito) | 2,0 |
| Interpretação (3 descobertas) | 1,0 |
| Apresentação (5–10 min) | 0,5 |
| **TOTAL** | **10,0** |

---

## 📝 Licença

Projeto sob **MIT** — use, adapte e compartilhe. ✅
