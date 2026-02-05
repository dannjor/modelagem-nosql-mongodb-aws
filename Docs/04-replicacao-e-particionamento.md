# 3. Coleções e Estruturas de Dados

## Visão Geral
A modelagem proposta organiza os dados do sistema de e-commerce em coleções que refletem as principais entidades do negócio. Cada coleção foi definida considerando volume de dados, frequência de acesso e padrões de consulta.

A estrutura busca equilibrar flexibilidade, desempenho e simplicidade operacional.

## Coleção: Clientes
Armazena as informações principais dos clientes da plataforma.

Principais atributos:
- Identificador do cliente
- Dados cadastrais
- Informações de contato
- Data de criação e status

Os dados de clientes são referenciados em outras coleções, evitando duplicação excessiva e facilitando atualizações.

## Coleção: Produtos
Responsável por armazenar os dados dos produtos disponíveis para venda.

Principais atributos:
- Identificador do produto
- Descrição e categoria
- Preço
- Informações de estoque
- Status do produto

Essa coleção é amplamente referenciada em vendas e carrinhos, sendo mantida de forma normalizada para garantir consistência.

## Coleção: Vendas
Representa as transações realizadas na plataforma.

Estrutura adotada:
- Identificador da venda
- Referência ao cliente
- Data da venda
- Valor total
- Lista de itens vendidos (embedding)

Cada documento de venda contém os itens adquiridos, com informações como produto, quantidade e valor no momento da compra. Essa abordagem facilita consultas de histórico e análise de pedidos.

## Coleção: Carrinho
Armazena os itens adicionados ao carrinho de compras antes da finalização do pedido.

Principais características:
- Associação direta ao cliente
- Lista de produtos em formato embedded
- Atualização frequente

Por se tratar de dados temporários e altamente voláteis, essa coleção foi pensada para operações rápidas de leitura e escrita.

## Coleção: Histórico de Compras
Utilizada para consultas analíticas e acompanhamento do comportamento do cliente ao longo do tempo.

Pode ser implementada como:
- Coleção dedicada para histórico
- Ou visão derivada a partir da coleção de vendas

Essa estrutura facilita análises como recorrência, ticket médio e perfil de consumo.

## Considerações Gerais
- Dados frequentemente acessados em conjunto foram modelados com embedding
- Entidades compartilhadas foram referenciadas
- A estrutura permite evolução sem necessidade de migrações complexas
- O modelo está preparado para crescimento de volume e diversidade de dados

