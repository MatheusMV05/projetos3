# Site Institucional BRASFI

[![GitHub stars](https://img.shields.io/github/stars/brasfi/site-institucional?style=social)](https://github.com/brasfi/site-institucional/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/brasfi/site-institucional?style=social)](https://github.com/brasfi/site-institucional/network/members)
[![GitHub issues](https://img.shields.io/github/issues/brasfi/site-institucional)](https://github.com/brasfi/site-institucional/issues)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/brasfi/site-institucional)](https://github.com/brasfi/site-institucional/pulls)
[![GitHub last commit](https://img.shields.io/github/last-commit/brasfi/site-institucional)](https://github.com/brasfi/site-institucional/commits/main)
[![GitHub contributors](https://img.shields.io/github/contributors/brasfi/site-institucional)](https://github.com/brasfi/site-institucional/graphs/contributors)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📋 Sobre o Projeto

O Site Institucional da BRASFI (Aliança Brasileira de Finanças e Investimentos Sustentáveis) é uma plataforma web moderna, responsiva e de alto desempenho desenvolvida para consolidar a presença digital da organização, facilitar a comunicação com stakeholders e divulgar iniciativas e eventos relacionados a finanças sustentáveis.

### 🎯 Objetivos

- Fortalecer a identidade institucional da BRASFI no ambiente digital
- Disponibilizar conteúdo relevante sobre finanças e investimentos sustentáveis
- Divulgar eventos, iniciativas e parcerias da organização
- Facilitar o contato entre a BRASFI e diferentes públicos de interesse
- Oferecer uma experiência de navegação otimizada em qualquer dispositivo

## 🏗️ Arquitetura

O projeto utiliza uma **arquitetura desacoplada**, seguindo o padrão MVC com API RESTful:

- **Back-end**: API REST desenvolvida com Spring Boot 3.x
- **Front-end**: Aplicação SPA (Single Page Application) construída com React
- **Banco de Dados**: PostgreSQL
- **Autenticação**: JWT (implementada para áreas restritas)
- **Infraestrutura**: Microsoft Azure (App Service, Database for PostgreSQL e Static Web Apps)

## 🚀 Tecnologias

### Back-end (Spring Boot 3.x)

- **Spring Boot Web**: Framework para criação da API REST
- **Spring Data JPA**: Camada de persistência e acesso a dados
- **PostgreSQL**: Sistema de gerenciamento de banco de dados relacional
- **Spring Security + JWT**: Implementação de autenticação e autorização
- **Lombok**: Biblioteca para redução de código boilerplate
- **Validation**: Validação robusta de dados de entrada
- **Spring Mail**: Serviço para envio de e-mails a partir de formulários
- **SpringDoc OpenAPI (Swagger)**: Documentação automática da API

### Front-end (React + Tailwind)

- **React.js**: Biblioteca JavaScript para construção de interfaces
- **React Router**: Gerenciamento de rotas e navegação
- **Axios**: Cliente HTTP para comunicação com a API
- **TailwindCSS**: Framework CSS para estilização
- **Formik + Yup**: Gerenciamento e validação de formulários
- **React Hook Form**: Biblioteca para criação de formulários dinâmicos
- **Framer Motion**: Biblioteca para animações de interface

## 📦 Estrutura do Projeto

### Back-end

```
backend/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── brasfi/
│   │   │           └── site_institucional/
│   │   │               ├── config/        # Configurações (Spring Security, CORS, etc.)
│   │   │               ├── controller/    # Controladores REST
│   │   │               ├── dto/           # Objetos de Transferência de Dados
│   │   │               ├── exception/     # Tratamento global de exceções
│   │   │               ├── model/         # Entidades JPA
│   │   │               ├── repository/    # Interfaces de repositório
│   │   │               ├── security/      # Implementação de segurança (JWT)
│   │   │               ├── service/       # Lógica de negócio
│   │   │               └── Application.java
│   │   └── resources/
│   │       ├── application.properties # Configurações da aplicação
│   │       └── static/                # Recursos estáticos
│   └── test/                          # Testes unitários e de integração
├── pom.xml                            # Dependências Maven
└── README.md
```
## Diagrama de classes SR1

![SR1](https://via.placeholder.com/800x400?text=SR1)
### Front-end

```
frontend/
├── public/                # Arquivos públicos
├── src/
│   ├── assets/            # Imagens, fontes, etc.
│   ├── components/        # Componentes reutilizáveis
│   │   ├── common/        # Componentes genéricos (botões, cards, etc.)
│   │   └── layout/        # Componentes de layout (header, footer, etc.)
│   ├── contexts/          # Contextos React (auth, theme, etc.)
│   ├── hooks/             # Custom hooks
│   ├── pages/             # Páginas da aplicação
│   ├── services/          # Serviços para comunicação com a API
│   ├── styles/            # Estilos globais
│   ├── utils/             # Funções utilitárias
│   ├── App.js             # Componente principal
│   ├── index.js           # Ponto de entrada
│   └── routes.js          # Configuração de rotas
├── .env                   # Variáveis de ambiente
├── package.json           # Dependências NPM
├── tailwind.config.js     # Configuração do Tailwind
└── README.md
```

## 📝 Funcionalidades

### MVP (Versão Inicial)

- **Home**: Apresentação institucional com destaques principais
- **Sobre Nós**: História, missão, visão e valores da BRASFI
- **Eventos & Iniciativas**: Listagem e detalhes de eventos passados e futuros
- **Blog/Notícias**: Sistema de publicação e visualização de conteúdos
- **Contato**: Formulário de contato com envio de e-mail
- **Parceiros**: Exibição de organizações parceiras com seus respectivos logos
- **Área Restrita para Membros**: Dashboard com conteúdo exclusivo

### Funcionalidades Futuras (Pós-MVP)

- **Cadastro para Newsletter**: Sistema de inscrição para recebimento de informativos
- **Sistema de Comentários**: Possibilidade de interação nos artigos do blog
- **Multilíngue**: Suporte para português e inglês
- **Analytics**: Integração com ferramentas de análise de tráfego

## 🔒 Segurança

O projeto implementa várias camadas de segurança:

- **CORS configurado**: Restrição de acesso à API por domínios não autorizados
- **Proteção contra SQL Injection**: Uso de PreparedStatements via Spring Data JPA
- **Tratamento Global de Exceções**: Implementação de ExceptionHandler centralizado
- **Validação de Entrada**: Validação robusta de todos os dados recebidos
- **Armazenamento Seguro de Senhas**: Utilização de algoritmo BCrypt
- **JWT**: Tokens seguros com tempo de expiração para autenticação

## 🚢 Deploy

### Infraestrutura Azure

O projeto é hospedado na infraestrutura Microsoft Azure:

1. **Azure App Service**: Hospedagem do back-end Spring Boot
2. **Azure Database for PostgreSQL**: Serviço gerenciado para o banco de dados
3. **Azure Static Web Apps**: Hospedagem do front-end React

### Pipeline de Implantação

A implantação utiliza GitHub Actions para CI/CD:

1. Commit realizado na branch principal (`main`)
2. GitHub Actions executa:
   - Testes automatizados
   - Build do projeto
   - Deploy no ambiente Azure

## 📊 Estatísticas do Repositório

[![Gráfico de Contribuições](https://github-readme-activity-graph.vercel.app/graph?username=brasfi&theme=minimal&area=true&hide_border=true)](https://github.com/brasfi/site-institucional)

![Estatísticas do Repositório](https://github-readme-stats.vercel.app/api/pin/?username=brasfi&repo=site-institucional&theme=vue)

## 📄 Licença

Este projeto está licenciado sob a [Licença MIT](LICENSE).

## 📞 Contato

Para mais informações sobre o projeto, entre em contato com a equipe de desenvolvimento:

- Email: studioryb.contato@gmail.com

---

Desenvolvido com ❤️ para a Aliança Brasileira de Finanças e Investimentos Sustentáveis (BRASFI)
