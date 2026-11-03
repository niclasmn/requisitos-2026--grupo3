# T193-16 Requisitos Mod de Sistemas 
_Grupo 3 | Prof. Marcelo Bezerra de Alcântara_

## 💼 Equipe:
- Nicholas Marques A.
- Diego Alexander
- Ycaro Vieira
- Charles Targino

## 🌐 Projeto Internacionalização 
-> _Desenvolvido conforme sugestões 3 e 4 do documento Propostas_Projetos_Internacionalizacao_ENADE_Unifor.docx_

```mermaid
graph TB
    %% Definição do Limite do Sistema
    subgraph PUMI [Portal Unificado de Oportunidades e Mobilidade Internacional]
        UC1((F3.1: Autenticar no Sistema))
        UC2((F1.1: Acessar Painel de Inscrições e Oportunidades))
        UC3((Administrar Convênios e Cadastrar Oportunidades))
        UC4((Analisar Trajetória e Compatibilidade de Disciplinas))
        
        %% Relacionamento de Inclusão Obrigatória
        UC2 -. "«include»" .-> UC1
        UC3 -. "«include»" .-> UC1
        UC4 -. "«include»" .-> UC1
    end

    %% Definição dos Atores
    A1["👤 Estudante Unifor<br>Mariana"]
    A2["👤 Profissional do NEI<br>Renata"]
    A3["👤 Coordenador de Curso<br>Felipe"]

    %% Conexões
    A1 ---> UC2
    A2 ---> UC3
    A3 ---> UC4

    %% Estilos
    style PUMI fill:#f9f9f9,stroke:#333,stroke-width:2px
    style UC1 fill:#d1ecf1,stroke:#0c5460,stroke-width:1px
    style UC2 fill:#d4edda,stroke:#155724,stroke-width:1px
    style UC3 fill:#fff3cd,stroke:#856404,stroke-width:1px
    style UC4 fill:#e2e3e5,stroke:#383d41,stroke-width:1px
```

```mermaid
graph TD
    %% Camada do Cliente
    subgraph CamadaCliente [Camada do Cliente]
        UI["💻 Interface de Usuário<br>Portal Web Responsivo PUMI<br>(Acessibilidade WCAG)"]
    end

    %% Camada de Aplicação
    subgraph CamadaAplicacao [Camada de Aplicação]
        Gateway["⚙️ API REST / Gateway<br>(Roteamento de Serviços)"]
        ModAuth["🔒 Componente de Controle de Acesso<br>e Autenticação por Perfil"]
        ModEstudante["🎒 Módulo de Oportunidades e Integração<br>(Busca, Filtros e Guias de Chegada)"]
        ModNEI["🏢 Módulo Administrativo do NEI<br>(Gestão de Convênios e Alertas de Prazos)"]
    end

    %% Camada de Persistência
    subgraph CamadaDados [Persistência de Dados]
        DB[("🗄️ Banco de Dados Unificado<br>de Internacionalização")]
    end

    %% Sistemas Externos
    subgraph SistemasExternos [Sistemas Externos]
        SysAcademico["🌐 Sistema Acadêmico Unifor<br>(Históricos e Créditos)"]
    end

    %% Fluxos
    UI -->|HTTPs Requests| Gateway
    Gateway --> ModAuth
    Gateway --> ModEstudante
    Gateway --> ModNEI
    
    ModAuth -.->|Valida Perfil| ModEstudante
    ModAuth -.->|Valida Perfil| ModNEI
    
    ModEstudante ---> DB
    ModNEI ---> DB
    ModNEI -.->|Consulta Trajetória| SysAcademico

    %% Estilos
    style UI fill:#ececff,stroke:#9370db,stroke-width:2px
    style Gateway fill:#fff0f5,stroke:#db7093,stroke-width:2px
    style DB fill:#e6f2ff,stroke:#0066cc,stroke-width:2px
    style SysAcademico fill:#f2f2f2,stroke:#7f7f7f,stroke-width:2px
```

```mermaid
graph TD
    %% Nós da Infraestrutura
    NodeClient["📱 Camada Cliente<br>(Navegadores / App Mobile)"]
    NodeNet["🛡️ Rede / Roteamento<br>(Load Balancer / Gateway)"]
    NodeApp["🖥️ Camada de Aplicação<br>(Servidor Aplicação Principal)"]
    NodeDB["💾 Camada de Dados<br>(Banco de Dados Principal)"]

    %% Fluxo
    NodeClient -->|1. HTTPS Seguro| NodeNet
    NodeNet -->|2. Encaminhamento Ágil| NodeApp
    NodeApp -->|3. Consulta de Elegibilidade| NodeDB

    %% Estilos
    style NodeClient fill:#e1f5fe,stroke:#0288d1,stroke-width:2px
    style NodeNet fill:#ede7f6,stroke:#5e35b1,stroke-width:2px
    style NodeApp fill:#f1f8e9,stroke:#558b2f,stroke-width:2px
    style NodeDB fill:#fff3e0,stroke:#ef6c00,stroke-width:2px
```


