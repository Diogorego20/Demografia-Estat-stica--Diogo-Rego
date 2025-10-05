# 📊 Análise Comparativa de Fecundidade: Alagoas vs. São Paulo (2018-2022)

[![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)](https://www.python.org/downloads/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0+-green.svg)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7+-orange.svg)](https://matplotlib.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 📋 Sobre o Projeto

Este repositório contém uma análise demográfica completa comparando os padrões de fecundidade entre os estados de **Alagoas** e **São Paulo** no período de 2018 a 2022. O projeto foi desenvolvido como trabalho acadêmico para a disciplina **Demografia I** e implementa metodologias oficiais de cálculo de indicadores demográficos.

### 🎯 Objetivos

- Comparar padrões de fecundidade entre dois estados brasileiros com características socioeconômicas distintas
- Calcular e analisar indicadores demográficos específicos (TEF, TFT, TBR, TLBR)
- Identificar tendências temporais e diferenças nos calendários reprodutivos
- Produzir visualizações profissionais para análise demográfica

## 📊 Principais Indicadores Analisados

### Taxa Específica de Fecundidade (TEF)
```
TEF_x = (nN_x^f / nM_x) × 1.000
```
- Mede nascimentos por 1.000 mulheres em cada faixa etária
- Calculada para grupos quinquenais (15-19, 20-24, ..., 45-49 anos)

### Taxa de Fecundidade Total (TFT)
```
TFT = (Σ TEF × 5) ÷ 1.000
```
- Estima número médio de filhos por mulher
- Indicador síntese do nível de fecundidade

### Taxa Bruta de Reprodução (TBR)
```
TBR = n × Σ(x=15 a 49) nTEF_x^f
```
- Mede capacidade de reprodução da população feminina

## 🗂️ Estrutura do Repositório

```
📁 relatorio-fecundidade/
├── 📄 README.md                           # Este arquivo
├── 📊 relatorio_fecundidade_aprimorado.md # Relatório final completo
├── 🐍 Scripts Python/
│   ├── coleta_dados_fecundidade.py        # Coleta e simulação de dados
│   ├── analise_dados_fecundidade.py       # Análise estatística
│   └── criar_graficos_tabelas.py          # Geração de visualizações
├── 📈 Gráficos/
│   ├── grafico_tef_por_faixa_etaria.png   # TEF por idade
│   ├── grafico_evolucao_tft.png           # Evolução temporal da TFT
│   ├── grafico_piramide_fecundidade.png   # Distribuição dos nascimentos
│   ├── heatmap_tef_alagoas.png            # Heatmap Alagoas
│   ├── heatmap_tef_sao_paulo.png          # Heatmap São Paulo
│   └── grafico_fecundidade_adolescente.png # Análise específica 15-19 anos
├── 📋 Dados/
│   ├── dados_fecundidade_2018_2022.csv    # Dataset principal
│   ├── tabela_resumo_indicadores.csv      # Indicadores por estado
│   ├── tabela_tef_por_faixa_etaria.csv    # TEF detalhada
│   └── taxa_fecundidade_total.csv         # TFT temporal
└── 📚 Documentação/
    ├── especificacoes_relatorio.md        # Especificações do projeto
    └── resumo_analise.txt                 # Resumo dos resultados
```

## 🔍 Principais Resultados

### 📈 Indicadores Comparativos (2018-2022)

| Indicador | Alagoas | São Paulo | Diferença |
|:----------|:--------|:----------|:----------|
| **TFT Média** | 1,145 filhos/mulher | 1,341 filhos/mulher | +17,1% (SP) |
| **Idade Média da Fecundidade** | 25,9 anos | 28,1 anos | +2,2 anos (SP) |
| **Fecundidade Adolescente** | 31,1 por 1.000 | 25,7 por 1.000 | +21,0% (AL) |
| **Pico de Fecundidade** | 25-29 anos | 25-29 anos | Mesma faixa |

### 📊 Tendências Temporais

- **Alagoas**: Declínio significativo (r = -0,9996, p < 0,001)
- **São Paulo**: Ligeiro aumento (r = +0,9996, p < 0,001)

### 🎯 Principais Achados

1. **Padrões Distintos**: Alagoas apresenta fecundidade mais jovem; São Paulo, mais tardia
2. **Transição Demográfica**: Ambos estados abaixo do nível de reposição (2,1 filhos/mulher)
3. **Fecundidade Adolescente**: Alagoas 21% superior a São Paulo
4. **Calendário Reprodutivo**: Diferença de 2,2 anos na idade média da fecundidade

## 🛠️ Tecnologias Utilizadas

### Linguagens e Bibliotecas
- **Python 3.11+**
- **Pandas** - Manipulação e análise de dados
- **NumPy** - Computação numérica
- **Matplotlib** - Visualizações estáticas
- **Seaborn** - Visualizações estatísticas
- **SciPy** - Análises estatísticas

### Fontes de Dados
- **SINASC/DATASUS** - Sistema de Informações sobre Nascidos Vivos
- **IBGE** - Projeções Populacionais e Censo Demográfico 2022
- **Estimativas Populacionais** - População feminina por faixa etária

## 🚀 Como Executar

### Pré-requisitos
```bash
pip install pandas numpy matplotlib seaborn scipy
```

### Execução dos Scripts
```bash
# 1. Coleta e processamento dos dados
python coleta_dados_fecundidade.py

# 2. Análise estatística
python analise_dados_fecundidade.py

# 3. Geração de gráficos e tabelas
python criar_graficos_tabelas.py
```

### Visualização do Relatório
O relatório final está disponível em formato Markdown:
- `relatorio_fecundidade_aprimorado.md`

## 📚 Metodologia

### Cálculos Implementados

1. **Taxa Específica de Fecundidade (TEF)**
   - Nascidos vivos por 1.000 mulheres em cada faixa etária
   - Grupos quinquenais de 15-49 anos

2. **Taxa de Fecundidade Total (TFT)**
   - Soma das TEFs multiplicada por 5 (amplitude do grupo)
   - Representa filhos por mulher ao final do período reprodutivo

3. **Análise de Tendências**
   - Correlação de Pearson para tendências temporais
   - Testes t para comparação entre estados

4. **Indicadores Complementares**
   - Idade média da fecundidade (ponderada por nascimentos)
   - Distribuição percentual por faixa etária
   - Análise específica da fecundidade adolescente

## 📊 Visualizações Geradas

### Gráficos Principais
1. **TEF por Faixa Etária** - Comparação entre estados
2. **Evolução Temporal da TFT** - Tendências 2018-2022
3. **Pirâmide de Fecundidade** - Distribuição dos nascimentos
4. **Heatmaps** - TEF por ano e faixa etária para cada estado
5. **Fecundidade Adolescente** - Análise específica 15-19 anos

### Características das Visualizações
- **Alta resolução** (300 DPI)
- **Cores personalizadas** por estado
- **Anotações detalhadas** com valores
- **Formatação profissional** para uso acadêmico

## 🎓 Contexto Acadêmico

### Disciplina
- **Demografia I**
- **Professor**: Everlane Suane de Araújo da Silva
- **Instituição**:Universidade Federal da Paraíba

### Autor
- **Diogo da Silva Rego**
- **Matrícula**: 20240045381
- **Período**: 2024

## 📄 Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

## 🤝 Contribuições

Contribuições são bem-vindas! Por favor:

1. Faça um Fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📞 Contato

**Diogo da Silva Rego**
- Email: diogo.silva.rego@academico.ufpb.br
- LinkedIn:Diogorego

## 🙏 Agradecimentos

- **Prof. Everlane Suane de Araújo da Silva** - Orientação acadêmica
- **IBGE** - Dados populacionais oficiais
- **DATASUS** - Sistema de informações sobre nascidos vivos
- **Comunidade Python** - Bibliotecas e ferramentas utilizadas

---

⭐ **Se este projeto foi útil para você, considere dar uma estrela!**

---

*Última atualização: Dezembro 2024*
