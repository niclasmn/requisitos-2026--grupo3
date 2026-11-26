# Especificação de Requisitos Funcionais

## Caso de Uso (CDU) - LAPIS

## Histórico de Versões

<!-- markdownlint-disable MD060 -->
| Data       | Versão | Descrição                                                                                                                                    | Autor    |
| ---------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| 26/11/2026 | 1.0    | Criação da especificação do CDU05 (UC5) com base na Visão da Demanda v2.0 do Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI). | Equipe 3 |
<!-- markdownlint-enable MD060 -->

## 1. Nome do Caso de Uso

Consultar Vitrine Docente e Publicação Científica

## 2. Objetivo

Disponibilizar aos professores da Unifor uma vitrine institucional centralizada com programas de mobilidade docente, redes de cooperação internacional e curadoria de revistas científicas internacionais qualificadas e sem custos proibitivos, visando impulsionar a produção científica internacional e o web impact da Universidade.

## 3. Tipo de Caso de Uso

Concreto

## 4. Atores

### 4.1 Primário

Docente Unifor (professor ou pesquisador da Universidade de Fortaleza interessado em intercâmbio docente, cooperação internacional ou publicação científica — Persona: Prof. Roberto).

### 4.2 Secundário

Não se aplica.

## 5. Precondições

1. O portal PUMI está acessível no ecossistema da Unifor.
2. Existem registros de programas docentes, redes de cooperação e periódicos recomendados aprovados pelo Departamento de Marketing (RN01).

## 6. Fluxo Principal

### P1. Acessar a jornada de Mobilidade Docente e Pesquisa Internacional

O docente da Unifor acessa o portal PUMI e seleciona a jornada **Docentes e Pesquisa Internacional (*Web Impact*)**.

### P2. Exibir vitrine docente e curadoria de periódicos científicos

O sistema apresenta a área dedicada aos professores dividida em dois eixos principais:
1. **Mobilidade Docente e Cooperação Internacional:** editais de intercâmbio para professores, missões acadêmicas, chamadas de pesquisa conjunta e redes de cooperação com instituições parceiras.
2. **Curadoria de Publicação Científica Internacional (*Web Impact*):** diretrizes institucionais e lista curada de periódicos científicos internacionais qualificados com isenção ou custos acessíveis de publicação (*APC*).

### P3. Filtrar oportunidades docentes ou periódicos recomendados

O docente filtra os itens por área do conhecimento, país/região parceira, tipo de oportunidade (mobilidade docente, cooperação ou periódico científico) ou faixa de custo de publicação.

### P4. Atualizar listagem filtrada

O sistema exibe os cartões correspondentes com título, instituição/editora parceira, escopo acadêmico, requisitos, prazos e indicadores de relevância científica.

### P5. Visualizar detalhes do programa ou periódico selecionado

O docente clica em um item de interesse e o sistema exibe a ficha completa com orientações de submissão, documentos institucionais necessários, alertas de prazo consular quando houver deslocamento (RN05) e o link oficial para candidatura ou submissão do artigo (F2.5).

## 7. Fluxos Alternativos

### A1. Consultar orientações institucionais para cooperação internacional

* **Ponto de entrada:** No passo P2, o docente seleciona a aba **Como Propor Parcerias e Redes de Cooperação**.
* **A1.1.** O sistema exibe o fluxo institucional da DRI para formalização de convênios acadêmicos, cartas de intenção e canais de contato da diretoria.
* **Ponto de saída:** Retorna ao passo P2.

### A2. Acessar portal externo do periódico ou edital docente

* **Ponto de entrada:** No passo P5, o docente clica em **Acessar Site Oficial do Periódico / Edital**.
* **A2.1.** O sistema abre o endereço oficial externo em nova aba do navegador.
* **Ponto de saída:** Encerra o caso de uso.

## 8. Fluxos de Exceção

### E1. Nenhum programa docente ou periódico encontrado para o filtro aplicado

* **Ponto de entrada:** No passo P4, o filtro por área do conhecimento ou país não retorna registros cadastrados.
* **E1.1.** O sistema exibe a mensagem: *"Nenhum programa docente ou periódico encontrado para os critérios selecionados. Exibindo todas as áreas disponíveis."* e restaura a listagem geral.
* **Ponto de saída:** Retorna ao passo P2.

### E2. Falha ao carregar o catálogo docente

* **Ponto de entrada:** Nos passos P2 ou P5, ocorre falha de comunicação com o servidor de conteúdo.
* **E2.1.** O sistema exibe a mensagem: *"Não foi possível carregar a Vitrine Docente no momento. Tente novamente em instantes."*
* **Ponto de saída:** Encerra o fluxo.

## 9. Pós-condições

1. O docente identifica oportunidades de mobilidade acadêmica, redes de pesquisa e periódicos científicos internacionais qualificados e acessíveis.
2. Fomenta-se o alinhamento das publicações e parcerias docentes à estratégia de *web impact* da Unifor.

## 10. Requisitos Não Funcionais

1. **Identidade Visual Institucional:** Seguir os padrões visuais e editoriais do Departamento de Marketing da Unifor.
2. **Conformidade LGPD (RN02):** Eventuais métricas de produção internacional exibidas na vitrine devem ser agregadas, sem exposição indevida de dados pessoais.
3. **Desempenho e Responsividade:** Carregamento dos filtros e fichas em até 2 segundos em dispositivos desktop e móveis.

## 11. Ponto de Extensão

Não se aplica.

## 12. Frequência de Utilização

**Média** — Acessado regularmente por docentes pesquisadores ao longo dos semestres letivos para planejamento de missões acadêmicas, convênios e submissão de artigos internacionais.

## 13. Interface Visual

### IV1. Vitrine Docente & Publicação Científica (*Web Impact*)

* **Localização:** Portal Unifor > DRI > Docentes e Pesquisa Internacional.
* **Leiaute:**
  * Cabeçalho contextual explicando o apoio da DRI à internacionalização docente e ao *web impact* da Unifor.
  * Alternância em duas abas principais: *Mobilidade & Cooperação Docente* e *Revistas Científicas Recomendadas*.
  * Barra de filtros por Área do Conhecimento, País/Região e Modalidade.
  * Cartões informativos com selo de custo acessível/isento (para periódicos), prazos e botão de acesso ao canal oficial.

## 14. Observações

A curadoria de revistas científicas internacionais sem custos proibitivos foi destacada pela DRI na entrevista pós-visão como estratégica para ampliar a visibilidade internacional (*web impact*) da Unifor.

## 15. Referências

* Documento de Visão da Demanda (VD) — PUMI, Versão 2.0 (23/11/2026), Seções 2.1, 2.2, 3.1, 3.2, 5.4 (Persona Prof. Roberto), 6 (F1.5, F2.5), 7 (RN01, RN02, RN05) e 8.1 (UC5).

## 16. Checklist de Validação do Artefato (CDU)

### 16.1 Estrutura mínima

* [x] Nome do caso de uso iniciado com verbo no infinitivo.
* [x] Objetivo claro, direto e com foco em um objetivo principal.
* [x] Tipo do caso de uso informado (concreto/abstrato), quando aplicável.
* [x] Atores primário e secundários identificados corretamente.
* [x] Precondições registradas (ou seção marcada como "Não se aplica").
* [x] Fluxo principal completo e coerente com o objetivo.
* [x] Fluxos alternativos e de exceção definidos quando necessários.
* [x] Pós-condições registradas (ou seção marcada como "Não se aplica").
* [x] Requisitos não funcionais específicos do CDU registrados, quando existirem.
* [x] Pontos de extensão identificados corretamente, quando existirem.
* [x] Frequência de utilização estimada.

### 16.2 Qualidade da especificação

* [x] Passos escritos com linguagem simples e objetiva.
* [x] Ações descritas com verbos no presente do indicativo (3ª pessoa).
* [x] Alternância entre ação do ator e ação da solução está clara.
* [x] Não há ambiguidade (termos vagos sem detalhe técnico).
* [x] Regras de negócio e mensagens estão referenciadas quando necessário.

### 16.3 Consistência e rastreabilidade

* [x] Pontos de entrada e saída dos fluxos alternativos estão explícitos.
* [x] Fluxos de exceção estão vinculados aos passos corretos da solução.
* [x] Referências internas entre passos (retorna/segue para) estão corretas.
* [x] Interface visual (IV1 etc.) está coerente com o fluxo descrito.
* [x] Referências para visão da demanda, glossário e RNF estão atualizadas.

### 16.4 Revisão final

* [x] Não há contradições entre seções do artefato.
* [x] Links internos e externos foram validados.
* [ ] Documento revisado por pares.
* [x] Artefato pronto para uso em desenvolvimento e testes.
