✔ README.md — CyberShield + Cypress
# 🛡️ CyberShield – Sistema com Login, Cadastro e Testes E2E (Cypress)

Este projeto implementa um sistema fictício de proteção digital chamado **CyberShield**, contendo:

- Tela de **Login**
- Tela de **Cadastro**
- Navegação entre abas
- Área protegida com:
  - Verificação de ameaças
  - Backup de arquivos
  - Recuperação de arquivos
  - Perfil do usuário

Além disso, foi implementada uma suíte completa de **testes automatizados com Cypress**, validando todas as funcionalidades principais do sistema.

---

## 📁 Estrutura do Projeto



/cypress
/e2e
login.cy.js
cadastro.cy.js
navegacao.cy.js
logout.cy.js
index.html
script.js
style.css
README.md


---

## 🚀 Como Rodar o Projeto

### 1️⃣ Instalar dependências
Dentro da pasta do projeto, execute:

```sh
npm init -y


Depois instale o Cypress:

npm install cypress --save-dev

2️⃣ Abrir o Cypress
npx cypress open


O Cypress irá abrir a interface para que você escolha e execute os testes.

3️⃣ Rodar o projeto localmente (caso necessário)

Como arquivos .html abertos diretamente podem bloquear algumas funções do Cypress, é recomendado rodar um servidor local simples:

npx http-server .


Depois, ajuste o cy.visit() nos testes, se preferir:

cy.visit("http://localhost:8080/index.html");

🧪 Testes Automatizados

A suíte de testes foi separada por funcionalidades:

✔ 1. login.cy.js

Validações:

Campos vazios não devem permitir login

E-mail inválido deve ser rejeitado

Login com senha errada deve falhar

Login correto deve liberar o painel protegido

O teste cria um usuário no localStorage antes de cada execução, garantindo funcionamento consistente.

✔ 2. cadastro.cy.js

Testes garantem que:

Campos obrigatórios sejam validados

E-mail inválido seja rejeitado

Cadastro válido salve o usuário e volte à tela de login

✔ 3. navegacao.cy.js

Após login automático, valida:

A troca correta entre as abas:

Início

Proteção

Backup

Recuperação

Perfil

✔ 4. logout.cy.js

Verifica que o botão “Sair”:

Oculta o conteúdo protegido

Retorna para a tela de login

💾 Tecnologias Utilizadas

HTML5

CSS3

JavaScript

LocalStorage

Cypress 12+

📌 Requisitos para funcionamento

Node.js instalado

NPM atualizado

Cypress instalado localmente

🙋‍♀️ Autora / Autor

Projeto desenvolvido para fins acadêmicos, estudo e prática de:

Testes E2E

Automatização

Design de interface

Desenvolvimento web front-end

✨ Melhorias Futuras (opcional)

Adicionar API real para autenticação

Criar dashboard mais completo

Substituir alert() por componentes visuais

Criar testes de backup e recuperação com mocks
