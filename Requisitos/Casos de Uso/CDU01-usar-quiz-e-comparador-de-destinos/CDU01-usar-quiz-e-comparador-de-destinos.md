# Especificação de Requisitos Funcionais

## Caso de Uso (CDU) - LAPIS

## Histórico de Versões

<!-- markdownlint-disable MD060 -->
| Data       | Versão | Descrição                                                                                                                                    | Autor    |
| ---------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| 26/11/2026 | 1.0    | Criação da especificação do CDU01 (UC1) com base na Visão da Demanda v2.0 do Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI). | Equipe 3 |
<!-- markdownlint-enable MD060 -->

## 1. Nome do Caso de Uso

Usar Quiz e Comparador de Destinos

## 2. Objetivo

Permitir que o estudante da Unifor descubra países, cidades e instituições conveniadas compatíveis com seu perfil por meio de um quiz interativo de afinidade e compare características práticas (custo estimado de manutenção, idioma, cultura, prós e contras) para apoiar sua decisão de mobilidade internacional.

## 3. Tipo de Caso de Uso

Concreto

## 4. Atores

### 4.1 Primário

Estudante Unifor (estudante de graduação ou pós-graduação da Universidade de Fortaleza interessado em mobilidade de saída — Persona: Lucas).

### 4.2 Secundário

Visitante / Parceiro (pode consultar diretamente as fichas comparativas públicas de destinos sem realizar autenticação).

## 5. Precondições

1. O portal PUMI está acessível no ecossistema digital oficial da Unifor.
2. Existem fichas de destinos e instituições conveniadas previamente aprovadas pelo Departamento de Marketing e publicadas no sistema (RN01).

## 6. Fluxo Principal

### P1. Acessar o módulo de descoberta de destinos

O estudante da Unifor acessa a jornada *Estude Mundo Afora com a Unifor* no portal PUMI e seleciona a opção **Quiz e Comparador de Destinos**.

### P2. Apresentar o questionário de afinidade

O sistema exibe a tela inicial do Quiz Interativo de Destinos com perguntas objetivas sobre faixa de orçamento mensal estimado, idiomas de domínio ou interesse, objetivos acadêmicos/culturais e preferências climáticas ou regionais.

### P3. Responder ao quiz de afinidade

O estudante preenche as respostas das etapas do questionário e aciona o comando **Ver Destinos Compatíveis**.

### P4. Processar compatibilidade e exibir recomendações

O sistema cruza as respostas informadas com os atributos cadastrados nas fichas de destinos publicadas, calcula o grau de afinidade e exibe uma lista ordenada de países, cidades e instituições conveniadas recomendadas.

### P5. Selecionar destinos para comparação detalhada

O estudante seleciona de dois a três destinos recomendados e aciona a opção **Comparar Destinos**.

### P6. Exibir ficha comparativa lado a lado

O sistema apresenta uma matriz comparativa contendo país, cidade, custo médio mensal de manutenção, idioma das aulas e local, aspectos culturais, principais prós e contras, alertas resumidos de antecedência consular (RN05) e links diretos para os editais vigentes vinculados a cada destino.

## 7. Fluxos Alternativos

### A1. Acessar diretamente o Comparador de Destinos sem responder ao Quiz

* **Ponto de entrada:** No passo P2, o usuário (Estudante Unifor ou Visitante) opta por ignorar o quiz e clica em **Explorar Todos os Destinos / Comparador**.
* **A1.1.** O sistema exibe o catálogo completo de fichas de destinos publicados, com filtros por continente, país, idioma e faixa de custo de manutenção.
* **A1.2.** O usuário aplica os filtros desejados e seleciona de dois a três destinos para visualização lado a lado.
* **Ponto de saída:** Segue para o passo P6 do fluxo principal.

### A2. Refazer o Quiz com novos critérios

* **Ponto de entrada:** Nos passos P4 ou P6, o estudante aciona a opção **Refazer Quiz**.
* **A2.1.** O sistema limpa as seleções anteriores e restaura o formulário inicial do questionário.
* **Ponto de saída:** Retorna ao passo P2 do fluxo principal.

### A3. Navegar da ficha comparativa para oportunidades vigentes do destino

* **Ponto de entrada:** No passo P6, o estudante clica em **Ver Oportunidades neste Destino**.
* **A3.1.** O sistema redireciona o estudante para o catálogo de editais filtrado pelo país/instituição escolhida (referência ao CDU02).
* **Ponto de saída:** Encerra este caso de uso e inicia o fluxo de consulta de editais.

## 8. Fluxos de Exceção

### E1. Nenhum destino encontrado para a combinação exata de critérios

* **Ponto de entrada:** No passo P4, o cruzamento de critérios do quiz não retorna destinos com compatibilidade mínima.
* **E1.1.** O sistema exibe a mensagem informativa: *"Não encontramos destinos exatos para todos os critérios selecionados. Veja opções próximas ajustando orçamento ou idioma."* e lista destinos parcialmente compatíveis.
* **E1.2.** O estudante escolhe uma das sugestões próximas ou opta por ajustar suas respostas.
* **Ponto de saída:** Retorna ao passo P2 (se optar por refazer) ou segue para o passo P5 (se selecionar uma sugestão próxima).

### E2. Submissão do quiz com perguntas obrigatórias não respondidas

* **Ponto de entrada:** No passo P3, o estudante tenta avançar ou concluir o quiz deixando campos obrigatórios em branco.
* **E2.1.** O sistema destaca os campos pendentes e exibe a mensagem: *"Por favor, responda às perguntas obrigatórias para gerar suas recomendações de destino."*
* **Ponto de saída:** Retorna ao passo P3 para preenchimento pelo estudante.

### E3. Falha ao carregar dados das fichas de destinos

* **Ponto de entrada:** Nos passos P4 ou P6, ocorre indisponibilidade temporária na consulta à base de dados de destinos.
* **E3.1.** O sistema exibe a mensagem: *"Não foi possível carregar as informações dos destinos no momento. Tente novamente em instantes."* e disponibiliza botão de recarregamento.
* **Ponto de saída:** Encerra o fluxo ou retorna ao passo P1 caso o usuário tente novamente.

## 9. Pós-condições

1. O estudante visualiza recomendações personalizadas de destinos e/ou o quadro comparativo detalhado de custos, idioma, cultura e prós/contras.
2. Nenhum dado pessoal identificável de intercambistas anteriores é exposto durante a navegação (RN02).

## 10. Requisitos Não Funcionais

1. **Identidade Visual Institucional:** As telas do quiz e do comparador devem seguir rigorosamente o guia de marca oficial da Unifor.
2. **Responsividade:** A matriz comparativa deve adaptar-se a dispositivos móveis (exibição em abas ou rolagem horizontal acessível) e desktops.
3. **Desempenho:** O cálculo de afinidade e o carregamento da comparação devem responder em até 2 segundos.
4. **Privacidade (LGPD - RN02):** As respostas do quiz em sessão pública não exigem identificação pessoal nem armazenam histórico vinculado ao CPF/matrícula sem consentimento.

## 11. Ponto de Extensão

### PE1. Consultar Editais e Instituições do Destino Selecionado

* **Ponto de extensão:** Passo P6 (e fluxo alternativo A3).
* **Descrição:** A partir da ficha comparativa de um destino, o estudante pode estender a navegação para o **CDU02 — Consultar Editais, Instituições e Mapa** já filtrado pelo país ou instituição conveniada selecionada.

## 12. Frequência de Utilização

**Alta** — Especialmente nos períodos que antecedem a abertura de editais semestrais de intercâmbio (março/abril e setembro/outubro). As informações mais acessadas são custo estimado de manutenção mensal, idioma exigido e prós/contras de cada país.

## 13. Interface Visual

### IV1. Tela do Quiz Interativo e Matriz Comparativa de Destinos

* **Localização:** Portal Unifor > DRI > Estude Mundo Afora > Quiz e Comparador de Destinos.
* **Leiaute:**
  * Cabeçalho institucional padrão Unifor com trilha de navegação (*breadcrumb*).
  * Cartão central progressivo (etapas 1 a 4) com barra de progresso, perguntas objetivas com ícones ilustrativos e botão para pular diretamente ao comparador.
  * Grade de resultados com selo de afinidade (%) e caixas de seleção (até 3 destinos) para comparação.
  * Tabela comparativa estruturada por critérios (País/Cidade, Custo Médio de Manutenção, Idioma, Cultura, Prós, Contras, Alerta de Prazo Consular) e botões de ação para visualizar editais vinculados.

## 14. Observações

Os valores de custo de manutenção exibidos nas fichas são estimativas orientativas mantidas pela DRI e revisadas pelo Marketing. Caso um destino não possua edital aberto no momento, a ficha permanece visível para planejamento antecipado do aluno.

## 15. Referências

* Documento de Visão da Demanda (VD) — PUMI, Versão 2.0 (23/11/2026), Seções 2.2, 3.1, 3.2, 5.1 (Persona Lucas), 6 (F1.2 e F1.3), 7 (RN01, RN02, RN05) e 8.1 (UC1).
* CDU02 — Consultar Editais, Instituições e Mapa.

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
