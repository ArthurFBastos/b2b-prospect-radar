# B2B Prospect Radar

Projeto de dados para analisar empresas B2B a partir de dados publicos de CNPJ e identificar cidades e segmentos com maior potencial de prospeccao.

## Sobre o projeto

A ideia deste projeto e simular uma demanda real de uma empresa de tecnologia que quer vender para outras empresas, mas ainda nao sabe bem quais regioes e segmentos priorizar.

Nesta primeira etapa, o foco esta na extracao e tratamento dos dados. A partir da base tratada, a ideia e evoluir para consultas SQL, indicadores, rankings e um dashboard.

## Pergunta principal

Em quais cidades e segmentos uma empresa B2B deveria concentrar seus esforcos de prospeccao?

## Escopo inicial

- Estado analisado: Minas Gerais
- Empresas consideradas: empresas ativas
- Segmentos de interesse: tecnologia, contabilidade, clinicas, escolas, consultorias, comercio atacadista e servicos profissionais

Comecei com um recorte menor para deixar o projeto mais viavel e facilitar a validacao do processo antes de expandir para outros estados.

## Fontes de dados

- [Dados Abertos CNPJ - Receita Federal](https://www.gov.br/receitafederal/pt-br/acesso-a-informacao/dados-abertos)
- [Arquivos publicos de CNPJ](https://arquivos.receitafederal.gov.br/dados/cnpj/dados_abertos_cnpj/)
- [IBGE](https://www.ibge.gov.br/)

## Tecnologias

- Python
- Pandas
- SQL
- BigQuery
- Looker Studio

## Pipeline previsto

```mermaid
flowchart LR
    A[Dados publicos] --> B[Extracao]
    B --> C[Tratamento com Python]
    C --> D[Base processada]
    D --> E[Analises em SQL]
    E --> F[Dashboard]
```

## Etapas

1. Definicao do problema e do recorte do projeto
2. Coleta dos dados publicos de CNPJ
3. Tratamento e padronizacao dos arquivos com Python
4. Filtro por UF, situacao cadastral e segmentos de interesse
5. Criacao de uma base processada para analise
6. Desenvolvimento de consultas SQL e indicadores
7. Construcao de dashboard com os principais resultados

## Estrutura do repositorio

```text
b2b-prospect-radar/
|-- data/
|   |-- raw/
|   `-- processed/
|-- notebooks/
|-- src/
|-- sql/
|-- docs/
|-- README.md
`-- requirements.txt
```

## Indicadores que pretendo gerar

- Quantidade de empresas ativas por cidade
- Ranking de cidades com maior potencial B2B
- Segmentos mais presentes em cada municipio
- Distribuicao de empresas por CNAE
- Score simples de oportunidade comercial
