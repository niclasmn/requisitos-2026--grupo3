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

```plantuml
@startuml
left to right direction
skinparam packageStyle rectangle
skinparam shadowing false

actor "Visitante / Parceiro" as A1
actor "Estudante Unifor" as A2
actor "Estudante Estrangeiro" as A3
actor "Docente Unifor" as A4
actor "Profissional da DRI" as A5
actor "Analista de Marketing" as A6

rectangle "Sistema PUMI (Integrado ao Portal Unifor)" {

  package "Mod 01 — Descoberta & Guias" {
    usecase "CDU01: Usar Quiz e Comparador de Destinos" as UC1
    usecase "CDU02: Consultar Editais, Instituições e Mapa" as UC2
    usecase "CDU03: Acessar Manual Estrangeiro e Contexto Fortaleza" as UC3
    usecase "CDU04: Consultar Alertas Legais de Visto e Frequência" as UC4
    usecase "CDU05: Consultar Vitrine Docente e Publicação Científica" as UC5
  }

  package "Mod 02 — Elegibilidade & Interesse" {
    usecase "CDU06: Verificar Elegibilidade Preliminar" as UC6
    usecase "CDU07: Registrar Manifestação de Interesse" as UC7
  }

  package "Mod 03 — Governança DRI & Marketing" {
    usecase "CDU08: Elaborar Rascunhos de Conteúdo e Editais" as UC8
    usecase "CDU09: Gerenciar Manifestações de Interesse" as UC9
    usecase "CDU10: Revisar e Aprovar Publicação Oficial" as UC10
  }
}

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
@enduml
```

---

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
