markdown_content = """# ☁️ Entendendo a Computação em Nuvem: IaaS, PaaS e SaaS

Aqui está uma explicação simples e direta sobre os três principais modelos de serviços em nuvem:

### 1. IaaS (Infraestrutura como Serviço)
- **O que é:** Você aluga a infraestrutura básica (servidores virtuais, armazenamento, redes) de um provedor. Você tem liberdade e controle para instalar o sistema operacional e configurar tudo do seu jeito.
- **Como entender fácil:** É como alugar um **terreno vazio**. Você tem o espaço, mas precisa construir a casa, fazer o encanamento e cuidar de quase tudo sozinho.
- **Exemplo famoso:** **Amazon EC2 (AWS)** (onde você aluga máquinas virtuais para rodar seus sistemas).

### 2. PaaS (Plataforma como Serviço)
- **O que é:** O provedor entrega a infraestrutura e o ambiente de desenvolvimento prontos. Você (geralmente um programador) só precisa se preocupar em escrever, testar e colocar o seu aplicativo no ar, sem ter que gerenciar servidores.
- **Como entender fácil:** É como alugar uma **casa pronta**. Você não precisou construir as paredes ou puxar a fiação, só precisa trazer os seus móveis (os seus códigos e dados).
- **Exemplo famoso:** **Heroku** (muito usado por desenvolvedores para hospedar aplicações de forma rápida sem configurar servidores).

### 3. SaaS (Software como Serviço)
- **O que é:** É o produto final. Você simplesmente acessa e usa um aplicativo completo pela internet (geralmente pelo navegador ou app de celular). O provedor gerencia tudo: infraestrutura, segurança, atualizações e o próprio sistema.
- **Como entender fácil:** É como ficar em um **hotel**. Tudo está pronto, limpo e funcionando. Você não constrói nem mobilia nada, apenas entra, aproveita o serviço e paga pela estadia.
- **Exemplo famoso:** **Netflix**, **Gmail** ou **Microsoft 365** (você entra, usa e não precisa se preocupar com os servidores deles).

---
> **Resumo Rápido:** 
> - **IaaS:** Você gerencia (quase) tudo. 
> - **PaaS:** Você foca apenas no seu código/aplicativo. 
> - **SaaS:** Você é apenas o usuário final aproveitando o software.
"""

with open("Modelos_Computacao_Nuvem.md", "w", encoding="utf-8") as f:
    f.write(markdown_content)

print("File generated successfully.")
