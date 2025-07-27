# 🎮 Loja de Jogos - Angular E-commerce

<div align="center">
  <img src="https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white" alt="Angular">
  <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white" alt="Bootstrap">
  <img src="https://img.shields.io/badge/JSON%20Server-000000?style=for-the-badge&logo=json&logoColor=white" alt="JSON Server">
</div>

<div align="center">
  <h3>Sistema de E-commerce para Loja de Jogos desenvolvido em Angular</h3>
  <p>Aplicação completa com CRUD de produtos, consumo de API REST e interface responsiva</p>
</div>

---

## 📋 Índice

- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades](#-funcionalidades)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Pré-requisitos](#-pré-requisitos)
- [Instalação](#-instalação)
- [Como Executar](#-como-executar)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [API Endpoints](#-api-endpoints)
- [Componentes](#-componentes)
- [Screenshots](#-screenshots)
- [Contribuição](#-contribuição)
- [Licença](#-licença)

---

## 🎯 Sobre o Projeto

A **Loja de Jogos** é uma aplicação Angular desenvolvida como sistema de e-commerce especializado em jogos. O projeto implementa um sistema completo de gerenciamento de produtos com operações CRUD (Create, Read, Update, Delete), consumindo uma API REST através do JSON-Server.

### 🎨 Design e UX
- Interface moderna e responsiva com Bootstrap
- Navegação intuitiva entre as seções
- Feedback visual para todas as ações do usuário
- Layout otimizado para diferentes dispositivos

### 🏗️ Arquitetura
- Arquitetura baseada em componentes Angular
- Separação clara entre apresentação e lógica de negócios
- Services dedicados para comunicação com API
- Roteamento dinâmico para navegação SPA

---

## ⚡ Funcionalidades

### 📦 Gerenciamento de Produtos
- ✅ **Listagem de Produtos**: Visualização completa dos produtos cadastrados
- ✅ **Cadastro de Produtos**: Formulário para adição de novos produtos
- ✅ **Edição de Produtos**: Atualização de informações existentes
- ✅ **Exclusão de Produtos**: Remoção com confirmação de segurança
- ✅ **Visualização de Imagens**: Exibição de thumbnails dos produtos

### 🔧 Funcionalidades Técnicas
- ✅ **API REST**: Comunicação completa com backend JSON-Server
- ✅ **Roteamento**: Navegação SPA com Angular Router
- ✅ **Formulários Reativos**: Validação e binding bidirecional
- ✅ **Componentes Reutilizáveis**: Arquitetura modular e escalável
- ✅ **Responsividade**: Interface adaptável a diferentes telas

---

## 🛠 Tecnologias Utilizadas

### Frontend
- **[Angular](https://angular.io/)** - Framework principal
- **[TypeScript](https://www.typescriptlang.org/)** - Linguagem de programação
- **[Bootstrap 5](https://getbootstrap.com/)** - Framework CSS
- **[RxJS](https://rxjs.dev/)** - Programação reativa

### Backend/API
- **[JSON-Server](https://github.com/typicode/json-server)** - Mock API REST
- **[Node.js](https://nodejs.org/)** - Runtime JavaScript

### Ferramentas de Desenvolvimento
- **[Angular CLI](https://cli.angular.io/)** - Interface de linha de comando
- **[npm](https://www.npmjs.com/)** - Gerenciador de pacotes
- **[Git](https://git-scm.com/)** - Controle de versão

---

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter instalado:

- **Node.js** (versão 14 ou superior)
- **npm** (geralmente incluído com Node.js)
- **Git** para controle de versão
- **Angular CLI** (instalação opcional, mas recomendada)

```bash
# Verificar versões instaladas
node --version
npm --version
git --version
```

---

## 🚀 Instalação

### 1. **Clone o repositório**
```bash
git clone https://github.com/seu-usuario/loja-jogos.git
cd loja-jogos
```

### 2. **Instale as dependências**
```bash
npm install
```

### 3. **Instale dependências específicas do projeto**
```bash
# Bootstrap para estilização
npm install bootstrap

# JSON-Server para API mock (versão específica requerida)
npm install json-server@0.17
```

### 4. **Configure as imagens**
- Crie a pasta `src/assets/imagens/`
- Adicione as imagens dos produtos:
  - `jogo1.PNG`
  - `jogo2.PNG`
  - `jogo3.PNG`
  - `logo.png`

---

## ▶️ Como Executar

### Executar em Modo de Desenvolvimento

O projeto requer dois serviços rodando simultaneamente:

#### **Terminal 1 - API (JSON-Server)**
```bash
# Navegar para a pasta do projeto
cd loja-jogos

# Iniciar o servidor da API
json-server --watch db.json
```
> 🌐 API rodará em: `http://localhost:3000`

#### **Terminal 2 - Frontend (Angular)**
```bash
# Navegar para a pasta do projeto (novo terminal)
cd loja-jogos

# Iniciar o servidor de desenvolvimento
ng serve
```
> 🌐 Aplicação rodará em: `http://localhost:4200`

### 🔧 Scripts Disponíveis

```bash
# Desenvolvimento
npm start              # Inicia o servidor Angular
npm run json-server    # Inicia apenas o JSON-Server

# Build e Deploy
npm run build          # Build para produção
npm run build:prod     # Build otimizado

# Testes
npm run test           # Executa testes unitários
npm run e2e           # Executa testes end-to-end

# Linting
npm run lint          # Verifica qualidade do código
```

---

## 📁 Estrutura do Projeto

```
loja-jogos/
├── 📁 src/
│   ├── 📁 app/
│   │   ├── 📁 componentes/
│   │   │   ├── 📁 menu/                    # Componente de navegação
│   │   │   ├── 📁 rodape/                  # Componente do rodapé
│   │   │   ├── 📁 painel-principal/        # Lista de produtos
│   │   │   └── 📁 cadastro-produto/        # Formulário CRUD
│   │   ├── 📁 servicos/
│   │   │   └── 📄 produto.service.ts       # Service da API
│   │   ├── 📄 app-routing.module.ts        # Configuração de rotas
│   │   ├── 📄 app.component.ts             # Componente raiz
│   │   └── 📄 app.module.ts                # Módulo principal
│   ├── 📁 assets/
│   │   └── 📁 imagens/                     # Imagens dos produtos
│   └── 📄 styles.css                       # Estilos globais
├── 📄 db.json                              # Banco de dados JSON
├── 📄 package.json                         # Dependências do projeto
├── 📄 angular.json                         # Configurações do Angular
└── 📄 README.md                            # Documentação
```

---

## 🔌 API Endpoints

A API fornece os seguintes endpoints para gerenciamento de produtos:

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| `GET` | `/produtos` | Lista todos os produtos |
| `GET` | `/produtos/:id` | Busca produto por ID |
| `POST` | `/produtos` | Cria novo produto |
| `PUT` | `/produtos/:id` | Atualiza produto existente |
| `DELETE` | `/produtos/:id` | Remove produto |

### 📄 Exemplo de Payload (Produto)
```json
{
  "id": 1,
  "produto": "Nome do Jogo",
  "descricao": "Descrição detalhada do jogo",
  "foto": "nome-da-imagem.PNG",
  "preco": 59.99
}
```

---

## 🧩 Componentes

### 🏠 **MenuComponent**
- Barra de navegação principal
- Links para painel principal e cadastro
- Design responsivo com Bootstrap

### 📋 **PainelPrincipalComponent**
- Listagem de produtos em tabela
- Botões de ação (Editar/Excluir)
- Integração com ProdutoService

### ➕ **CadastroProdutoComponent**
- Formulário para cadastro/edição
- Validação de campos obrigatórios
- Modo dual (Create/Update)

### 🦶 **RodapeComponent**
- Informações de copyright
- Posicionamento fixo
- Estilização consistente

### ⚙️ **ProdutoService**
- Comunicação com API REST
- Métodos CRUD completos
- Gerenciamento de Observable/RxJS

---

## 📱 Screenshots

### 🏠 Painel Principal
*Listagem completa de produtos com ações disponíveis*

### ➕ Cadastro de Produto
*Formulário intuitivo para gerenciamento de produtos*

### 🔧 API em Funcionamento
*JSON-Server fornecendo dados em tempo real*

---

## 🎯 Próximas Funcionalidades

- [ ] 🛒 Carrinho de compras
- [ ] 👤 Sistema de autenticação
- [ ] 💳 Integração com gateway de pagamento
- [ ] 📊 Dashboard administrativo
- [ ] 🔍 Sistema de busca e filtros
- [ ] ⭐ Sistema de avaliações
- [ ] 📧 Notificações por email
- [ ] 🏷️ Sistema de categorias

---

## 🤝 Contribuição

Contribuições são sempre bem-vindas! Para contribuir:

1. **Fork** o projeto
2. **Crie** uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. **Commit** suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. **Push** para a branch (`git push origin feature/AmazingFeature`)
5. **Abra** um Pull Request

### 📋 Diretrizes de Contribuição
- Siga os padrões de código do projeto
- Adicione testes para novas funcionalidades
- Atualize a documentação quando necessário
- Use commits semânticos

---

## 🧪 Testes

### Executar Testes
```bash
# Testes unitários
ng test

# Testes e2e
ng e2e

# Testes com coverage
ng test --code-coverage
```

### 📊 Coverage Report
Os relatórios de cobertura são gerados na pasta `coverage/`

---

## 🚀 Deploy

### Build para Produção
```bash
ng build --prod
```

### Deploy Automático
Configure deploy automático com GitHub Actions, Netlify ou Vercel.

---

## 📞 Suporte

Se você tiver alguma dúvida ou problema:

- 📧 **Email**: seu-email@exemplo.com
- 🐛 **Issues**: [GitHub Issues](https://github.com/seu-usuario/loja-jogos/issues)
- 💬 **Discussões**: [GitHub Discussions](https://github.com/seu-usuario/loja-jogos/discussions)

---

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

## 👨‍💻 Autor

**Seu Nome**
- GitHub: [@seu-usuario](https://github.com/seu-usuario)
- LinkedIn: [Seu Perfil](https://linkedin.com/in/seu-perfil)
- Email: seu-email@exemplo.com

---

<div align="center">
  <h3>⭐ Se este projeto te ajudou, deixe uma estrela!</h3>
  <p>Desenvolvido com ❤️ e Angular</p>
  
  <img src="https://img.shields.io/github/stars/seu-usuario/loja-jogos?style=social" alt="GitHub stars">
  <img src="https://img.shields.io/github/forks/seu-usuario/loja-jogos?style=social" alt="GitHub forks">
  <img src="https://img.shields.io/github/issues/seu-usuario/loja-jogos" alt="GitHub issues">
</div>
