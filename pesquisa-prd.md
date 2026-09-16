# 📄 Entendendo o PRD (Product Requirements Document)

O PRD (Product Requirements Document, ou Documento de Requisitos do Produto) é o artefato estratégico que define o que o produto deve fazer, para quem ele deve ser feito, por que ele importa e quais critérios determinam o sucesso da entrega.

Em outras palavras, o PRD responde às perguntas mais importantes antes de qualquer implementação:

- O que estamos construindo?
- Para quem estamos construindo?
- Qual problema estamos resolvendo?
- Quais requisitos são essenciais?
- Como saberemos se o resultado foi bem-sucedido?

Ele não fala apenas de interface ou tecnologia. Ele conecta visão de negócio, experiência do usuário, engenharia e métricas de sucesso.

Enquanto um wireframe mostra como a interface pode parecer, e a arquitetura define como o sistema será construído, o PRD define a intenção do produto e os critérios de valor que ele deve entregar.

---

## 🧭 Por que o PRD é importante?

Um bom PRD ajuda a:

- alinhar produto, design e engenharia
- reduzir retrabalho e ambiguidades
- evitar mudanças improvisadas no meio do desenvolvimento
- facilitar a priorização de funcionalidades
- estabelecer critérios claros para validação e release

Sem um PRD bem definido, o time corre o risco de construir algo que parece correto, mas não resolve o problema real do usuário ou não atende às metas do negócio.

---

## 📋 As 5 Seções Principais de um PRD

### 1. Contexto, Visão e Objetivos (Background, Vision & Goals)

Esta seção define a base estratégica do projeto. Ela não descreve botões, telas ou banco de dados; ela explica o problema de negócio e o valor que o produto pretende entregar.

Elementos importantes:

- O problema: qual dor, ineficiência ou oportunidade está sendo resolvida?
- O contexto: há dados de mercado, feedback de clientes, métricas atuais ou sinais do mercado?
- A visão da solução: como a funcionalidade proposta resolve esse problema?
- Objetivos estratégicos: isso está alinhado com OKRs, metas de crescimento, retenção, redução de custos ou melhoria de operação?

Exemplo:

- Problema: a equipe de atendimento está perdendo tempo com processos manuais.
- Visão: automatizar a triagem inicial para reduzir tempo de resposta e erros.
- Objetivo: reduzir o tempo de suporte em 30% em 6 meses.

### 2. Público-Alvo e Casos de Uso (Target Audience & Use Cases)

Antes de começar a modelar qualquer funcionalidade, é essencial entender quem será impactado pelo produto.

Elementos importantes:

- Personas: perfis semi-fictícios dos usuários finais
- Jornadas do usuário: como a pessoa percorre o processo para alcançar um objetivo
- Casos de uso: quais ações o usuário deve conseguir executar
- Edge cases: cenários raros, falhas ou condições extremas que o sistema precisa lidar corretamente

Exemplo:

- Persona: gestor de operação com rotina corrida, que usa celular em movimento e precisa tomar decisões rápidas
- Caso de uso: visualizar o status de pedidos em tempo real
- Edge case: sem internet, o sistema deve mostrar o último estado sincronizado e informar que os dados podem estar desatualizados

### 3. Escopo e Requisitos (Requirements & Out-of-Scope)

Esta é a seção mais importante para engenharia, porque transforma a visão em especificações claras e acionáveis.

Elementos importantes:

- Requisitos funcionais: o que o sistema deve fazer
- Requisitos não funcionais: performance, segurança, escalabilidade, disponibilidade, usabilidade e compliance
- Fora de escopo: o que será deliberadamente deixado para versões futuras

Os requisitos funcionais geralmente são escritos em formato de histórias de usuário, como:

- Como usuário, quero visualizar meus pedidos em tempo real para acompanhar entregas.
- Como administrador, quero filtrar relatórios por período para tomar decisões com mais rapidez.

Os requisitos não funcionais podem incluir:

- tempo de resposta inferior a 2 segundos
- criptografia de dados sensíveis
- suporte a 1.000 usuários simultâneos
- disponibilidade de 99,9%

O out-of-scope é tão importante quanto o escopo. Ele evita que o time aceite pedidos que não fazem parte do objetivo principal da entrega.

### 4. Premissas, Restrições e Dependências (Assumptions, Constraints & Dependencies)

Nenhum produto é construído em isolamento. Essa seção mapeia o ecossistema ao redor da solução.

Elementos importantes:

- Premissas: condições que a equipe considera verdadeiras para planejar o projeto
- Restrições: limitações de tempo, orçamento, infraestrutura, compliance ou tecnologia
- Dependências: APIs, integrações, aprovações, equipes externas ou terceiros

Exemplos:

- Premissa: 80% dos usuários acessam o sistema pelo celular
- Restrição: todos os dados financeiros devem ser armazenados de acordo com políticas de segurança
- Dependência: integração com um sistema legado da área financeira antes do lançamento

### 5. Métricas de Sucesso e Lançamento (Success Metrics & Go-To-Market)

O trabalho não termina quando o código é entregue. O verdadeiro objetivo é criar valor mensurável.

Elementos importantes:

- métricas quantitativas de sucesso
- dashboard de acompanhamento
- estratégia de lançamento
- plano de rollback
- critérios para evitar ou corrigir problemas em produção

Exemplos de métricas:

- aumentar a taxa de conversão em 10%
- reduzir o tempo médio de atendimento em 25%
- aumentar a retenção em 15% em 90 dias

Uma estratégia de lançamento pode incluir:

- rollout gradual para 10% dos usuários
- testes A/B para comparar versões
- monitoramento por alertas em tempo real

O plano de rollback define o que a equipe fará se o sistema causar regressões ou distúrbios na operação após o lançamento.

---

## ✅ O que um PRD bem escrito deve conter?

Um bom PRD deve responder, com clareza, às seguintes perguntas:

- Qual é o problema?
- Quem são os usuários?
- Qual é o objetivo do produto?
- O que precisa existir para atender esse objetivo?
- O que está fora do escopo?
- Quais são as restrições e dependências?
- Como mediremos sucesso?
- Como validaremos a entrega?

Se o documento não responde isso de forma objetiva, ele provavelmente está incompleto ou ambíguo.

---

## 🔎 Checklist para ler um PRD como senior

Ao analisar um PRD, vale questionar:

- O problema está descrito de forma clara e mensurável?
- O público-alvo está bem definido?
- Os requisitos são testáveis?
- Há critério de aceite para as principais funcionalidades?
- O escopo está bem delimitado?
- As dependências e riscos estão identificados?
- As métricas de sucesso são confiáveis e observáveis?
- Existe um plano de lançamento e reversão?

Os melhores times não apenas leem o PRD; eles questionam os pressupostos e desafiam hipóteses antes de construir.

---

## 🧩 Estrutura Resumida de um PRD

### 1. Visão geral
- Nome do projeto
- Resumo executivo
- Problema/ oportunidade

### 2. Objetivos e metas
- Objetivos de negócio
- Metas de usuário e de produto
- KPIs/OKRs

### 3. Público-alvo
- Personas
- Segmentos de usuários
- Necessidades e dores

### 4. Requisitos
- Funcionais
- Não funcionais
- Critérios de aceite

### 5. Escopo
- Dentro do escopo
- Fora do escopo

### 6. Restrições e dependências
- Premissas
- Limitações
- Integrações

### 7. Métricas e lançamento
- KPI principal
- Estratégia de rollout
- Plano de rollback

---

## 📝 Exemplo de template prático

### Título do Projeto
Sistema de gestão de pedidos internos

### Resumo Executivo
O projeto visa reduzir falhas de acompanhamento e melhorar a visibilidade do status dos pedidos entre os times de operação e atendimento.

### Problema
Hoje, os pedidos são acompanhados por mensagens e planilhas manuais, o que gera atraso, duplicidade e baixa visibilidade.

### Público-Alvo
- gestores de operação
- time de atendimento
- analistas de suporte

### Objetivos
- reduzir tempo de resposta em 30%
- aumentar visibilidade do status dos pedidos
- reduzir erros de comunicação entre equipes

### Requisitos Funcionais
- cadastrar pedidos
- atualizar status em tempo real
- visualizar histórico de movimentação
- filtrar pedidos por período e responsável

### Requisitos Não Funcionais
- resposta em até 2 segundos para leitura de dados
- autenticação segura
- disponibilidade de 99,9%

### Escopo
Dentro do escopo:
- cadastro e acompanhamento de pedidos
- visualização de status
- histórico de movimentação

Fora do escopo:
- pagamento integrado
- automação de cobrança
- integração com CRM externo nesta versão

### Métricas de Sucesso
- redução de 25% no tempo médio de atendimento
- aumento de 15% na taxa de conclusão de pedidos
- queda de 40% nos erros de comunicação

### Plano de Lançamento
- rollout gradual para 20% dos usuários
- acompanhamento de métricas por 7 dias
- ajustes antes da expansão

---

> 💡 Dica de Sênior: ao receber um PRD, não o trate como documento definitivo e imutável. O melhor time de produto e engenharia questiona premissas, identifica ambiguidades, sugere ajustes e transforma requisitos em decisões objetivas. O PRD é uma ferramenta de clareza, não apenas um registro de decisões.

---

## Conclusão

O PRD é um dos artefatos mais importantes para a criação de produtos com qualidade, previsibilidade e valor real. Ele conecta estratégia, usuário, tecnologia e resultado.

Quando bem feito, ele reduz ruído, orienta decisões e melhora a chance de entregar algo realmente útil para o usuário e para o negócio.

Se você quiser aprofundar no assunto, a próxima etapa é praticar a escrita de um PRD em um caso real, transformando uma ideia em um documento com objetivos, requisitos, métricas e critérios de aceite claros.

