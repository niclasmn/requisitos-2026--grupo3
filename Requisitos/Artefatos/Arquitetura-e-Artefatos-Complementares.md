# Arquitetura e Artefatos Complementares — Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI)

**Instituição:** Universidade de Fortaleza (Unifor)  
**Disciplina / Contexto:** T193-16 — Requisitos e Modelagem de Sistemas  

---

## 1. Visão Arquitetural de Alto Nível

O **PUMI** é estruturado como uma aplicação web responsiva integrada ao portal institucional da **Unifor**, composta por:

* **Camada de Apresentação Web:** páginas e jornadas responsivas (*Estude Mundo Afora com a Unifor*, *Do Mundo para a Unifor*, *Docentes e Pesquisa Internacional*) e painéis administrativos (*DRI* e *Marketing*), aplicando identidade visual institucional e diretrizes WCAG.
* **Camada de Aplicação / API:** regras de negócio de filtragem, cálculo de afinidade do quiz, verificação preliminar de elegibilidade, geração de protocolo de manifestação de interesse e máquina de estados do fluxo editorial (*Rascunho* -> *Aguardando Aprovação do Marketing* -> *Publicado* / *Ajustes Solicitados* / *Arquivado*).
* **Camada de Dados Relacional:** persistência estruturada de oportunidades, instituições conveniadas, fichas de destinos, guias, curadoria docente, indicadores agregados, manifestações de interesse e trilhas de auditoria.
* **Integrações Institucionais (a validar com TI):** serviço de autenticação institucional (SSO) e canais/formulários oficiais externos de candidatura formal.

---

## 2. Diagrama de Casos de Uso e Governança (PlantUML)

flowchart LR
    %% Atores
    A1["👤 Visitante / Parceiro"]
    A2["👤 Estudante Unifor"]
    A3["👤 Estudante Estrangeiro"]
    A4["👤 Docente Unifor"]
    A5["👤 Profissional da DRI"]
    A6["👤 Analista de Marketing"]

    %% Sistema e Pacotes
    subgraph PUMI ["Sistema PUMI (Integrado ao Portal Unifor)"]
        direction TB

        subgraph Mod01 ["Mod 01 — Descoberta & Guias"]
            UC1(["CDU01: Usar Quiz e Comparador de Destinos"])
            UC2(["CDU02: Consultar Editais, Instituições e Mapa"])
            UC3(["CDU03: Acessar Manual Estrangeiro e Contexto Fortaleza"])
            UC4(["CDU04: Consultar Alertas Legais de Visto e Frequência"])
            UC5(["CDU05: Consultar Vitrine Docente e Publicação Científica"])
        end

        subgraph Mod02 ["Mod 02 — Elegibilidade & Interesse"]
            UC6(["CDU06: Verificar Elegibilidade Preliminar"])
            UC7(["CDU07: Registrar Manifestação de Interesse"])
        end

        subgraph Mod03 ["Mod 03 — Governança DRI & Marketing"]
            UC8(["CDU08: Elaborar Rascunhos de Conteúdo e Editais"])
            UC9(["CDU09: Gerenciar Manifestações de Interesse"])
            UC10(["CDU10: Revisar e Aprovar Publicação Oficial"])
        end
    end

    %% Relacionamentos
    A1 --> UC2
    A1 --> UC4

    A2 --> UC1
    A2 --> UC2
    A2 --> UC4
    A2 --> UC6
    A2 --> UC7

    A3 --> UC2
    A3 --> UC3
    A3 --> UC4

    A4 --> UC2
    A4 --> UC4
    A4 --> UC5

    A5 --> UC8
    A5 --> UC9

    A6 --> UC10

    %% Estilização opcional
    classDef actor fill:#f9f9f9,stroke:#333,stroke-width:1.5px;
    class A1,A2,A3,A4,A5,A6 actor;

## 3. Organização do Repositório de Requisitos (Padrão LAPIS)

```text
Requisitos/
├── README.md
├── Elicitacao/
│   └── Elicitacao.md
├── Especificacao de Casos de Uso/
│   ├── CDU01-usar-quiz-e-comparador-de-destinos/
│   │   └── CDU01-usar-quiz-e-comparador-de-destinos.md
│   ├── ...
│   └── CDU10-revisar-e-aprovar-publicacao-oficial/
│       └── CDU10-revisar-e-aprovar-publicacao-oficial.md
├── Especificacao de Regra de Negocio/
│   └── Especificacao-de-Regras-de-Negocio.md
├── Requisito Nao Funcionais/
│   └── Requisitos-Nao-Funcionais.md
└── Artefatos/
    └── Arquitetura-e-Artefatos-Complementares.md
```
