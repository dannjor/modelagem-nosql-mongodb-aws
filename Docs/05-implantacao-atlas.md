# 5. Implantação no MongoDB Atlas (AWS)

## Visão Geral da Implantação
A solução proposta foi implantada utilizando o **MongoDB Atlas**, serviço gerenciado de banco de dados MongoDB em cloud, com infraestrutura provisionada na **AWS**.

Essa abordagem elimina a necessidade de gerenciamento manual de servidores, permitindo foco na modelagem, escalabilidade e uso eficiente dos dados.

## Configuração do Cluster
A implantação contempla:
- Criação de um cluster MongoDB no Atlas
- Seleção da AWS como provedor de nuvem
- Definição de região conforme requisitos de latência
- Configuração de replica set para alta disponibilidade
- Possibilidade de habilitação de sharding conforme crescimento do volume de dados

O Atlas automatiza tarefas como backup, monitoramento e atualizações, reduzindo riscos operacionais.

## Segurança e Acesso
Foram consideradas boas práticas de segurança:
- Controle de acesso por usuário e permissões
- Restrição de IPs autorizados
- Comunicação segura via TLS
- Gerenciamento de credenciais pelo Atlas

Essas medidas garantem proteção dos dados e aderência a requisitos básicos de segurança.

## Escalabilidade e Manutenção
A arquitetura em cloud permite:
- Escalonamento vertical e horizontal sob demanda
- Monitoramento de performance em tempo real
- Ajustes rápidos de capacidade conforme a carga
- Alta disponibilidade sem intervenção manual

## Benefícios da Solução em Cloud
- Redução de custos operacionais
- Alta confiabilidade
- Facilidade de expansão
- Infraestrutura preparada para ambientes produtivos
- Integração com outros serviços da AWS

A utilização do MongoDB Atlas na AWS viabiliza uma solução robusta, escalável e alinhada às necessidades de sistemas modernos baseados em dados.

