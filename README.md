# 🎲 Projeto de Análise de Dados – Jogos e Brinquedos

> **Equipe:** Alfa (6 pessoas) | **Metodologia:** Scrum (Sprint 1) | **Tema:** Mercado de jogos e brinquedos

> ⚠️ **Nota:** os números e insights abaixo são **ilustrativos**, criados para a simulação Scrum. Ao conectar o conjunto de dados real, substitua os valores pelos resultados das análises da equipe e remova esta nota.

---

## 📌 Objetivo

Analisar dados de vendas e avaliações de jogos e brinquedos para responder:

1. Quais categorias vendem mais e geram mais receita?
2. Como as vendas variam ao longo do ano?
3. Qual a relação entre preço, faixa etária e avaliação dos clientes?
4. Que oportunidades o negócio pode explorar?

---

## 👥 Equipe e Papéis

| # | Membro | Papel | Responsabilidades |
|---|---|---|---|
| 1 | _Joana_ | **Scrum Master** | Facilita reuniões, controla o timer, remove bloqueios, conduz a retrospectiva |
| 2 | _Esdras_ | **Coleta e Importação de Dados** | Obter o dataset, organizar `/data`, documentar a fonte |
| 3 | _Tamires_ | **Limpeza de Dados** | Tratar nulos, duplicados, tipos e padronização |
| 4 | _Nathany_ | **Análise Exploratória** | Estatísticas descritivas, correlações e padrões |
| 5 | _Flavia_ | **Visualização de Dados** | Gráficos, dashboards e exportação das imagens |
| 6 | _Lucas_ | **Apresentação** Apresentação com Storytelling |

> Os papéis são flexíveis: quem terminar antes ajuda os colegas, e o Scrum Master também pode contribuir com tarefas técnicas.

---

## 🛠️ Ferramentas

- **Python** (pandas, matplotlib, seaborn)
- **Jupyter Notebook / Google Colab**
- **GitHub Projects** (quadro Scrum/Kanban)
- **Git** para versionamento (uma branch por membro)

---

## 📁 Estrutura do Repositório

```
/data            → dados brutos e tratados (.csv)
/notebooks       → 01_coleta | 02_limpeza | 03_exploratoria | 04_visualizacoes
/visualizacoes   → gráficos exportados (.png)
README.md        → este documento
requirements.txt → dependências
```

### Convenção de branches

| Membro | Branch |
|---|---|
| 2 – Coleta | `feature/coleta-de-dados` |
| 3 – Limpeza | `feature/limpeza-de-dados` |
| 4 – Exploratória | `feature/analise-exploratoria` |
| 5 – Visualização | `feature/visualizacoes` |
| 6 – Documentação | `feature/documentacao` |

Todo código entra na `main` via **Pull Request revisado por pelo menos 1 colega**.

---

## 🧹 Resumo da Limpeza de Dados

| Problema encontrado | Tratamento aplicado |
|---|---|
| Valores nulos em `avaliacao` | Preenchidos com a mediana da categoria |
| Registros duplicados de pedidos | Removidos pelo `id_pedido` |
| Preços como texto (`"R$ 49,90"`) | Convertidos para `float` |
| Categorias com grafias diferentes | Padronizadas |
| Datas em formatos mistos | Convertidas para `datetime` |

---

## 💡 Principais Insights

| # | Insight | Resultado (ilustrativo) | Recomendação | Responsável |
|---|---|---|---|---|
| 1 | **Sazonalidade forte no fim do ano** | Dia das Crianças, Black Friday e Natal somam ~45% da receita anual | Antecipar estoque e campanhas a partir de setembro | Membro 4 |
| 2 | **Jogos de tabuleiro e quebra-cabeças lideram em ticket médio** | Maior ticket e melhores avaliações; pelúcias vendem em volume, mas com margem menor | Destacar tabuleiros em kits e combos | Membro 4 |
| 3 | **Brinquedos educativos/STEM crescem acima da média** | Maior crescimento entre as categorias, puxado por pais, avós e escolas | Ampliar catálogo e criar parcerias com escolas | Membro 5 |
| 4 | **Faixa etária influencia a avaliação** | 3–6 anos têm as melhores notas; 0–2 anos concentram queixas de segurança e durabilidade | Reforçar certificações e comunicação de segurança | Membro 3 |
| 5 | **Preço alto não garante nota alta** | Correlação fraca entre preço e avaliação | Investir em descrições, fotos e indicação de faixa etária | Membro 4 |
| 6 | **Clientes recorrentes valem mais** | Quem compra mais de uma vez gasta bem mais ao longo do ano; prefere colecionáveis e expansões | Programa de fidelidade e lançamentos em série | Membro 6 |

---

## 📊 Visualizações Produzidas

| Gráfico | Pergunta que responde | Responsável |
|---|---|---|
| Linha: vendas por mês | Existe sazonalidade? | Membro 5 |
| Barras: receita por categoria | Quais categorias lideram? | Membro 5 |
| Boxplot: avaliação por faixa etária | Qual público avalia melhor? | Membro 4 |
| Dispersão: preço × avaliação | Preço influencia a satisfação? | Membro 4 |

```markdown
![Vendas por mês](visualizacoes/vendas_por_mes.png)
```

---

## 🏃 Sprint 1

**Meta:** dados limpos e análise exploratória inicial com 4 visualizações.

### Quadro de tarefas

| Tarefa | Responsável | Apoio | Status |
|---|---|---|---|
| Coletar e importar dados | Membro 2 | Membro 3 | ✅ Pronto |
| Limpeza de dados | Membro 3 | Membro 2 | ✅ Pronto |
| Análise exploratória | Membro 4 | Membro 3 | ✅ Pronto |
| Criar visualizações | Membro 5 | Membro 4 | ✅ Pronto |
| Documentar insights no README | Membro 6 | Membro 1 | ✅ Pronto |
| Revisão de PRs e `requirements.txt` | Membro 6 | Todos | ✅ Pronto |
| Facilitar Dailies e retrospectiva | Membro 1 | — | ✅ Pronto |

### Cronograma simulado (5 dias × 4 min)

| Dia | Foco da equipe | Movimento no quadro |
|---|---|---|
| 1 | Membro 2 importa dados; Membros 4, 5 e 6 estudam o dataset e preparam templates | Coleta → Em Andamento |
| 2 | Membro 3 inicia a limpeza; Membro 2 conclui a coleta | Coleta → Pronto; Limpeza → Em Andamento |
| 3 | Membro 3 finaliza a limpeza; Membro 4 inicia a exploração | Limpeza → Pronto; Exploratória → Em Andamento |
| 4 | Membro 4 busca padrões; Membro 5 constrói gráficos | Exploratória → Pronto; Visualização → Em Andamento |
| 5 | Membro 5 finaliza gráficos; Membro 6 consolida o README e revisa PRs | Visualização e Documentação → Pronto |

### Modelo de Daily Scrum (exemplo – Dia 2)

| Membro | Ontem | Hoje | Bloqueios |
|---|---|---|---|
| 1 – Scrum Master | Organizei o quadro | Acompanhar o timer e os bloqueios | Nenhum |
| 2 – Coleta | Importei os dados | Documentar a fonte e apoiar a limpeza | Nenhum |
| 3 – Limpeza | Identifiquei nulos | Tratar nulos e duplicados | Dúvida sobre outliers |
| 4 – Exploratória | Estudei as colunas | Estatísticas descritivas | Aguardando dados limpos |
| 5 – Visualização | Pesquisei tipos de gráfico | Preparar template de visualização | Nenhum |
| 6 – Documentação | Montei o esqueleto do README | Configurar `requirements.txt` | Nenhum |

### Retrospectiva

| ✅ O que deu certo | 🔧 O que melhorar |
|---|---|
| Dailies rápidas e objetivas | Critérios de "pronto" mais claros |
| Uso de branches e Pull Requests | Quebrar tarefas dependentes em partes menores |
| Quadro atualizado diariamente | Estimar melhor o tempo das tarefas |
| Boa divisão de papéis entre 6 pessoas | Reduzir ociosidade de quem depende da limpeza (Membros 4 e 5) |

---

## ⚠️ Desafios de Equipes de 6 Pessoas

| Desafio | Como lidar |
|---|---|
| Mais gente, mais conflitos de merge | Uma branch por pessoa, commits pequenos e PRs curtos |
| Dependência entre tarefas (limpeza → análise → gráficos) | Trabalhar com dados de amostra enquanto a limpeza termina |
| Dailies longas | Limite de 1 minuto por pessoa; assuntos técnicos ficam para depois |
| Membros ociosos | Programação em pares e redistribuição de tarefas pelo Scrum Master |
| Decisões demoradas | Votação rápida; o Scrum Master desempata |

## ⚠️ Limitações dos Dados

- Os dados podem não representar todo o mercado (viés de amostra).
- Correlação não implica causalidade.
- Avaliações de clientes podem conter viés de resposta.

## 🚀 Próximos Passos (Sprint 2)

- [ ] Analisar o impacto de promoções nas vendas (Membro 4)
- [ ] Segmentar clientes por clusterização (Membro 3)
- [ ] Construir modelo simples de previsão de demanda (Membro 2)
- [ ] Criar dashboard interativo (Membro 5)
- [ ] Atualizar a documentação e revisar o código (Membro 6)
- [ ] Facilitar planejamento e retrospectiva (Membro 1)

---

## ▶️ Como Executar

```bash
git clone https://github.com/equipe/projeto-analise-jogos-brinquedos.git
cd projeto-analise-jogos-brinquedos
pip install -r requirements.txt
jupyter notebook
```
