🎨 **Neides Project**  
> Um sistema completo para gestão de cardápio e pedidos em uma cantina, utilizando o padrão arquitetural **MVC** e implementando **design patterns** para maior flexibilidade e organização.

---

🚀 **Sobre o Projeto**
O **Neides Project** foi desenvolvido para facilitar o controle de estoque, vendas e preços de itens de uma cantina, com foco na escalabilidade e reutilização de código. Utilizamos os princípios **SOLID**, arquitetura **MVC** e padrões de design para resolver problemas específicos.

O projeto inclui funcionalidades como:  
- 📋 Cadastro, atualização e remoção de itens do cardápio.  
- 📈 Controle de estoque em tempo real.  
- 💰 Aplicação de descontos dinâmicos.  
- 🔄 Atualização automática da interface baseada em mudanças de estoque e preços.  

---

📂 **Principais Componentes**
- **Models:** Define a lógica e a persistência dos dados, como itens do cardápio e informações de estoque.  
- **Views:** Gerencia a interface do usuário (HTML, CSS e templates Django).  
- **Controllers:** Lógica de aplicação, validação e manipulação de dados.  
- **Utils:** Funções utilitárias, como aplicação de descontos e notificações.

---

🛠️ **Tecnologias Utilizadas**
- **Linguagem:** Python 🐍  
- **Framework Web:** Django 🌐  
- **Banco de Dados:** MySQL 💾  
- **Frontend:** HTML + CSS 🎨  

---

🧩 **Padrões de Design Implementados**

1. **Observer**  
- **Objetivo:** Notificar automaticamente as **Views** (interface do usuário) sobre mudanças no **Model** (dados).  
- **Aplicação:**  
  - Sempre que o estoque ou preço de um item muda, a interface é atualizada automaticamente.  
  - Exemplo: Atualização de cardápio em tempo real.  

2. **Singleton**  
- **Objetivo:** Garantir que apenas uma instância de certas classes (como conexão com o banco de dados) exista.  
- **Aplicação:**  
  - A classe de conexão com o banco (`DatabaseConnection`) é um Singleton.  
  - Exemplo: A mesma conexão é compartilhada entre controladores para otimizar recursos.  

3. **Strategy**  
- **Objetivo:** Permitir diferentes comportamentos para o cálculo de descontos dinamicamente.  
- **Aplicação:**  
  - Implementação de estratégias como `DescontoFixo` e `DescontoPercentual`.  
  - Exemplo: Aplicar descontos diferentes para estudantes ou clientes regulares.

---
🏗️ **Como Rodar o Projeto**

1️⃣ **Pré-requisitos**  
- Python 3.9+  
- MySQL  
- Django 4+  


2️⃣ **Passos de Configuração**  

1. **Clone o repositório**  
   ```bash
   git clone https://github.com/InatelS203/ControleCardapioNeide.git
   cd neides_project
   ```

2. **Crie o ambiente virtual**  
   ```bash
   python -m venv venv
   source venv/bin/activate  # No Windows: venv\Scripts\activate
   ```

3. **Instale as dependências**  
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure o banco de dados**  
   - Crie um banco de dados no MySQL.  
   - Atualize as credenciais no arquivo `settings.py`.  

5. **Execute as migrações**  
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

6. **Inicie o servidor local**  
   ```bash
   python manage.py runserver
   ```

---

## 📌 **Funcionalidades Planejadas**
- ✅ Cadastro de novos itens no cardápio.  
- ✅ Controle de estoque e exibição de itens disponíveis.  
- ✅ Atualização de preços e quantidades.  
- 🚧 Relatórios de vendas diários e mensais (em andamento).  
- 🚧 Notificações para reabastecimento de estoque (em andamento).  

---

👩‍💻 Desenvolvido por Vitória Dutra e Lucca Marcondes. ✨
