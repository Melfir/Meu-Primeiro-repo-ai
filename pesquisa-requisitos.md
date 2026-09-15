# Requisitos Funcionais vs. Requisitos Não Funcionais

> **A regra de ouro:** Requisitos **Funcionais** = **O QUE** o sistema faz | Requisitos **Não Funcionais** = **COMO** o sistema faz

---

## 📚 Índice
- [Requisitos Funcionais](#-requisitos-funcionais-o-que-o-sistema-faz)
- [Requisitos Não Funcionais](#-requisitos-não-funcionais-como-o-sistema-faz)
- [Comparação Rápida](#-comparação-rápida)
- [Casos que Confundem](#-casos-que-confundem)
- [Analogia da Casa](#-dica-de-sênior-a-analogia-da-casa)
- [Checklist Prático](#-checklist-prático)

---

## 🛠️ Requisitos Funcionais (O QUE o sistema faz)

São as ações que o usuário pode realizar ou as regras de negócio que o aplicativo precisa executar para funcionar. Se um requisito funcional faltar, o sistema simplesmente não faz o que deveria fazer.

**Características:**
- Descrevem **funcionalidades visíveis** ao usuário
- Podem ser testadas com testes funcionais (UI, fluxos)
- São o "core" do sistema

### Exemplos práticos (App estilo iFood)

1. **Cadastro e Login:** O usuário deve ser capaz de criar uma conta usando seu e-mail e senha ou fazendo login via Google/Apple.
2. **Carrinho de Compras:** O cliente deve poder adicionar, remover e alterar a quantidade de itens no carrinho antes de finalizar a compra.
3. **Rastreamento em Tempo Real:** O aplicativo deve permitir que o cliente acompanhe a localização do entregador no mapa.
4. **Filtros de Busca:** O usuário deve poder filtrar restaurantes por categoria, avaliação e tempo de entrega.
5. **Histórico de Pedidos:** Manter registro de todos os pedidos anteriores com detalhes e opção de reordenação.

---

## 🚀 Requisitos Não Funcionais (COMO o sistema faz)

São os critérios de qualidade do sistema. Eles não são uma "funcionalidade" que o usuário clica, mas garantem que a experiência seja boa, segura e rápida. Envolvem performance, segurança, escalabilidade, confiabilidade e usabilidade.

**Características:**
- Descrevem **qualidades do sistema**
- Medidas em métricas quantificáveis
- Relacionadas a como o sistema se comporta sob diferentes condições

### Exemplos práticos (App estilo iFood)

1. **Performance (Desempenho):** O aplicativo deve carregar a lista de restaurantes próximos em no máximo 2 segundos, mesmo com internet 3G.
2. **Escalabilidade (Capacidade):** O backend deve suportar picos de até 100.000 usuários simultâneos na noite de sexta-feira sem indisponibilidade.
3. **Segurança:** Dados de cartão de crédito devem ser criptografados (PCI DSS compliant) e nunca salvos em texto puro.
4. **Disponibilidade (Uptime):** O sistema deve estar disponível 99.9% do tempo (máximo 8h de downtime/ano).
5. **Usabilidade:** Qualquer usuário deve completar um pedido em menos de 3 minutos, com no máximo 4 cliques.
6. **Compatibilidade:** Suportar iOS 12+, Android 8+ e resoluções de tela de 320px a 1920px.

---

## 📊 Comparação Rápida

| **Aspecto** | **Funcional (RF)** | **Não Funcional (RNF)** |
|-----------|-------------------|----------------------|
| **Pergunta** | O QUE o sistema faz? | COMO o sistema faz? |
| **Foco** | Ações e funcionalidades | Qualidade e desempenho |
| **Exemplo** | Adicionar item ao carrinho | Carregar em < 2 segundos |
| **Teste** | Testes funcionais, UAT | Testes de carga, segurança |
| **Impacto** | Sem isso, sistema não funciona | Sem isso, experiência é ruim |
| **Métrica** | Sim ou Não (funciona/não funciona) | Numérica (velocidade, % uptime) |

---

## ⚠️ Casos que Confundem

Nem sempre é óbvio se algo é funcional ou não-funcional. Aqui estão casos comuns:

### 🔔 Notificação Push em Tempo Real
- **Funcional:** "O app deve enviar notificações quando um pedido é aceito"
- **Não Funcional:** "A notificação deve ser entregue em < 500ms"

### 🌙 Dark Mode
- **Funcional:** "O app deve ter modo escuro" (é uma feature)
- **Não Funcional:** "A mudança de tema deve ocorrer em < 300ms" (é a qualidade)

### 🔐 Autenticação com 2FA
- **Funcional:** "O usuário deve fazer login com e-mail + SMS (2FA)"
- **Não Funcional:** "O SMS deve chegar em < 2 minutos"

### 📍 Geolocalização
- **Funcional:** "Mostrar restaurantes próximos ao usuário"
- **Não Funcional:** "Precisão de localização ±100 metros com 95% de confiabilidade"

---

## 💡 Dica de Sênior: A Analogia da Casa

Pense em uma casa para entender a diferença:

**Requisitos Funcionais:** A casa precisa ter...
- 3 quartos
- 2 banheiros
- 1 cozinha
- Uma porta na frente

**Requisitos Não Funcionais:** A casa precisa...
- Suportar ventos de 100 km/h
- Ter isolamento acústico de 60dB
- Ser construída em até 6 meses
- Manter temperatura interna entre 18-25°C
- Resistir a terremotos de 7.0 na escala Richter

Sem os RF, você não tem uma casa. Sem os RNF, você tem uma casa que desaba no primeiro vento! 🌪️

---

## ✅ Checklist Prático

Antes de iniciar seu projeto, certifique-se de:

### Requisitos Funcionais
- [ ] Todos os fluxos de usuário estão documentados?
- [ ] Cada ação possível foi listada?
- [ ] As regras de negócio foram definidas?
- [ ] Os casos de sucesso e erro foram considerados?

### Requisitos Não Funcionais
- [ ] Métricas de performance foram definidas (tempo de resposta, throughput)?
- [ ] Requisitos de segurança foram estabelecidos (criptografia, compliance)?
- [ ] Capacidade e escalabilidade foram estimadas (quantos usuários simultâneos)?
- [ ] Disponibilidade/Uptime foi acordado (99.9%? 99.99%)?
- [ ] Compatibilidade de plataformas/navegadores foi definida?
- [ ] Requisitos de acessibilidade foram considerados (WCAG, ARIA)?

### Validação
- [ ] Stakeholders revisaram e aprovaram os requisitos?
- [ ] RF e RNF foram priorizados?
- [ ] Critérios de aceitação foram definidos?

---

## 📋 Template para Seu Projeto

Use este formato para documentar requisitos:

```
### RF-001: [Nome do Requisito Funcional]
**Descrição:** O que o sistema deve fazer
**Ator:** Quem faz (usuário, admin, sistema)
**Pré-condições:** Situação inicial necessária
**Fluxo Principal:** Passo a passo
**Fluxo Alternativo:** Cenários alternativos
**Pós-condições:** Resultado esperado
**Critério de Aceitação:** DADO que..., QUANDO..., ENTÃO...

---

### RNF-001: [Nome do Requisito Não Funcional]
**Tipo:** Performance | Segurança | Escalabilidade | Usabilidade | Compatibilidade
**Descrição:** O critério de qualidade
**Métrica:** Valor numérico e unidade (ex: < 2 segundos, 99.9% uptime)
**Prioridade:** Alta | Média | Baixa
**Como Testar:** Método de validação
```

---

## 🔗 Referências e Padrões

- **ISO/IEC/IEEE 29148:** Engenharia de Requisitos - padrão internacional
- **ABNT NBR 13596:** Norma técnica brasileira de requisitos
- **User Stories:** "Como [ator], quero [ação], para [benefício]" (RFC)
- **Acceptance Criteria:** "DADO [contexto], QUANDO [ação], ENTÃO [resultado]" (BDD)

---

## 💬 Dúvidas Comuns

**P: Posso ter um requisito que seja funcional E não-funcional?**  
R: Sim! Uma funcionalidade (RF) sempre tem critérios de qualidade (RNF). Não são excludentes, são complementares.

**P: Qual é mais importante, RF ou RNF?**  
R: Ambos são críticos. RF sem RNF = sistema que funciona mas é lento/inseguro. RNF sem RF = sistema rápido mas que não faz nada.

**P: Como não esquecer de nenhum RNF?**  
R: Crie um checklist de categorias: Performance, Segurança, Escalabilidade, Confiabilidade, Usabilidade, Compatibilidade, Manutenibilidade, Compliance.

---

**Última atualização:** 2026  
**Criado para:** Iniciantes e times em crescimento 🚀