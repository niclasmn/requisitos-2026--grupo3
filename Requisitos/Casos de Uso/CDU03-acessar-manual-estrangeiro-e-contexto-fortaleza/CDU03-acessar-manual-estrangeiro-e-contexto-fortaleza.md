# Especificação de Requisitos Funcionais

## Caso de Uso (CDU) - LAPIS

## Histórico de Versões

<!-- markdownlint-disable MD060 -->
| Data       | Versão | Descrição                                                                                                                                    | Autor    |
| ---------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| 26/11/2026 | 1.0    | Criação da especificação do CDU03 (UC3) com base na Visão da Demanda v2.0 do Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI). | Equipe 3 |
<!-- markdownlint-enable MD060 -->

## 1. Nome do Caso de Uso

Acessar Manual Estrangeiro e Contexto Fortaleza

## 2. Objetivo

Disponibilizar ao estudante estrangeiro um guia prático em língua inglesa com orientações essenciais de pré-chegada e vivência na Unifor em Fortaleza, abrangendo disciplinas ofertadas em inglês/outros idiomas, bairros próximos ao campus, moradia, custo de vida, serviços do entorno e alertas obrigatórios sobre visto de estudante e frequência mínima.

## 3. Tipo de Caso de Uso

Concreto

## 4. Atores

### 4.1 Primário

Estudante Estrangeiro (universitário internacional interessado ou aceito para mobilidade acadêmica de entrada na Unifor — Persona: Claire).

### 4.2 Secundário

Não se aplica.

## 5. Precondições

1. O portal PUMI está acessível publicamente no ecossistema da Unifor.
2. Os conteúdos do Manual do Estrangeiro e Guia de Fortaleza possuem versão em inglês aprovada pelo Departamento de Marketing (RN01 e RN07).

## 6. Fluxo Principal

### P1. Acessar a jornada internacional de entrada

O estudante estrangeiro acessa o portal PUMI e seleciona a jornada **Do Mundo para a Unifor (*From the World to Unifor*)**.

### P2. Exibir o Manual do Estrangeiro e Guia de Fortaleza em inglês

O sistema apresenta a interface em língua inglesa (RN07) organizada em seções temáticas: *Academic & Courses in English*, *Student Visa & Mandatory Rules*, *Living in Fortaleza & Neighborhoods*, *Cost of Living & Campus Surroundings* e *Application Steps*.

### P3. Selecionar seção de interesse (Disciplinas ou Contexto Local)

O estudante seleciona uma das categorias do guia, como **Disciplinas Ofertadas em Inglês/Outros Idiomas** ou **Moradia e Entorno da Unifor em Fortaleza**.

### P4. Apresentar orientações práticas e alertas institucionais

O sistema exibe o conteúdo detalhado da seção escolhida, incluindo a lista atualizada de disciplinas ministradas fora do português, orientações sobre bairros residenciais próximos ao campus (ex.: Edson Queiroz, Cocó, Água Fria), opções de moradia, estimativa de custo de vida local, localização estratégica da Unifor próxima a praias, shoppings, bancos e comércio, além dos destaques permanentes de **visto de estudante obrigatório** (RN03) e **75% de frequência mínima** (RN04).

### P5. Consultar passo a passo de candidatura ou contato institucional

O estudante avança para a seção de orientação de candidatura (*How to Apply*), onde o sistema exibe os requisitos documentais, prazos e os links/canais oficiais de submissão da DRI (F2.5).

## 7. Fluxos Alternativos

### A1. Alternar idioma de visualização entre Inglês e Português

* **Ponto de entrada:** No passo P2, o usuário clica no seletor de idioma no topo da página (*EN / PT*).
* **A1.1.** O sistema alterna a exibição do conteúdo entre a versão prioritária em inglês (RN07) e a versão em português.
* **Ponto de saída:** Retorna ao passo P2 mantendo a seção ativa.

### A2. Baixar ou imprimir guia resumido de pré-chegada

* **Ponto de entrada:** Nos passos P2 ou P4, o estudante aciona a opção **Imprimir / Salvar Guia em PDF (*Print / Save Guide*)**.
* **A2.1.** O sistema aciona a folha de estilo otimizada para impressão/salvamento limpo das orientações essenciais de chegada.
* **Ponto de saída:** Retorna ao passo P4.

## 8. Fluxos de Exceção

### E1. Conteúdo específico sem tradução disponível no idioma selecionado

* **Ponto de entrada:** Nos passos P3 ou P4, o estudante acessa um documento complementar externo ou anexo institucional disponível apenas em português.
* **E1.1.** O sistema exibe o aviso em inglês: *"This supplementary document is currently available only in Portuguese. All essential admission and visa guidelines are available in English above."* (em conformidade com a estratégia de tradução viável definida na RN07).
* **Ponto de saída:** Retorna ao passo P4.

### E2. Falha no carregamento das informações do guia

* **Ponto de entrada:** Nos passos P2 ou P4, ocorre erro de rede ou indisponibilidade do servidor de conteúdo.
* **E2.1.** O sistema exibe mensagem em inglês: *"Unable to load the International Student Guide at the moment. Please refresh the page or contact DRI."*
* **Ponto de saída:** Encerra o fluxo ou retorna ao passo P1 upon recarregamento.

## 9. Pós-condições

1. O estudante estrangeiro obtém informações claras em inglês sobre disciplinas em outros idiomas, moradia, custo de vida em Fortaleza e funcionamento do entorno da Unifor.
2. O estudante é formalmente cientificado da obrigatoriedade do visto de estudante (RN03) e da exigência de 75% de frequência (RN04).

## 10. Requisitos Não Funcionais

1. **Prioridade de Idioma Inglês (RN07):** Toda a navegação principal, títulos, alertas legais e orientações do manual devem estar redigidos em inglês claro e revisado.
2. **Conformidade Visual:** Seguir os padrões institucionais da Unifor definidos pelo Marketing.
3. **Usabilidade Móvel:** O guia deve ser facilmente navegável via smartphone, considerando o uso pelo estudante estrangeiro durante o deslocamento e chegada a Fortaleza.

## 11. Ponto de Extensão

### PE1. Consultar Detalhes das Regras Legais de Visto e Frequência

* **Ponto de extensão:** Passo P4 (nos quadros de destaque legal).
* **Descrição:** Permite ao estudante estrangeiro acessar o quadro completo de regras inegociáveis versus flexibilidades acadêmicas descrito no **CDU04 — Consultar Alertas Legais de Visto e Frequência**.

## 12. Frequência de Utilização

**Média** — Com picos de acesso durante as janelas de nomeação de intercambistas estrangeiros pelas universidades parceiras e nos meses que antecedem o início dos semestres letivos (janeiro/fevereiro e julho/agosto).

## 13. Interface Visual

### IV1. Portal *From the World to Unifor* — Manual do Estrangeiro e Guia de Fortaleza

* **Localização:** Portal Unifor > DRI > Do Mundo para a Unifor (*From the World to Unifor*).
* **Leiaute:**
  * Banner institucional em inglês destacando a Unifor e Fortaleza.
  * Faixa permanente de alerta legal (*Mandatory Notice: Student Visa & 75% Minimum Attendance*).
  * Menu lateral ou em abas com as seções: *Courses in English*, *Living in Fortaleza (Neighborhoods & Housing)*, *Cost of Living & Surroundings (Beaches, Malls, Banks)* e *How to Apply*.
  * Cartões visuais informativos com distâncias aproximadas do campus da Unifor aos principais pontos de serviço e lazer.

## 14. Observações

Conforme alinhado com a DRI (RN07), o portal prioriza a tradução em inglês nas páginas essenciais para estrangeiros, manuais de chegada e apresentação institucional, evitando custos inviáveis com tradução integral de documentos administrativos internos extensos.

## 15. Referências

* Documento de Visão da Demanda (VD) — PUMI, Versão 2.0 (23/11/2026), Seções 2.2, 3.1, 3.2, 3.3, 5.2 (Persona Claire), 6 (F2.2, F2.5), 7 (RN01, RN03, RN04, RN07) e 8.1 (UC3).
* CDU04 — Consultar Alertas Legais de Visto e Frequência.

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
