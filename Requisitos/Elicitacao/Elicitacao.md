# Elicitação de Requisitos — Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI)

**Instituição:** Universidade de Fortaleza (Unifor)  
**Disciplina / Contexto:** T193-16 — Requisitos e Modelagem de Sistemas  
**Metodologia:** Scrum  

---

## Histórico de Versões

| Data | Versão | Descrição | Autor |
|---|---:|---|---|
| 29/10/2026 | 1.0 | Registro inicial do processo de elicitação e visão do PUMI. | Equipe 3 — Nicholas |
| 01/11/2026 | 1.1 | Consolidação das frentes de mobilidade e escopo do MVP. | Equipe 3 |
| 10/11/2026 | 1.2 | Refinamento de personas, perfis de acesso e funcionalidades. | Equipe 3 |
| 23/11/2026 | 2.0 | Consolidação pós-entrevista com a DRI: governança do Marketing, conformidade LGPD, regras de visto/frequência (75%), integração ao portal Unifor, mobilidade docente/web impact, quiz de destinos e guia de Fortaleza. | Equipe 3 |

---

## 1. Visão Geral, Proposta de Valor e Escopo

O **Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI)** é um módulo de expansão integrado ao ambiente digital oficial da **Universidade de Fortaleza (Unifor)** e da **Diretoria de Relações Internacionais (DRI)**, sem operar como site externo isolado.

### 1.1. Frentes Estratégicas
1. **Descoberta Inteligente e Apoio à Decisão (Mobilidade de Saída):** organização de editais próprios e de parceiros (como Santander), antecedência consular e **Quiz / Assistente Interativo de Afinidade**, permitindo comparar países, cidades, custo de manutenção, cultura e prós/contras.
2. **Acolhimento e Contexto Local (Mobilidade de Entrada):** manual prático em inglês sobre disciplinas ofertadas em inglês/outros idiomas, bairros próximos ao campus, moradia, custo de vida e proximidades em Fortaleza (praias, shoppings, bancos e comércio).
3. **Visibilidade Acadêmica e Mobilidade Docente (*Web Impact*):** vitrine institucional de cooperação, intercâmbio docente e curadoria de revistas científicas internacionais qualificadas e sem custos proibitivos.

### 1.2. Escopo do MVP e Exclusões Explícitas
* **Incluído no MVP:** navegação integrada por jornadas, quiz e comparador de destinos, catálogo de oportunidades com mapa-múndi simplificado e indicadores agregados, manual do estrangeiro em inglês e guia de Fortaleza, alertas legais (visto de estudante vs. passaporte e frequência mínima de 75%), vitrine docente, verificação preliminar de elegibilidade, manifestação simplificada de interesse com protocolo, gestão de rascunhos pela DRI e aprovação editorial pelo Departamento de Marketing.
* **Fora do Escopo do MVP:** candidatura formal/inscrição definitiva dentro do PUMI, upload de documentos e análise documental oficial dentro da plataforma.

---

## 2. Partes Interessadas (Stakeholders)

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

## 3. Personas

### 3.1. Lucas — Estudante da Unifor (Mobilidade de Saída)
* **Perfil:** Estudante de graduação interessado em intercâmbio, indeciso sobre o destino e com dúvidas sobre custos e trâmites consulares.
* **Objetivos:** Descobrir destinos alinhados ao perfil, comparar custo de vida e cultura, verificar elegibilidade preliminar e planejar prazos com antecedência.
* **Dores:** Incerteza entre países, confusão entre passaporte e visto de estudante e desconhecimento dos prazos de envio a consulados.
* **Necessidades:** Quiz interativo de afinidade, fichas comparativas, alertas de vistos/prazos e verificador preliminar de elegibilidade.

### 3.2. Claire — Estudante Estrangeira (Mobilidade de Entrada)
* **Perfil:** Universitária estrangeira que deseja realizar mobilidade acadêmica na Unifor em Fortaleza.
* **Objetivos:** Compreender em inglês o processo de candidatura, disciplinas em outros idiomas, opções de moradia perto do campus e regras acadêmicas/migratórias.
* **Dores:** Falta de orientações práticas sobre bairros, moradia e entorno da Unifor; risco de viajar sem visto de estudante adequado ou desconhecer a frequência mínima de 75%.
* **Necessidades:** Manual do estrangeiro em inglês, guia de localização/moradia em Fortaleza e alertas claros sobre visto obrigatório e 75% de frequência.

### 3.3. Camila — Profissional da DRI
* **Perfil:** Analista da DRI que atende dúvidas recorrentes, organiza editais e prepara comunicações institucionais.
* **Objetivos:** Reduzir atendimentos repetitivos, manter minutas organizadas e submeter atualizações ao Marketing com agilidade.
* **Dores:** Retrabalho com perguntas básicas sobre moradia, vistos e prazos; necessidade de cumprir a aprovação do Marketing sem expor dados pessoais (LGPD).
* **Necessidades:** Gestão de rascunhos com aprovação do Marketing, centralização de guias e painel de manifestações de interesse.

### 3.4. Prof. Roberto — Docente da Unifor
* **Perfil:** Professor pesquisador interessado em cooperação internacional, intercâmbio docente e publicação de artigos no exterior.
* **Objetivos:** Identificar oportunidades de mobilidade docente e periódicos científicos internacionais qualificados sem custos proibitivos.
* **Dores:** Falta de visibilidade centralizada de iniciativas docentes e dificuldade para mapear periódicos recomendados para ampliar o *web impact* da Unifor.
* **Necessidades:** Vitrine de mobilidade docente, parcerias de pesquisa e curadoria de revistas científicas internacionais.

### 3.5. Mariana — Analista de Marketing da Unifor
* **Perfil:** Profissional responsável pela identidade visual, qualidade textual e conformidade institucional dos canais digitais da Unifor.
* **Objetivos:** Assegurar que todo conteúdo da DRI siga o padrão visual da Unifor, não apresente falhas ou riscos de imagem e respeite a LGPD.
* **Dores:** Publicações sem padronização gráfica ou sem revisão editorial prévia.
* **Necessidades:** Fila de revisão e aprovação editorial para validar, solicitar ajustes ou aprovar publicações submetidas pela DRI.

---

## 4. Levantamento de Requisitos Funcionais (Rastreabilidade com CDUs)

| ID Func. | Funcionalidade | CDU Relacionado | Escopo | Atores | Valor |
|---|---|---|---|---|---|
| **F1.1** | Portal integrado por jornadas | CDU02 | Incluída | Todos os visitantes | Alto |
| **F1.2** | Quiz / Assistente interativo de destinos | CDU01 | Incluída | Estudante Unifor | Alto |
| **F1.3** | Fichas comparativas de destinos | CDU01 | Incluída | Estudante Unifor, visitante | Alto |
| **F1.4** | Catálogo de oportunidades e mapa | CDU02 | Incluída | Estudante Unifor, docente, visitante | Alto |
| **F1.5** | Vitrine docente e publicação científica | CDU05 | Incluída | Docente Unifor | Alto |
| **F1.6** | Indicadores agregados (LGPD) | CDU02 | Incluída | Todos os visitantes | Médio |
| **F2.1** | Guia de saída e alertas consulares | CDU04 | Incluída | Estudante Unifor, docente | Alto |
| **F2.2** | Manual do estrangeiro e contexto Fortaleza | CDU03 | Incluída | Estudante estrangeiro | Alto |
| **F2.3** | Quadro de regras inegociáveis vs. flexibilidades | CDU04 | Incluída | Estudante estrangeiro, estudante Unifor | Alto |
| **F2.4** | Verificação preliminar de elegibilidade | CDU06 | Incluída | Estudante Unifor | Alto |
| **F2.5** | Direcionamento para candidatura oficial | CDU02, CDU03, CDU05, CDU07 | Incluída | Estudante Unifor, estrangeiro, docente | Alto |
| **F3.1** | Manifestação simplificada de interesse | CDU07 | Incluída | Estudante Unifor | Alto |
| **F3.2** | Gestão de manifestações pela DRI | CDU09 | Incluída | Profissional da DRI | Alto |
| **F3.3** | Gestão de rascunhos pela DRI | CDU08 | Incluída | Profissional da DRI | Alto |
| **F3.4** | Fluxo de aprovação e publicação (Marketing) | CDU10 | Incluída | Analista de Marketing | Alto |
| **F3.5** | Gestão de tradução estratégica | CDU08, CDU10 | Incluída | Profissional da DRI, Marketing | Alto |

---

## 5. Pontos Pendentes de Validação Institucional

* **Critérios de Elegibilidade (PMG):** Nota mínima de PMG por edital, cálculo e regras definitivas sujeitos à validação da DRI.
* **Autenticação Institucional (SSO):** Viabilidade técnica, documentação e autorização da área de TI da Unifor para login institucional.
* **Priorização Scrum:** Revisão final de backlog e prioridades (*Must / Should / Could*) com o Product Owner e a equipe.
