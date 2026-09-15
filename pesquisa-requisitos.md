# Requisitos Funcionais vs. Requisitos Não Funcionais

A regra de ouro para não esquecer a diferença é:
* **Funcional:** É **O QUE** o sistema faz (as funcionalidades, as ações).
* **Não Funcional:** É **COMO** o sistema faz (a qualidade, a performance, a segurança).

---

## 🛠️ Requisitos Funcionais (O QUE o sistema faz)
São as ações que o usuário pode realizar ou as regras de negócio que o aplicativo precisa executar para funcionar. Se um requisito funcional faltar, o sistema simplesmente não faz o que deveria.

**Exemplos práticos (App estilo iFood):**
1. **Cadastro e Login:** O usuário deve ser capaz de criar uma conta usando seu e-mail e senha ou fazendo login via Google/Apple.
2. **Carrinho de Compras:** O cliente deve poder adicionar, remover e alterar a quantidade de itens no seu carrinho antes de finalizar a compra.
3. **Rastreamento:** O aplicativo deve permitir que o cliente acompanhe a localização do entregador em tempo real no mapa.

---

## 🚀 Requisitos Não Funcionais (COMO o sistema faz)
São os critérios de qualidade do sistema. Eles não são uma "funcionalidade" que o usuário clica, mas garantem que a experiência seja boa, segura e rápida. Envolvem performance, segurança, escalabilidade, usabilidade, etc.

**Exemplos práticos (App estilo iFood):**
1. **Performance (Desempenho):** O aplicativo deve carregar a lista de restaurantes próximos em no máximo 2 segundos, mesmo usando internet 3G.
2. **Escalabilidade (Capacidade):** O sistema backend deve suportar picos de até 100.000 usuários acessando simultaneamente na noite de sexta-feira sem cair.
3. **Segurança:** Os dados de cartão de crédito dos clientes não devem ser salvos em texto puro no banco de dados, devendo utilizar criptografia de ponta a ponta (PCI Compliance).

---

### 💡 Dica de Sênior: A Analogia da Casa
* **Requisito Funcional:** A casa precisa ter 3 quartos, 2 banheiros e uma porta na frente.
* **Requisito Não Funcional:** A casa precisa suportar ventos de 100 km/h, ter isolamento acústico e ser construída em até 6 meses.
