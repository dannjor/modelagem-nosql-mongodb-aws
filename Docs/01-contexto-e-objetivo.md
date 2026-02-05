# 1. Contexto e Objetivo

## Contexto
Este projeto foi desenvolvido a partir de um desafio prático de modelagem de dados, com foco na utilização de bancos de dados não relacionais em um cenário de e-commerce.

O contexto simula uma empresa de vendas online com alto volume de transações, diversidade de produtos e necessidade de escalabilidade. Nesse cenário, o modelo relacional tradicional apresenta limitações relacionadas à flexibilidade de schema e desempenho em consultas complexas e distribuídas.

Diante disso, optou-se pela utilização do MongoDB, explorando o modelo orientado a documentos, que permite maior adaptabilidade às mudanças do negócio e melhor performance para determinados padrões de acesso aos dados.

A solução considera também a implantação em ambiente cloud, utilizando MongoDB Atlas na AWS, garantindo alta disponibilidade, escalabilidade e facilidade de gerenciamento.

## Objetivo
O objetivo principal do projeto é propor uma modelagem de dados não relacional eficiente e escalável, alinhada às necessidades de um sistema de e-commerce moderno.

Objetivos específicos:
- Modelar os dados utilizando o paradigma orientado a documentos
- Definir estruturas adequadas para leitura e escrita em larga escala
- Aplicar conceitos de embedding e reference de forma estratégica
- Considerar cenários de crescimento e distribuição dos dados
- Explorar mecanismos de replicação e particionamento
- Demonstrar a viabilidade da solução em ambiente cloud (MongoDB Atlas / AWS)

Este projeto tem como foco demonstrar a tomada de decisão em modelagem NoSQL, considerando trade-offs técnicos e impactos diretos no desempenho e na escalabilidade da solução.

