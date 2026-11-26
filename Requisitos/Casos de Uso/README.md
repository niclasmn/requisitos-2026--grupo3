# Casos de Uso — Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI)

Catálogo estruturado das especificações de **Casos de Uso (CDU)** do sistema **PUMI** (Universidade de Fortaleza — Unifor / DRI), modeladas a partir da **Visão da Demanda (v2.0)** e estruturadas conforme o template padrão **LAPIS**.

---

## Catálogo de Casos de Uso

| ID | Caso de Uso | Módulo | Ator Primário | Rastreabilidade (Func. / RN) |
| --- | --- | --- | --- | --- |
| **CDU01** (`UC1`) | [Usar Quiz e Comparador de Destinos](./CDU01-usar-quiz-e-comparador-de-destinos/CDU01-usar-quiz-e-comparador-de-destinos.md) | Mod 01 — Descoberta & Guias | Estudante Unifor | F1.2, F1.3 \| RN02, RN05 |
| **CDU02** (`UC2`) | [Consultar Editais, Instituições e Mapa](./CDU02-consultar-editais-instituicoes-e-mapa/CDU02-consultar-editais-instituicoes-e-mapa.md) | Mod 01 — Descoberta & Guias | Visitante / Usuário do Portal | F1.1, F1.4, F1.6, F2.5 \| RN01, RN02, RN05 |
| **CDU03** (`UC3`) | [Acessar Manual Estrangeiro e Contexto Fortaleza](./CDU03-acessar-manual-estrangeiro-e-contexto-fortaleza/CDU03-acessar-manual-estrangeiro-e-contexto-fortaleza.md) | Mod 01 — Descoberta & Guias | Estudante Estrangeiro | F2.2, F2.5 \| RN01, RN03, RN04, RN07 |
| **CDU04** (`UC4`) | [Consultar Alertas Legais de Visto e Frequência](./CDU04-consultar-alertas-legais-visto-e-frequencia/CDU04-consultar-alertas-legais-visto-e-frequencia.md) | Mod 01 — Descoberta & Guias | Usuário / Candidato à Mobilidade | F2.1, F2.3 \| RN01, RN03, RN04, RN05, RN07 |
| **CDU05** (`UC5`) | [Consultar Vitrine Docente e Publicação Científica](./CDU05-consultar-vitrine-docente-e-publicacao-cientifica/CDU05-consultar-vitrine-docente-e-publicacao-cientifica.md) | Mod 01 — Descoberta & Guias | Docente Unifor | F1.5, F2.5 \| RN01, RN02, RN05 |
| **CDU06** (`UC6`) | [Verificar Elegibilidade Preliminar](./CDU06-verificar-elegibilidade-preliminar/CDU06-verificar-elegibilidade-preliminar.md) | Mod 02 — Elegibilidade & Interesse | Estudante Unifor | F2.4 \| RN02, RN06 |
| **CDU07** (`UC7`) | [Registrar Manifestação de Interesse](./CDU07-registrar-manifestacao-de-interesse/CDU07-registrar-manifestacao-de-interesse.md) | Mod 02 — Elegibilidade & Interesse | Estudante Unifor | F3.1, F2.5 \| RN01, RN02, RN05 |
| **CDU08** (`UC8`) | [Elaborar Rascunhos de Conteúdo e Editais](./CDU08-elaborar-rascunhos-de-conteudo-e-editais/CDU08-elaborar-rascunhos-de-conteudo-e-editais.md) | Mod 03 — Governança DRI & Marketing | Profissional da DRI | F3.3, F3.5 \| RN01, RN02, RN03, RN04, RN05, RN07 |
| **CDU09** (`UC9`) | [Gerenciar Manifestações de Interesse](./CDU09-gerenciar-manifestacoes-de-interesse/CDU09-gerenciar-manifestacoes-de-interesse.md) | Mod 03 — Governança DRI & Marketing | Profissional da DRI | F3.2 \| RN02 |
| **CDU10** (`UC10`) | [Revisar e Aprovar Publicação Oficial](./CDU10-revisar-e-aprovar-publicacao-oficial/CDU10-revisar-e-aprovar-publicacao-oficial.md) | Mod 03 — Governança DRI & Marketing | Analista de Marketing | F3.4, F3.5 \| RN01, RN02, RN03, RN04, RN07 |

---

## Diagrama de Casos de Uso e Governança

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

## Estrutura de Pastas no Repositório

```text
├── README.md
├── CDU01-usar-quiz-e-comparador-de-destinos/
│   └── CDU01-usar-quiz-e-comparador-de-destinos.md
├── CDU02-consultar-editais-instituicoes-e-mapa/
│   └── CDU02-consultar-editais-instituicoes-e-mapa.md
├── CDU03-acessar-manual-estrangeiro-e-contexto-fortaleza/
│   └── CDU03-acessar-manual-estrangeiro-e-contexto-fortaleza.md
├── CDU04-consultar-alertas-legais-visto-e-frequencia/
│   └── CDU04-consultar-alertas-legais-visto-e-frequencia.md
├── CDU05-consultar-vitrine-docente-e-publicacao-cientifica/
│   └── CDU05-consultar-vitrine-docente-e-publicacao-cientifica.md
├── CDU06-verificar-elegibilidade-preliminar/
│   └── CDU06-verificar-elegibilidade-preliminar.md
├── CDU07-registrar-manifestacao-de-interesse/
│   └── CDU07-registrar-manifestacao-de-interesse.md
├── CDU08-elaborar-rascunhos-de-conteudo-e-editais/
│   └── CDU08-elaborar-rascunhos-de-conteudo-e-editais.md
├── CDU09-gerenciar-manifestacoes-de-interesse/
│   └── CDU09-gerenciar-manifestacoes-de-interesse.md
└── CDU10-revisar-e-aprovar-publicacao-oficial/
    └── CDU10-revisar-e-aprovar-publicacao-oficial.md
```
