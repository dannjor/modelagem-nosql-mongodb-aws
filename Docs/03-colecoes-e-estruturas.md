# 4. Replicação e Particionamento

## Replicação de Dados
A replicação no MongoDB é implementada por meio de **Replica Sets**, que consistem em um conjunto de nós responsáveis por manter cópias sincronizadas dos dados.

Nesse modelo:
- Um nó atua como **Primary**, responsável por operações de escrita
- Os demais nós atuam como **Secondary**, replicando os dados de forma assíncrona
- Em caso de falha do nó primário, ocorre a eleição automática de um novo Primary

Benefícios da replicação:
- Alta disponibilidade
- Tolerância a falhas
- Continuidade das operações em cenários de indisponibilidade
- Possibilidade de direcionar leituras para nós secundários

## Particionamento (Sharding)
O particionamento de dados é utilizado para distribuir grandes volumes de dados entre múltiplos nós, permitindo escalabilidade horizontal.

No contexto deste projeto, o sharding é aplicado considerando:
- Volume crescente de vendas
- Alto número de consultas simultâneas
- Necessidade de balanceamento de carga

A escolha da **chave de shard** é um ponto crítico e deve:
- Possuir alta cardinalidade
- Distribuir dados de forma uniforme
- Evitar hotspots de escrita

Exemplos de chaves consideradas:
- Identificador da venda
- Identificador do cliente combinado com data

## Benefícios da Abordagem Distribuída
A combinação de replicação e particionamento permite:
- Escalar leitura e escrita de forma eficiente
- Manter alta disponibilidade
- Suportar crescimento contínuo do volume de dados
- Garantir desempenho mesmo sob alta carga

Essa arquitetura prepara o sistema para cenários reais de produção, alinhando-se às boas práticas de bancos de dados distribuídos.
