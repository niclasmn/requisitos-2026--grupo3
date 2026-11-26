# Especificação de Requisitos Funcionais

## Caso de Uso (CDU) - LAPIS

## Histórico de Versões

<!-- markdownlint-disable MD060 -->
| Data       | Versão | Descrição                                                                                                                                    | Autor    |
| ---------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| 26/11/2026 | 1.0    | Criação da especificação do CDU09 (UC9) com base na Visão da Demanda v2.0 do Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI). | Equipe 3 |
<!-- markdownlint-enable MD060 -->

## 1. Nome do Caso de Uso

Gerenciar Manifestações de Interesse

## 2. Objetivo

Permitir que o profissional da Diretoria de Relações Internacionais (DRI) visualize, filtre, acompanhe e atualize o status de atendimento das manifestações de interesse registradas pelos estudantes da Unifor, organizando a triagem inicial e o direcionamento aos canais oficiais.

## 3. Tipo de Caso de Uso

Concreto

## 4. Atores

### 4.1 Primário

Profissional da DRI (analista ou atendente da DRI autenticado no painel administrativo — Persona: Camila).

### 4.2 Secundário

Estudante Unifor (visualiza a atualização do status de seu protocolo na área autenticada).

## 5. Precondições

1. O profissional da DRI está autenticado no ambiente administrativo do PUMI.
2. Existem manifestações de interesse registradas pelos estudantes (originadas pelo CDU07).

## 6. Fluxo Principal

### P1. Acessar o painel de gestão de manifestações de interesse

O profissional da DRI acessa o ambiente administrativo do PUMI e seleciona o módulo **Manifestações de Interesse**.

### P2. Exibir indicadores de fila e listagem de protocolos

O sistema apresenta o resumo quantitativo por situação (*Recebida*, *Em orientação*, *Concluída*, *Cancelada*) e a tabela paginada com as manifestações registradas, exibindo número de protocolo, data de registro, oportunidade vinculada, nome e curso do estudante (visíveis apenas internamente conforme RN02) e status atual.

### P3. Filtrar manifestações por oportunidade, status ou protocolo

O profissional da DRI aplica filtros por edital/oportunidade, status de atendimento, período ou busca pelo número de protocolo/matrícula.

### P4. Selecionar uma manifestação para triagem

O profissional seleciona um registro específico para visualizar seus detalhes completos.

### P5. Exibir detalhes da solicitação e histórico de atendimento

O sistema exibe os dados acadêmicos do estudante, a observação ou dúvida registrada no momento da manifestação e o histórico de movimentações do protocolo.

### P6. Atualizar status de atendimento e registrar nota interna

O profissional seleciona o novo status de atendimento (**"Em orientação"**, **"Concluída"** ou **"Cancelada"**), registra uma nota interna de acompanhamento (ex.: *Orientado sobre prazos consulares e direcionado ao edital oficial*) e aciona **Salvar Atualização**. O sistema grava a alteração com data/hora e responsável, atualizando o status visível ao estudante.

## 7. Fluxos Alternativos

### A1. Exportar relatório gerencial consolidado (CSV/Excel)

* **Ponto de entrada:** No passo P2, o profissional da DRI clica em **Exportar Consolidado**.
* **A1.1.** O sistema gera arquivo tabular com os registros filtrados para controle interno da DRI, registrando log de auditoria da exportação em conformidade com a LGPD (RN02).
* **Ponto de saída:** Retorna ao passo P2.

### A2. Filtrar apenas manifestações pendentes de primeiro contato

* **Ponto de entrada:** No passo P3, o profissional seleciona o filtro rápido **Aguardando Triagem (*Status: Recebida*)**.
* **A2.1.** O sistema ordena as solicitações da mais antiga para a mais recente para priorização do atendimento.
* **Ponto de saída:** Segue para o passo P4 do fluxo principal.

## 8. Fluxos de Exceção

### E1. Nenhum protocolo encontrado para os filtros informados

* **Ponto de entrada:** No passo P3, o número de protocolo ou combinação de filtros não retorna registros.
* **E1.1.** O sistema exibe a mensagem: *"Nenhuma manifestação de interesse encontrada para os critérios informados."* e oferece opção para limpar os filtros.
* **Ponto de saída:** Retorna ao passo P2.

### E2. Tentativa de alterar manifestação já cancelada pelo estudante

* **Ponto de entrada:** No passo P6, o registro foi cancelado pelo estudante (fluxo A2 do CDU07) enquanto a tela estava aberta.
* **E2.1.** O sistema impede a sobrescrita indevida e exibe a mensagem: *"Esta manifestação foi cancelada pelo estudante e não permite novas alterações de status."*
* **Ponto de saída:** Retorna ao passo P2.

## 9. Pós-condições

1. O status da manifestação de interesse é atualizado e auditado no sistema.
2. O estudante pode visualizar o andamento atualizado de seu protocolo.
3. Os dados pessoais dos interessados permanecem protegidos em ambiente restrito da DRI (RN02).

## 10. Requisitos Não Funcionais

1. **Proteção de Dados Pessoais (RN02 - LGPD):** O acesso à lista nominal de interessados é estritamente restrito a usuários autenticados com perfil DRI, com registro de log de acesso e alteração.
2. **Usabilidade Operacional:** Filtros rápidos por edital e status para reduzir o tempo de triagem da equipe.

## 11. Ponto de Extensão

Não se aplica.

## 12. Frequência de Utilização

**Alta** — Utilizado diariamente pela equipe da DRI durante períodos de divulgação de oportunidades e orientação pré-candidatura.

## 13. Interface Visual

### IV1. Painel Administrativo DRI — Gestão de Manifestações de Interesse

* **Localização:** Portal Unifor > Área Administrativa PUMI > Manifestações de Interesse.
* **Leiaute:**
  * Cartões de contagem rápida no topo: *Recebidas*, *Em Orientação*, *Concluídas* e *Canceladas*.
  * Barra de filtros (Oportunidade, Status, Período, Busca por Protocolo/Aluno).
  * Tabela de protocolos com ação rápida *Atender / Atualizar Status*.
  * Painel lateral (*drawer*) de detalhes do protocolo com histórico de atendimento, seletor de novo status e campo de anotação interna.

## 14. Observações

A gestão centralizada de manifestações substitui o controle informal disperso em caixas de e-mail, permitindo à DRI medir a demanda por oportunidade e alimentar os indicadores agregados (sem dados pessoais) exibidos no portal.

## 15. Referências

* Documento de Visão da Demanda (VD) — PUMI, Versão 2.0 (23/11/2026), Seções 2.2, 3.2, 5.3 (Persona Camila), 6 (F3.2), 7 (RN02) e 8.1 (UC9).
* CDU07 — Registrar Manifestação de Interesse.

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
