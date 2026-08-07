# TCC 2026 — [Nome do Grupo]
**LTP3 + QP3 · CEMIC 2026 · Prof. Rafael Martins Alves**
           
---
   
## 👥 Integrantes        

# TCC 2026 - [Nome do Grupo]
**LTP3 + QP3 · CEMIC 2026 · Prof. Rafael**

---

## 📝 Descrição do Projeto

Nosso projeto consiste no desenvolvimento de um site dedicado à adoção de cães e gatos que necessitam de abrigo e proteção. Diante da falta de plataformas centralizadas e acessíveis para o resgate de animais de rua ou abandonados, criamos este sistema para facilitar o processo de acolhimento. O site atua em duas frentes principais: permite que protetores cadastrem animais que precisam de um lar (informando dados como foto, porte e idade) e possibilita que novos tutores naveguem pela plataforma, filtrem as buscas e iniciem o processo de adoção com segurança.

---

## 👥 Integrantes

| Nome completo | GitHub | Turma |
| :--- | :--- | :--- |
| Vitória Santana | @usuario_vitoria | [3b] |
| Sofia Abarno | @usuario_sofia | [3b] |
| Maíra Gomes | @usuario_maira | [3b] |
| Letícia Krixi | @leticiakrixis | [3b] |
| Letícia Silva | @usuario_leticia_s | [3b] |

---

## 🏗️ Diagrama de Arquitetura do Sistema

```mermaid
graph TD
    %% Estilo Geral
    classDef usuario fill:#e1f5fe,stroke:#0288d1,stroke-width:2px;
    classDef sistema fill:#fff3e0,stroke:#f57c00,stroke-width:2px;
    classDef banco fill:#e8f5e9,stroke:#388e3c,stroke-width:2px;

    %% Nós Principais
    Visitante[🌐 Visitante / Usuário]:::usuario
    
    subgraph Plataforma_Web [Site de Adoção]
        Home[📄 Tela Inicial / Home]:::sistema
        Login[🔐 Tela de Login / Cadastro]:::sistema
        PainelProtetor[🐾 Painel do Protetor<br>Cadastrar Animal]:::sistema
        PainelAdotante[❤️ Painel do Adotante<br>Buscar e Adotar]:::sistema
    end

    subgraph Servidor_e_Dados [Back-End & Banco de Dados]
        BD[(💾 Banco de Dados)]:::banco
    end

    %% Fluxo de Navegação
    Visitante -->|Acessa o site| Home
    Home -->|Quer cadastrar ou adotar| Login
    
    Login -->|Perfil: Protetor / ONG| PainelProtetor
    Login -->|Perfil: Adotante| PainelAdotante
    
    %% Ações do Protetor
    PainelProtetor -->|Insere Foto, Idade e Porte| CadPet[Formulário de Cadastro de Pets]
    CadPet -->|Salvar Dados| BD

    %% Ações do Adotante
    BD -->|Lista os Pets Disponíveis| PainelAdotante
    PainelAdotante -->|Filtra por Cão/Gato| Buscar[Buscar Animais]
    Buscar -->|Demonstra Interesse| Adotar[Iniciar Processo de Adoção]
```

---

## 🚀 Como Executar o Projeto

### 1. Requisitos Prévios
Certifique-se de ter instalado em sua máquina:
* [Git](https://git-scm.com)
* [Node.js](https://nodejs.org) (ou a tecnologia utilizada no seu Back-end)

### 2. Passo a Passo
1. Clone o repositório do projeto:
   ```bash
   git clone https://github.com
   ```
2. Acesse a pasta do projeto:
   ```bash
   cd tcc-2026-3b-equipe06-adocao-pets
   ```
3. Instale as dependências necessárias:
   ```bash
   npm install
   ```
4. Execute o comando de inicialização para rodar localmente:
   ```bash
   npm start
   ```

   atualização do conograma + relatório daatualização do tcc
