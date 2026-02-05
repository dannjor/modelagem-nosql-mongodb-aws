# 2. Estratégia de Modelagem NoSQL

## Abordagem de Modelagem
A modelagem de dados não relacional adotada neste projeto segue o paradigma orientado a documentos, característico do MongoDB. Diferentemente do modelo relacional, essa abordagem prioriza os padrões de acesso aos dados, buscando reduzir a necessidade de joins e otimizar as consultas mais frequentes.

A definição da estrutura das coleções foi orientada pelas principais operações do sistema de e-commerce, como consulta de pedidos, histórico de compras por cliente e controle de produtos e estoque.

## Embedding vs Reference
Um dos principais pontos de decisão em bancos NoSQL é a escolha entre **embedding** (documentos aninhados) e **reference** (referências entre documentos).

Neste projeto, foram adotadas as seguintes diretrizes:
- **Embedding** para dados fortemente relacionados e frequentemente acessados em conjunto  
  - Exemplo: itens de um pedido dentro do documento de vendas
- **Reference** para dados compartilhados ou de grande volume  
  - Exemplo: informações de produtos e clientes referenciadas em pedidos

Essa abordagem reduz duplicação excessiva de dados, mantém flexibilidade e melhora o desempenho das consultas mais comuns.

## Orientação por Padrões de Acesso
A modelagem foi pensada considerando os principais padrões de acesso:
- Consulta de pedidos por cliente
- Análise do histórico de compras
- Acompanhamento de vendas por período
- Consulta rápida de informações de produtos

Ao alinhar a estrutura dos documentos aos padrões de consulta, o modelo minimiza leituras desnecessárias e melhora a eficiência da aplicação.

## Trade-offs e Considerações
A escolha pelo modelo NoSQL implica em alguns trade-offs:
- Possível duplicação controlada de dados
- Maior responsabilidade da aplicação na integridade
- Menor rigidez de schema

Esses pontos foram considerados aceitáveis diante dos ganhos em escalabilidade, flexibilidade e desempenho, especialmente para um cenário de e-commerce em crescimento.

A modelagem proposta busca equilibrar simplicidade, desempenho e capacidade de evolução do sistema ao longo do tempo.

