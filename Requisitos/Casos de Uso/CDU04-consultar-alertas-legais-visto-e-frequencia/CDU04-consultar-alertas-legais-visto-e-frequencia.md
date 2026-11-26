# Especificação de Requisitos Funcionais

## Caso de Uso (CDU) - LAPIS

## Histórico de Versões

<!-- markdownlint-disable MD060 -->
| Data       | Versão | Descrição                                                                                                                                    | Autor    |
| ---------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| 26/11/2026 | 1.0    | Criação da especificação do CDU04 (UC4) com base na Visão da Demanda v2.0 do Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI). | Equipe 3 |
<!-- markdownlint-enable MD060 -->

## 1. Nome do Caso de Uso

Consultar Alertas Legais de Visto e Frequência

## 2. Objetivo

Apresentar de forma destacada e inequívoca as normas legais migratórias e acadêmicas inegociáveis da mobilidade internacional — especialmente a obrigatoriedade do visto de estudante (em contraste com passaporte/visto de turismo), os prazos de antecedência consular e a exigência de 75% de frequência mínima — diferenciando-as das flexibilidades acadêmicas passíveis de análise caso a caso.

## 3. Tipo de Caso de Uso

Concreto

## 4. Atores

### 4.1 Primário

Usuário / Candidato à Mobilidade (Estudante Unifor, Estudante Estrangeiro, Docente Unifor ou Visitante consultando regras de mobilidade).

### 4.2 Secundário

Não se aplica.

## 5. Precondições

1. O portal PUMI está acessível ao público.
2. As diretrizes legais e acadêmicas estão publicadas e aprovadas pelo Departamento de Marketing (RN01).

## 6. Fluxo Principal

### P1. Acessar o Guia de Mobilidade e Regras Legais

O usuário acessa o portal PUMI e seleciona a seção **Regras Legais, Vistos e Vida Acadêmica** (acessível tanto pela jornada de saída quanto pela jornada de entrada, em português e em inglês).

### P2. Exibir quadro comparativo de regras inegociáveis versus flexibilidades

O sistema exibe a página estruturada em três blocos principais:
1. **Regras Legais e Institucionais Inegociáveis:** obrigatoriedade do **visto de estudante válido** para matrícula de estrangeiros na Unifor (alertando para a ilegalidade e penalidades junto à Polícia Federal e MEC caso tente ingressar apenas com passaporte/visto de turismo — RN03) e obrigatoriedade de **75% de frequência mínima** para aprovação nas disciplinas (RN04).
2. **Diferença entre Passaporte e Visto de Estudante + Antecedência Consular:** explicação prática sobre passaporte, carta de aceite, prazos de envio de documentos a consulados, emissão de seguro-viagem e compra de passagens (RN05).
3. **Flexibilidades Acadêmicas Avaliadas Caso a Caso:** orientações sobre possibilidades sujeitas à análise da coordenação e da DRI (como cursar disciplinas de outro curso ou aproveitamento de créditos).

### P3. Selecionar perfil de interesse (Saída ou Entrada)

O usuário alterna entre a visualização focada em **Mobilidade de Saída (Estudantes e Docentes Unifor)** ou **Mobilidade de Entrada (Estudantes Estrangeiros)**.

### P4. Detalhar checklists documentais e prazos críticos

O sistema apresenta o checklist orientativo correspondente ao perfil selecionado, destacando os prazos mínimos recomendados antes da viagem e os contatos institucionais da DRI para dúvidas específicas.

## 7. Fluxos Alternativos

### A1. Consultar alertas legais em língua inglesa

* **Ponto de entrada:** No passo P2, o estudante estrangeiro seleciona o idioma **Inglês (EN)**.
* **A1.1.** O sistema exibe todo o conteúdo de regras inegociáveis (Student Visa vs. Tourist Visa/Passport e 75% Attendance Rule) e flexibilidades acadêmicas em inglês (RN07).
* **Ponto de saída:** Segue para o passo P3 do fluxo principal.

### A2. Acessar alerta legal a partir de um edital ou do Manual do Estrangeiro

* **Ponto de entrada:** O usuário clica em um link de alerta legal dentro do CDU02 (Editais) ou do CDU03 (Manual do Estrangeiro).
* **A2.1.** O sistema abre diretamente a seção correspondente do guia de regras legais com foco no alerta clicado.
* **Ponto de saída:** Segue para o passo P4 do fluxo principal.

## 8. Fluxos de Exceção

### E1. Indisponibilidade temporária da página de orientações

* **Ponto de entrada:** No passo P2, ocorre falha no carregamento da página pelo servidor web.
* **E1.1.** O sistema exibe mensagem informando a indisponibilidade momentânea e orienta que nenhuma viagem ou matrícula seja realizada sem consulta prévia à DRI sobre visto e prazos consulares.
* **Ponto de saída:** Encerra o fluxo.

## 9. Pós-condições

1. O usuário compreende a distinção clara entre normas legais/acadêmicas inegociáveis (visto de estudante e 75% de frequência) e flexibilidades sujeitas à análise.
2. Reduz-se o risco de irregularidades migratórias (Polícia Federal/MEC) e de reprovação por falta.

## 10. Requisitos Não Funcionais

1. **Destaque Visual e Clareza Semântica:** Os alertas de visto de estudante (RN03) e frequência mínima de 75% (RN04) devem utilizar componentes visuais de alerta institucional (ícones e caixas de destaque) aprovados pelo Marketing.
2. **Bilíngue Estratégico (RN07):** Disponibilidade obrigatória em português e inglês.

## 11. Ponto de Extensão

Não se aplica.

## 12. Frequência de Utilização

**Alta** — Consultado continuamente por candidatos em preparação documental e referenciado diretamente pelos atendentes da DRI para prevenir dúvidas recorrentes.

## 13. Interface Visual

### IV1. Tela de Alertas Legais, Vistos e Regras Acadêmicas

* **Localização:** Portal Unifor > DRI > Guia de Mobilidade > Regras Legais e Vistos.
* **Leiaute:**
  * Abas de alternância rápida: *Para Estudantes Unifor (Saída)* e *For International Students (Entrada)*.
  * Dois cartões de alerta máximo lado a lado no topo: **Visto de Estudante Obrigatório (Passaporte ≠ Visto)** e **Frequência Mínima de 75% (Sem Exceções)**.
  * Linha do tempo visual de antecedência consular (Carta de Aceite -> Consulado -> Visto -> Passagens/Seguro -> Embarque).
  * Quadro comparativo em duas colunas: *Regras Inegociáveis* vs. *Flexibilidades Acadêmicas (Análise Caso a Caso)*.

## 14. Observações

Este caso de uso endereça diretamente uma das maiores dores relatadas pela DRI na entrevista: evitar que alunos estrangeiros tentem se matricular apenas com passaporte/visto de turismo ou desconheçam a regra brasileira de 75% de frequência.

## 15. Referências

* Documento de Visão da Demanda (VD) — PUMI, Versão 2.0 (23/11/2026), Seções 2.2, 3.2, 3.3, 6 (F2.1, F2.3), 7 (RN01, RN03, RN04, RN05, RN07) e 8.1 (UC4).

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
