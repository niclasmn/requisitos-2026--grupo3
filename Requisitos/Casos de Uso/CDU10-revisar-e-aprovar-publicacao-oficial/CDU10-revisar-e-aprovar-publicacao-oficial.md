# Especificação de Requisitos Funcionais

## Caso de Uso (CDU) - LAPIS

## Histórico de Versões

<!-- markdownlint-disable MD060 -->
| Data       | Versão | Descrição                                                                                                                                    | Autor    |
| ---------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| 26/11/2026 | 1.0    | Criação da especificação do CDU10 (UC10) com base na Visão da Demanda v2.0 do Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI). | Equipe 3 |
<!-- markdownlint-enable MD060 -->

## 1. Nome do Caso de Uso

Revisar e Aprovar Publicação Oficial

## 2. Objetivo

Permitir que o analista do Departamento de Marketing revise os conteúdos submetidos pela DRI (editais, fichas de destinos, guias, vitrine docente, traduções em inglês e indicadores agregados), validando identidade visual, qualidade textual, conformidade com a LGPD e regras institucionais antes de aprovar sua publicação oficial ou devolvê-los para ajustes.

## 3. Tipo de Caso de Uso

Concreto

## 4. Atores

### 4.1 Primário

Analista de Marketing (profissional do Departamento de Marketing da Unifor responsável pela governança editorial e visual — Persona: Mariana).

### 4.2 Secundário

Profissional da DRI (recebe notificação da aprovação ou do parecer de ajustes solicitados).

## 5. Precondições

1. O analista de Marketing está autenticado no ambiente administrativo do PUMI com permissão de aprovador editorial.
2. Existem conteúdos submetidos pela DRI com status **"Aguardando Aprovação do Marketing"** (originados pelo CDU08).

## 6. Fluxo Principal

### P1. Acessar a fila de revisão e aprovação editorial

O analista de Marketing autentica-se no painel administrativo do PUMI e acessa a seção **Fila de Aprovação Editorial (Governança Marketing)**.

### P2. Listar conteúdos pendentes de revisão

O sistema exibe todos os itens com status **"Aguardando Aprovação do Marketing"**, informando título, tipo de conteúdo, autor da DRI, data de submissão e indicativo de versão bilíngue (PT/EN).

### P3. Selecionar conteúdo para revisão e pré-visualização

O analista seleciona um item da fila. O sistema exibe o conteúdo completo em modo de **Pré-visualização Institucional** (simulando a apresentação final no portal Unifor em português e em inglês, quando aplicável) acompanhado de um checklist de conformidade editorial (guia de marca Unifor, qualidade textual, ausência de dados pessoais conforme RN02, presença de alertas obrigatórios RN03/RN04 e qualidade da tradução estratégica RN07).

### P4. Validar conformidade e aprovar publicação oficial

Após verificar que o material atende integralmente aos padrões visuais, textuais e legais da Unifor, o analista de Marketing aciona o botão **Aprovar e Publicar Oficialmente**.

### P5. Efetivar publicação no portal integrado

O sistema altera o status do conteúdo para **"Publicado"**, registra o identificador do aprovador, data e hora da publicação (RN01), disponibiliza imediatamente o conteúdo nas páginas públicas do PUMI integradas ao portal da Unifor e notifica a DRI.

## 7. Fluxos Alternativos

### A1. Solicitar ajustes editoriais ou visuais à DRI

* **Ponto de entrada:** No passo P4, o analista de Marketing identifica inadequação textual, visual, de imagem, tradução ou conformidade institucional.
* **A1.1.** O analista clica em **Devolver para Ajustes**, preenche obrigatoriamente o campo de **Parecer Editorial** descrevendo as correções necessárias e confirma o envio.
* **A1.2.** O sistema altera o status do item para **"Ajustes Solicitados"**, mantém o conteúdo fora do portal público (RN01) e notifica o profissional da DRI (retornando ao fluxo A2 do CDU08).
* **Ponto de saída:** Retorna ao passo P2.

### A2. Aprovar despublicação ou arquivamento de conteúdo vigente

* **Ponto de entrada:** No passo P3, o item submetido pela DRI refere-se a uma solicitação de retirada/arquivamento de conteúdo publicado.
* **A2.1.** O analista valida a pertinência da remoção e aciona **Aprovar Despublicação**.
* **A2.2.** O sistema altera o status do conteúdo público para **"Arquivado"**, retirando-o da navegação pública e preservando o histórico de auditoria (RN01).
* **Ponto de saída:** Retorna ao passo P2.

## 8. Fluxos de Exceção

### E1. Tentativa de devolver conteúdo sem preencher parecer editorial

* **Ponto de entrada:** No fluxo alternativo A1.1, o analista tenta confirmar a devolução deixando o campo de parecer em branco.
* **E1.1.** O sistema bloqueia a ação e exibe a mensagem: *"Informe o parecer editorial detalhando os ajustes necessários para orientar a equipe da DRI."*
* **Ponto de saída:** Retorna ao passo A1.1.

### E2. Identificação de exposição indevida de dados pessoais (LGPD)

* **Ponto de entrada:** No passo P3, o analista identifica nomes, matrículas ou fotos não autorizadas de estudantes no conteúdo submetido.
* **E2.1.** O sistema permite sinalizar a tag de alerta **Conformidade LGPD (RN02)** na devolução para ajustes, impedindo categoricamente a publicação do material.
* **Ponto de saída:** Segue para o fluxo alternativo A1.

## 9. Pós-condições

1. Somente conteúdos explicitamente aprovados pelo Departamento de Marketing tornam-se visíveis ao público no portal integrado da Unifor (RN01).
2. Fica mantida a trilha completa de auditoria (quem elaborou na DRI, quem aprovou no Marketing e quando foi publicado).

## 10. Requisitos Não Funcionais

1. **Controle de Acesso Estrito (RN01):** Apenas usuários autenticados no grupo *Departamento de Marketing* podem transicionar um registro para o estado *Publicado* ou *Arquivado*.
2. **Fidelidade de Pré-visualização:** A pré-visualização deve renderizar exatamente o leiaute responsivo oficial da Unifor antes da publicação.
3. **Rastreabilidade:** Histórico imutável de aprovações e pareceres editoriais.

## 11. Ponto de Extensão

Não se aplica.

## 12. Frequência de Utilização

**Média** — Executado sob demanda sempre que a DRI submete novos editais, atualizações de guias, indicadores semestrais ou revisões de tradução.

## 13. Interface Visual

### IV1. Painel de Governança Editorial — Fila de Aprovação do Marketing

* **Localização:** Portal Unifor > Área Administrativa PUMI > Governança Editorial (Marketing).
* **Leiaute:**
  * Lista de pendências ordenadas por data de submissão com selo de prioridade e idioma (PT / PT+EN).
  * Tela dividida (*split view*): à esquerda, pré-visualização visual fiel da página no portal Unifor (com alternância Desktop/Mobile e PT/EN); à direita, checklist de validação editorial (Marca Unifor, Texto, LGPD, Regras Legais) e botões **Aprovar e Publicar Oficialmente** e **Devolver para Ajustes**.

## 14. Observações

Este caso de uso materializa a governança institucional definida na Visão da Demanda v2.0: garante que o PUMI opere integrado ao site oficial da Unifor sem riscos de imagem, inconsistências visuais ou violações da LGPD.

## 15. Referências

* Documento de Visão da Demanda (VD) — PUMI, Versão 2.0 (23/11/2026), Seções 2.2, 3.1, 3.2, 3.3, 5.5 (Persona Mariana), 6 (F3.4, F3.5), 7 (RN01 a RN07) e 8.1 (UC10).
* CDU08 — Elaborar Rascunhos de Conteúdo e Editais.

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
