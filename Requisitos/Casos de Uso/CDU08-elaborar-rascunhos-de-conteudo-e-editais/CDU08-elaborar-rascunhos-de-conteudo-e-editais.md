# Especificação de Requisitos Funcionais

## Caso de Uso (CDU) - LAPIS

## Histórico de Versões

<!-- markdownlint-disable MD060 -->
| Data       | Versão | Descrição                                                                                                                                    | Autor    |
| ---------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| 26/11/2026 | 1.0    | Criação da especificação do CDU08 (UC8) com base na Visão da Demanda v2.0 do Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI). | Equipe 3 |
<!-- markdownlint-enable MD060 -->

## 1. Nome do Caso de Uso

Elaborar Rascunhos de Conteúdo e Editais

## 2. Objetivo

Permitir que o profissional da Diretoria de Relações Internacionais (DRI) crie, edite e organize minutas de oportunidades/editais, fichas comparativas de destinos, guias de mobilidade, vitrine docente e indicadores estatísticos agregados (incluindo versões prioritárias em inglês), submetendo-os ao fluxo de aprovação editorial do Departamento de Marketing.

## 3. Tipo de Caso de Uso

Concreto

## 4. Atores

### 4.1 Primário

Profissional da DRI (analista ou gestor da Diretoria de Relações Internacionais autenticado no painel administrativo — Persona: Camila).

### 4.2 Secundário

Analista de Marketing (recebe os rascunhos submetidos na fila de revisão editorial — CDU10).

## 5. Precondições

1. O profissional da DRI está autenticado no módulo administrativo do PUMI com permissão de editor da DRI.
2. As diretrizes editoriais e regras de negócio institucionais (RN01 a RN07) estão configuradas no sistema.

## 6. Fluxo Principal

### P1. Acessar o painel administrativo de conteúdos da DRI

O profissional da DRI autentica-se no ambiente administrativo do PUMI e acessa a área **Gestão de Conteúdos e Rascunhos**.

### P2. Listar conteúdos existentes e iniciar novo rascunho

O sistema exibe a listagem de conteúdos da DRI filtráveis por tipo (*Edital/Oportunidade*, *Ficha de Destino*, *Guia/Alerta Legal*, *Vitrine Docente*, *Indicadores Agregados*) e status (*Rascunho*, *Aguardando Aprovação do Marketing*, *Ajustes Solicitados*, *Publicado*), oferecendo o botão **Novo Conteúdo**.

### P3. Selecionar tipo de conteúdo e preencher informações principais

O profissional da DRI seleciona o tipo de artefato (por exemplo, *Novo Edital de Mobilidade*) e preenche os campos estruturados: título, público-alvo, descrição, instituição parceira, cronograma com prazos de antecedência consular (RN05), critérios preliminares de elegibilidade (ex.: PMG), link do canal oficial de inscrição e alertas obrigatórios aplicáveis (RN03 e RN04).

### P4. Vincular tradução estratégica em inglês (quando aplicável)

Para conteúdos destinados à jornada de entrada, manuais de chegada ou apresentação institucional (RN07), o profissional da DRI preenche a aba **Versão em Inglês (*EN*)** vinculada ao mesmo registro.

### P5. Validar conformidade preliminar e submeter para aprovação do Marketing

O profissional da DRI aciona o botão **Submeter para Aprovação do Marketing**. O sistema valida o preenchimento dos campos obrigatórios, verifica a presença da versão em inglês nos conteúdos prioritários (RN07), altera o status do registro para **"Aguardando Aprovação do Marketing"** (RN01) e notifica a fila editorial do Departamento de Marketing.

## 7. Fluxos Alternativos

### A1. Salvar minuta como Rascunho para continuação posterior

* **Ponto de entrada:** Nos passos P3 ou P4, o profissional da DRI ainda não concluiu a elaboração do texto ou aguarda dados de parceiros.
* **A1.1.** O profissional clica em **Salvar Rascunho**.
* **A1.2.** O sistema persiste os dados com status **"Rascunho"** sem enviá-lo ao Marketing e sem exibi-lo no portal público (RN01).
* **Ponto de saída:** Retorna ao passo P2.

### A2. Editar conteúdo devolvido pelo Marketing com parecer de ajustes

* **Ponto de entrada:** No passo P2, o profissional seleciona um item com status **"Ajustes Solicitados"** pelo Departamento de Marketing.
* **A2.1.** O sistema exibe o conteúdo acompanhado do parecer editorial registrado pelo analista de Marketing.
* **A2.2.** O profissional realiza as correções solicitadas e aciona novamente **Submeter para Aprovação do Marketing**.
* **Ponto de saída:** Segue para o passo P5 do fluxo principal.

### A3. Propor atualização ou despublicação de conteúdo já publicado

* **Ponto de entrada:** No passo P2, o profissional seleciona um item com status **"Publicado"** e clica em **Criar Nova Versão / Solicitar Despublicação**.
* **A3.1.** O sistema cria uma minuta de revisão vinculada ao conteúdo vigente mantendo a versão atual no ar até que o Marketing aprove a alteração ou remoção (RN01).
* **Ponto de saída:** Segue para os passos P3 a P5 do fluxo principal.

## 8. Fluxos de Exceção

### E1. Tentativa de submissão sem versão em inglês em conteúdo prioritário

* **Ponto de entrada:** No passo P5, o profissional tenta submeter um conteúdo da categoria *Manual do Estrangeiro*, *Regras Legais de Entrada* ou *Apresentação Institucional* sem preencher os campos obrigatórios em inglês.
* **E1.1.** O sistema bloqueia a submissão e exibe a mensagem: *"Conteúdos da jornada internacional de entrada exigem versão em inglês preenchida antes do envio ao Marketing (RN07)."*
* **Ponto de saída:** Retorna ao passo P4.

### E2. Campos obrigatórios incompletos na submissão

* **Ponto de entrada:** No passo P5, faltam informações essenciais (como prazo de inscrição, canal oficial de candidatura ou datas de antecedência consular).
* **E2.1.** O sistema destaca os campos ausentes e exibe a mensagem: *"Preencha todos os campos obrigatórios antes de submeter o conteúdo para revisão."*
* **Ponto de saída:** Retorna ao passo P3.

## 9. Pós-condições

1. O conteúdo fica salvo no sistema com status **"Rascunho"** ou **"Aguardando Aprovação do Marketing"**.
2. Nenhuma alteração é publicada diretamente no portal público sem a validação explícita do Departamento de Marketing (RN01).

## 10. Requisitos Não Funcionais

1. **Segregação de Perfis e Governança (RN01):** O perfil *Profissional da DRI* não possui permissão técnica de publicação direta em produção; apenas o perfil *Analista de Marketing* pode efetivar o status *Publicado*.
2. **Conformidade LGPD (RN02):** Formulários de indicadores estatísticos aceitam apenas valores numéricos agregados, bloqueando campos de identificação individual.
3. **Auditoria:** Registro de autor, data e hora de criação, edição e submissão de cada versão.

## 11. Ponto de Extensão

Não se aplica.

## 12. Frequência de Utilização

**Média** — Utilizado semanalmente pela equipe da DRI para cadastrar novos editais, atualizar guias, manter a curadoria de periódicos docentes e consolidar estatísticas semestrais.

## 13. Interface Visual

### IV1. Painel Administrativo DRI — Editor de Conteúdos e Rascunhos

* **Localização:** Portal Unifor > Área Administrativa PUMI > Gestão de Conteúdos (DRI).
* **Leiaute:**
  * Tabela gerencial com filtros por Tipo de Conteúdo, Status (etiquetas coloridas: *Rascunho*, *Aguardando Marketing*, *Ajustes Solicitados*, *Publicado*) e Data de Atualização.
  * Formulário em abas: *Dados Gerais (PT)*, *Versão em Inglês (EN)*, *Regras e Prazos* e *Histórico / Pareceres do Marketing*.
  * Barra inferior fixa com ações: *Salvar Rascunho* e *Submeter para Aprovação do Marketing*.

## 14. Observações

Este fluxo implementa diretamente a regra institucional levantada na entrevista com a DRI: a diretoria prepara e organiza o conteúdo técnico, mas toda publicação ou remoção passa pelo crivo visual, textual e de imagem do Departamento de Marketing.

## 15. Referências

* Documento de Visão da Demanda (VD) — PUMI, Versão 2.0 (23/11/2026), Seções 2.2, 3.1, 3.2, 3.3, 5.3 (Persona Camila), 6 (F3.3, F3.5), 7 (RN01 a RN07) e 8.1 (UC8).
* CDU10 — Revisar e Aprovar Publicação Oficial.

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
