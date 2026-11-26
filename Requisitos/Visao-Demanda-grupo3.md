# Visão da Demanda (VD)

## Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI)

**Instituição:** Universidade de Fortaleza (Unifor)  
**Disciplina / Contexto:** T193-16 — Requisitos e Modelagem de Sistemas  
**Metodologia de Desenvolvimento:** Scrum  

---

## Histórico de Versões

| Data | Versão | Descrição | Autor |
|---|---:|---|---|
| 29/10/2026 | 1.0 | Criação inicial da visão da demanda do PUMI. | Equipe 3 — Nicholas |
| 01/11/2026 | 1.1 | Revisão da visão, consolidação das frentes de Gestão de Oportunidades e Portal de Internacionalização e delimitação para MVP Scrum. | Equipe 3 |
| 10/11/2026 | 1.2 | Ajuste de perfis de acesso, funcionalidades, diagramas e histórias de usuário. | Equipe 3 |
| 23/11/2026 | 2.0 | **Revisão pós-entrevista com Stakeholder (DRI):** adequação à governança do Marketing, conformidade estrita com LGPD e regras de imigração/frequência (75%), integração ao ecossistema Unifor (sem site externo), inclusão de mobilidade docente/*web impact*, quiz interativo de destinos e guia de contexto local em Fortaleza. | Equipe 3 |

> **Nota de Elaboração:** Esta versão consolida os requisitos levantados na entrevista com a gestão da Diretoria de Relações Internacionais (DRI) da Unifor. Regras legais (imigração/visto e LGPD), normas acadêmicas (frequência mínima) e fluxos institucionais (aprovação pelo Marketing) refletem diretrizes obrigatórias da instituição. Detalhes operacionais específicos (como nota mínima de PMG por edital e integração técnica de SSO) permanecem sujeitos à validação final com a DRI e a equipe de TI.

---

## 1. Objetivo

Definir a visão, a proposta de valor, o escopo e os requisitos do **Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI)**, concebido como um **módulo de expansão integrado ao ambiente digital oficial da Unifor e da Diretoria de Relações Internacionais (DRI)** — e não como um site externo separado.

O papel do sistema é **centralizar orientações práticas, facilitar a descoberta de destinos e oportunidades acadêmicas (discentes e docentes), impulsionar a visibilidade científica internacional (*web impact*) e organizar o contato inicial com a DRI**, respeitando rigorosamente as diretrizes visuais e editoriais do **Departamento de Marketing**, a **Lei Geral de Proteção de Dados (LGPD)** e as normas legais de imigração e ensino superior.

---

## 2. Proposta de Valor

### 2.1. Visão

Ser a extensão digital oficial, confiável e integrada da internacionalização da Unifor: um ambiente orientativo onde estudantes da instituição, docentes e candidatos estrangeiros encontrem caminhos claros para **estudar e pesquisar no exterior**, **vivenciar a Unifor em Fortaleza** e **fortalecer o impacto internacional (*web impact*) da Universidade**.

### 2.2. Proposta de Valor para a DRI e para a Instituição

O PUMI estrutura-se em três frentes estratégicas alinhadas à atuação real da DRI:

1. **Descoberta Inteligente e Apoio à Decisão (Mobilidade de Saída):** organiza editais (próprios e de parceiros como Santander), prazos com antecedência necessária para trâmites consulares e um **Quiz/Assistente Interativo de Afinidade**, permitindo comparar países, cidades, custo de manutenção, cultura e prós/contras.
2. **Acolhimento e Contexto Local (Mobilidade de Entrada):** oferece ao estudante estrangeiro um manual prático sobre disciplinas ofertadas em inglês/outros idiomas, bairros, moradia, custo de vida e localização estratégica da Unifor em Fortaleza (proximidade com praias, shoppings, bancos e comércio).
3. **Visibilidade Acadêmica e Mobilidade Docente (*Web Impact*):** cria uma vitrine institucional para cooperação e intercâmbio de professores, apoiando a divulgação e o monitoramento de oportunidades de publicação científica internacional em periódicos qualificados e sem custos proibitivos.

**Valor entregue à DRI e à Unifor:**
* **Redução do atendimento repetitivo ("boca a boca" e e-mails básicos):** centralização de orientações de pré-chegada, moradia, documentação, custos e funcionamento acadêmico.
* **Mitigação de riscos legais e acadêmicos:** alertas claros sobre a obrigatoriedade do **visto de estudante** (evitando tentativas de matrícula apenas com passaporte/turismo e penalidades junto à Polícia Federal e MEC) e sobre a regra inegociável de **75% de frequência mínima**.
* **Conformidade com a governança institucional:** fluxo administrativo desenhado para que a DRI prepare conteúdos e submeta ao crivo visual, textual e de imagem do Departamento de Marketing.
* **Projeção internacional com privacidade:** divulgação de métricas agregadas de mobilidade e produção científica internacional sem expor dados pessoais de alunos (LGPD).

---

## 3. Descrição da Demanda

A solução consiste em uma aplicação web responsiva integrada à estrutura oficial da Unifor, organizada por jornadas de público e sustentada por um **fluxo administrativo com governança de aprovação**.

### 3.1. Públicos e Jornadas Principais

* **Estude mundo afora com a Unifor (Estudantes da Unifor):** consultam instituições conveniadas, utilizam o **Quiz Interativo de Destinos**, comparam custos de manutenção e cultura, verificam elegibilidade preliminar, recebem alertas sobre prazos de visto/consulado e registram manifestação de interesse.
* **Do mundo para a Unifor (Estudantes Estrangeiros):** acessam orientações essenciais em inglês sobre candidatura, obrigatoriedade de visto de estudante, disciplinas ofertadas em outros idiomas, regra de 75% de frequência e o **Guia de Vida em Fortaleza**.
* **Docentes e Pesquisa Internacional (*Web Impact*):** professores da Unifor consultam programas de mobilidade docente, redes de cooperação e orientações/vitrines sobre revistas científicas internacionais recomendadas.
* **Gestão e Governança de Conteúdo (DRI + Marketing):** profissionais da DRI elaboram e atualizam minutas de editais, guias e indicadores agregados em ambiente administrativo, submetendo-os à revisão e publicação oficial pelo **Departamento de Marketing**.

### 3.2. Módulos do Produto

| Módulo | Finalidade | Principais Recursos |
|---|---|---|
| **Portal Integrado Unifor** | Apresentar as jornadas da DRI dentro da estrutura e identidade visual da Unifor. | Página inicial integrada, navegação por público (Estudante Unifor, Estrangeiro, Docente) e indicadores estatísticos agregados (sem nomes individuais). |
| **Quiz & Comparador de Destinos** | Apoiar o aluno da Unifor na escolha do país/cidade ideal antes do edital. | Assistente interativo tipo teste vocacional/afinidade e fichas comparativas (custo de manutenção, idioma, cultura, prós e contras). |
| **Catálogo de Oportunidades e Instituições** | Centralizar editais vigentes e instituições conveniadas. | Filtros por modalidade, país, público (discente/docente) e situação; mapa-múndi simplificado e lista pesquisável. |
| **Guia de Mobilidade e Alertas Legais** | Prevenir erros críticos de documentação e adaptação acadêmica. | Alertas destacados sobre **Visto de Estudante vs. Passaporte**, prazos de envio a consulados, exigência de **75% de frequência**, aproveitamento de disciplinas e seguros. |
| **Manual do Estrangeiro & Fortaleza** | Facilitar a chegada e adaptação de alunos internacionais. | Lista de disciplinas em inglês/outros idiomas, guia de bairros próximos à Unifor, moradia, custo de vida, praias, shoppings, bancos e lojas. |
| **Vitrine Docente & Publicação Científica** | Fomentar a internacionalização docente e o *web impact* da Unifor. | Divulgação de programas para professores, parcerias de pesquisa e curadoria de revistas científicas internacionais qualificadas e sem custos proibitivos. |
| **Interesse e Atendimento** | Organizar o primeiro contato e reduzir demandas repetitivas. | Registro simplificado de interesse com protocolo, triagem inicial e direcionamento aos canais oficiais de candidatura. |
| **Fluxo Administrativo e Governança** | Permitir que a DRI mantenha propostas de conteúdo organizadas sob supervisão do Marketing. | Criação e edição de rascunhos pela DRI com status de **"Aguardando Aprovação do Marketing"** antes da publicação no ar. |

### 3.3. Diretrizes de Experiência, Governança e Conformidade

* **Integração Institucional (Sem Site Isolado):** O PUMI não operará como site externo paralelo; deverá integrar-se ao ambiente web da Unifor e seguir rigorosamente o guia de marca vigente.
* **Governança de Publicação (Crivo do Marketing):** A DRI não publica nem remove conteúdos diretamente no site oficial sem aprovação. O painel administrativo modela o fluxo de preparação pela DRI e validação/publicação pelo Departamento de Marketing.
* **Conformidade Estrita com a LGPD:** É proibida a exibição pública de nomes, matrículas ou dados individuais de estudantes em intercâmbio. O portal exibirá apenas **dados quantitativos agregados** (ex.: quantidade de alunos recebidos/enviados por período ou país).
* **Separação entre Regra Legal Inegociável e Flexibilidade Acadêmica:** O sistema deve deixar explícito que normas legais e institucionais — como **visto de estudante para matrícula** e **75% de frequência mínima** — não são negociáveis, enquanto questões acadêmicas específicas (como cursar disciplina de outro curso) podem ser avaliadas caso a caso.
* **Tradução Estratégica Priorizada:** Devido aos custos de tradução e manutenção, o portal não assumirá tradução 100% irrestrita de todo o conteúdo interno, priorizando a versão em inglês nas páginas essenciais para estrangeiros, manuais de chegada e apresentação institucional.

---

## 4. Partes Interessadas

| Parte Interessada | Papel no Projeto | Necessidades e Responsabilidades |
|---|---|---|
| **Diretoria de Relações Internacionais (DRI)** | Stakeholder principal e área de negócio | Definir regras de mobilidade discente e docente; elaborar rascunhos de editais, guias e comparativos; acompanhar manifestações de interesse; consolidar indicadores agregados. |
| **Departamento de Marketing (Unifor)** | Stakeholder de governança e aprovação | Validar identidade visual, qualidade textual, imagens e riscos institucionais; aprovar e efetivar a publicação de conteúdos no ecossistema oficial da Unifor. |
| **Estudantes da Unifor** | Usuários finais (Mobilidade de Saída) | Descobrir destinos compatíveis (via quiz e comparativos), entender custos, prazos consulares e requisitos acadêmicos, verificar elegibilidade e registrar interesse. |
| **Estudantes Estrangeiros** | Usuários finais (Mobilidade de Entrada) | Consultar conteúdos essenciais em inglês sobre visto de estudante, disciplinas em outros idiomas, frequência de 75% e vida em Fortaleza (moradia e proximidades). |
| **Docentes da Unifor** | Usuários finais (Cooperação e Pesquisa) | Acessar oportunidades de intercâmbio docente, parcerias internacionais e informações sobre periódicos científicos para elevar o *web impact* institucional. |
| **Equipe de TI / Infraestrutura Unifor** | Stakeholder técnico | Orientar integração com o portal institucional, hospedagem, autenticação (SSO), segurança e conformidade LGPD. |
| **Equipe de Desenvolvimento (Equipe 3)** | Equipe de projeto | Levantar e modelar requisitos, priorizar backlog, desenvolver o MVP alinhado às restrições institucionais e validar incrementos. |

---

## 5. Personas

### 5.1. Lucas — Estudante da Unifor (Mobilidade de Saída)
* **Descrição:** Estudante de graduação interessado em intercâmbio, mas indeciso sobre qual país escolher e desinformado sobre custos de manutenção e trâmites consulares.
* **Objetivos:** Descobrir destinos alinhados ao seu perfil, comparar custo de vida e cultura, verificar elegibilidade preliminar e organizar prazos com antecedência.
* **Dores:** Dúvida entre países; confusão entre passaporte e visto de estudante; desconhecimento sobre prazos de envio de documentos a consulados.
* **Necessidades no PUMI:** Quiz interativo de afinidade, fichas comparativas de destinos, alertas de vistos/prazos e verificador preliminar de elegibilidade.

### 5.2. Claire — Estudante Estrangeira (Mobilidade de Entrada)
* **Descrição:** Universitária estrangeira que deseja realizar mobilidade acadêmica na Unifor em Fortaleza.
* **Objetivos:** Entender em inglês como funciona a candidatura, quais disciplinas são ofertadas fora do português, onde morar perto do campus e quais regras acadêmicas e migratórias precisa cumprir.
* **Dores:** Falta de informações práticas sobre bairros, moradia e entorno da Unifor; risco de viajar sem o visto de estudante adequado ou estranhar a exigência de 75% de frequência.
* **Necessidades no PUMI:** Manual do estrangeiro em inglês, guia de localização/moradia em Fortaleza e alertas claros sobre visto obrigatório e 75% de frequência.

### 5.3. Camila — Profissional da DRI
* **Descrição:** Analista da DRI que atende dúvidas de alunos e docentes, organiza editais e prepara comunicações institucionais.
* **Objetivos:** Reduzir o volume de e-mails repetitivos sobre dúvidas básicas, manter minutas de editais e guias organizadas e submeter atualizações ao Marketing com agilidade.
* **Dores:** Retrabalho respondendo às mesmas perguntas sobre moradia, vistos e prazos; necessidade de alinhar publicações ao fluxo de aprovação do Marketing sem expor dados pessoais (LGPD).
* **Necessidades no PUMI:** Ambiente de gestão de rascunhos com fluxo de aprovação para o Marketing, centralização de guias FAQ e painel de manifestações de interesse.

### 5.4. Prof. Roberto — Docente da Unifor
* **Descrição:** Professor pesquisador interessado em cooperação internacional, intercâmbio docente e publicação de artigos no exterior.
* **Objetivos:** Encontrar oportunidades de mobilidade para docentes e identificar periódicos científicos internacionais qualificados sem custos proibitivos.
* **Dores:** Falta de visibilidade centralizada sobre ações voltadas a docentes e dificuldade para mapear revistas recomendadas que contribuam para o *web impact* da Unifor.
* **Necessidades no PUMI:** Vitrine dedicada à mobilidade docente, parcerias de pesquisa e curadoria de periódicos internacionais.

### 5.5. Mariana — Analista de Marketing da Unifor
* **Descrição:** Profissional responsável por zelar pela identidade visual, qualidade textual e segurança institucional dos canais digitais da Unifor.
* **Objetivos:** Garantir que toda página, edital ou guia publicado pela DRI siga os padrões gráficos da Unifor, não contenha erros ou riscos de imagem e respeite a LGPD.
* **Dores:** Publicações despadronizadas ou sem revisão editorial prévia.
* **Necessidades no PUMI:** Fila de revisão e aprovação editorial onde possa validar, solicitar ajustes ou aprovar a publicação dos conteúdos submetidos pela DRI.

---

## 6. Necessidades e Funcionalidades

### Necessidade 1 — Descobrir destinos, oportunidades e visibilidade internacional

| ID | Funcionalidade | Descrição | Escopo | Atores | Valor |
|---|---|---|---|---|---|
| F1.1 | Portal integrado por jornadas | Apresentar o PUMI dentro do ecossistema Unifor, direcionando para *Estude Mundo Afora*, *Do Mundo para a Unifor* e *Mobilidade Docente*. | Incluída | Todos os visitantes | Alto |
| F1.2 | Quiz / Assistente interativo de destinos | Questionário de afinidade (orçamento, idioma, objetivos, cultura) que sugere destinos e instituições conveniadas compatíveis. | Incluída | Estudante Unifor | Alto |
| F1.3 | Fichas comparativas de destinos | Exibir país, cidade, custo estimado de manutenção, idioma, cultura e prós/contras para apoio à decisão. | Incluída | Estudante Unifor, visitante | Alto |
| F1.4 | Catálogo de oportunidades e mapa | Listar editais (próprios e parceiros como Santander) com filtros por público (discente/docente), país e prazo, além de mapa-múndi simplificado. | Incluída | Estudante Unifor, docente, visitante | Alto |
| F1.5 | Vitrine docente e publicação científica | Disponibilizar seção para mobilidade de professores, cooperação e curadoria de revistas científicas internacionais de qualidade e custo acessível (*web impact*). | Incluída | Docente Unifor | Alto |
| F1.6 | Indicadores agregados (LGPD) | Exibir estatísticas consolidadas de mobilidade (ex.: total de intercambistas por período/região), sem exibir nomes ou dados pessoais. | Incluída | Todos os visitantes | Médio |

### Necessidade 2 — Orientar sobre regras legais, acadêmicas e contexto local

| ID | Funcionalidade | Descrição | Escopo | Atores | Valor |
|---|---|---|---|---|---|
| F2.1 | Guia de saída e alertas consulares | Reunir orientações sobre documentos, proficiência, seguros e alertas destacados sobre **diferença entre passaporte e visto de estudante** e prazos de envio a consulados. | Incluída | Estudante Unifor, docente | Alto |
| F2.2 | Manual do estrangeiro e contexto Fortaleza | Guia em inglês com disciplinas ofertadas em inglês/outros idiomas, bairros próximos à Unifor, moradia, custo de vida e proximidades (praias, shoppings, bancos, lojas). | Incluída | Estudante estrangeiro | Alto |
| F2.3 | Quadro de regras inegociáveis vs. flexibilidades | Destacar obrigatoriedade de **visto de estudante para matrícula** e **75% de frequência mínima**, diferenciando de flexibilidades acadêmicas sujeitas a análise. | Incluída | Estudante estrangeiro, estudante Unifor | Alto |
| F2.4 | Verificação preliminar de elegibilidade | Permitir autodeclaração de critérios acadêmicos (como PMG) para comparação orientativa com os requisitos cadastrados no edital. | Incluída | Estudante Unifor | Alto |
| F2.5 | Direcionamento para candidatura oficial | Apresentar links e instruções dos canais oficiais de inscrição (internos ou de parceiros). | Incluída | Estudante Unifor, estrangeiro, docente | Alto |

### Necessidade 3 — Registrar interesse e governar publicações (DRI + Marketing)

| ID | Funcionalidade | Descrição | Escopo | Atores | Valor |
|---|---|---|---|---|---|
| F3.1 | Manifestação simplificada de interesse | Permitir que estudante autenticado registre interesse em uma oportunidade, gerando protocolo e exibindo aviso de que não equivale à candidatura oficial. | Incluída | Estudante Unifor | Alto |
| F3.2 | Gestão de manifestações pela DRI | Listar registros de interesse por oportunidade e atualizar status de atendimento (“Recebida”, “Em orientação”, “Concluída”, “Cancelada”). | Incluída | Profissional da DRI | Alto |
| F3.3 | Gestão de rascunhos pela DRI | Permitir que a DRI crie e edite minutas de oportunidades, fichas de destinos, guias e indicadores agregados, submetendo-as para revisão. | Incluída | Profissional da DRI | Alto |
| F3.4 | Fluxo de aprovação e publicação (Marketing) | Permitir que o Marketing revise conteúdos submetidos pela DRI, solicite ajustes ou aprove a publicação oficial no portal. | Incluída | Analista de Marketing | Alto |
| F3.5 | Gestão de tradução estratégica | Permitir vincular versões em inglês aos conteúdos prioritários (jornada de entrada, manuais e apresentação institucional). | Incluída | Profissional da DRI, Marketing | Alto |

---

## 7. Regras de Negócio

| ID | Regra | Descrição |
|---|---|---|
| **RN01** | **Governança de Publicação (Marketing)** | Nenhum conteúdo criado ou alterado pela DRI pode ser publicado diretamente no ambiente público sem passar pelo status de aprovação do Departamento de Marketing. |
| **RN02** | **Privacidade e Anonimização (LGPD)** | É estritamente proibida a divulgação pública de nomes, matrículas, fotos não autorizadas ou dados individuais de intercambistas; apenas estatísticas agregadas são permitidas. |
| **RN03** | **Obrigatoriedade de Visto de Estudante** | Todo conteúdo voltado à mobilidade de entrada deve alertar que a matrícula na Unifor exige **visto de estudante válido**, sendo ilegal a matrícula apenas com passaporte/visto de turismo. |
| **RN04** | **Frequência Mínima Inegociável** | Os guias acadêmicos devem explicitar que a aprovação nas disciplinas da Unifor exige, além de nota, **frequência mínima de 75%**, sem exceções. |
| **RN05** | **Antecedência Consular e Prazos** | Editais e cronogramas devem destacar a antecedência necessária para emissão de carta de aceite, envio de passaporte/documentos a consulados, passagens e seguro-viagem. |
| **RN06** | **Caráter Orientativo da Elegibilidade** | A verificação preliminar de elegibilidade (ex.: PMG) não garante aprovação nem substitui a conferência documental oficial da DRI. |
| **RN07** | **Escopo Viável de Idiomas** | O idioma inglês é obrigatório nos conteúdos essenciais destinados ao público internacional (guia de entrada, regras legais, contexto local e visão institucional), sem exigir tradução integral de documentos internos extensos. |

---

## 8. Arquitetura e Diagramas

### 8.1. Diagrama de Casos de Uso e Governança

```mermaid
flowchart LR
    subgraph Perfis["👥 Perfis de Acesso"]
        direction TB
        A1[Visitante / Parceiro]
        A2[Estudante Unifor]
        A3[Estudante Estrangeiro]
        A4[Docente Unifor]
        A5[Profissional da DRI]
        A6[Analista de Marketing]
    end

    subgraph Modulos["📦 Sistema PUMI (Integrado ao Portal Unifor)"]
        direction TB
        
        subgraph M1["Mod 01 — Descoberta & Guias"]
            UC1([Usar Quiz & Comparador de Destinos])
            UC2([Consultar Editais, Instituições & Mapa])
            UC3([Acessar Manual Estrangeiro & Contexto Fortaleza])
            UC4([Consultar Alertas Legais: Visto & 75% Frequência])
            UC5([Consultar Vitrine Docente & Web Impact])
        end

        subgraph M2["Mod 02 — Elegibilidade & Interesse"]
            UC6([Verificar Elegibilidade Preliminar])
            UC7([Registrar Manifestação de Interesse])
        end

        subgraph M3["Mod 03 — Governança DRI & Marketing"]
            UC8([Elaborar Rascunhos de Conteúdo & Editais])
            UC9([Gerenciar Manifestações de Interesse])
            UC10([Revisar & Aprovar Publicação Oficial])
        end
    end

    A1 --> UC2 & UC4
    A2 --> UC1 & UC2 & UC4 & UC6 & UC7
    A3 --> UC2 & UC3 & UC4
    A4 --> UC2 & UC4 & UC5
    A5 --> UC8 & UC9
    A6 --> UC10
