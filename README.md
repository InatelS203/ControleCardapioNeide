🎨 **Neides Project**  
> Um sistema para gerenciamento de cardápio e vendas em uma cantina, seguindo os princípios SOLID, a arquitetura MVC e utilizando padrões de design.

---

🚀 **Sobre o Projeto**
O Neides Project é uma aplicação web projetada para auxiliar no controle de cardápio, estoque e vendas de uma cantina. Foi desenvolvido utilizando Django, com foco em escalabilidade, organização e manutenibilidade do código.

🔑 Características principais
📋 Cadastro, atualização e exclusão de itens do cardápio.
📈 Controle de estoque dinâmico, com exibição automática de itens disponíveis.
💰 Aplicação de descontos personalizados.
🛠️ Geração de relatórios de vendas.
🌟 Projeto orientado pelos princípios SOLID, garantindo modularidade e reusabilidade.

📐 **Princípios SOLID Aplicados**

**SRP (Single Responsibility Principle)**

Cada classe tem uma responsabilidade única.
Exemplo: 'ItemController' gerencia a lógica de controle, separada da manipulação de dados nos modelos.

**OCP (Open/Closed Principle)**

As classes estão abertas para extensão, mas fechadas para modificação.
Exemplo: A classe 'Venda' pode ser estendida para incluir novos tipos de relatórios.

**LSP (Liskov Substitution Principle)**

Subclasses podem ser usadas sem alterar o comportamento do sistema.
Exemplo: Estratégias de desconto podem ser trocadas sem impactar o cálculo total.

**ISP (Interface Segregation Principle)**

Interfaces específicas garantem que classes não implementem métodos desnecessários.
Exemplo: A interface 'DiscountStrategy' define apenas o método 'applyDiscount'.

**DIP (Dependency Inversion Principle)**

Depender de abstrações e não de implementações.
Exemplo: 'ItemController' depende de abstrações como 'Item' e 'Venda'.

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
- ✅ Relatórios de vendas diários e mensais. 

---

👩‍💻 Desenvolvido por Vitória Dutra e Lucca Marcondes. ✨
