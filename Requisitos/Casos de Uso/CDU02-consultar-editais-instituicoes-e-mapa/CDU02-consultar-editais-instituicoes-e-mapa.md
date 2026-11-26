# Especificação de Requisitos Funcionais

## Caso de Uso (CDU) - LAPIS

## Histórico de Versões

<!-- markdownlint-disable MD060 -->
| Data       | Versão | Descrição                                                                                                                                    | Autor    |
| ---------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| 26/11/2026 | 1.0    | Criação da especificação do CDU02 (UC2) com base na Visão da Demanda v2.0 do Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI). | Equipe 3 |
<!-- markdownlint-enable MD060 -->

## 1. Nome do Caso de Uso

Consultar Editais, Instituições e Mapa

## 2. Objetivo

Permitir que visitantes, estudantes da Unifor, estudantes estrangeiros e docentes consultem o catálogo unificado de oportunidades de mobilidade, instituições conveniadas, mapa-múndi simplificado e indicadores estatísticos agregados, acessando os detalhes de cada edital e os links dos canais oficiais de candidatura.

## 3. Tipo de Caso de Uso

Concreto

## 4. Atores

### 4.1 Primário

Visitante / Usuário do Portal (Estudante Unifor, Estudante Estrangeiro, Docente Unifor ou Parceiro externo navegando no portal integrado).

### 4.2 Secundário

Não se aplica.

## 5. Precondições

1. O portal PUMI está integrado ao ambiente web oficial da Unifor.
2. Existem oportunidades, instituições conveniadas e indicadores agregados com status **Publicado** após aprovação do Departamento de Marketing (RN01).

## 6. Fluxo Principal

### P1. Acessar o catálogo de oportunidades e instituições

O usuário acessa o portal PUMI e seleciona a seção **Oportunidades, Editais e Instituições Conveniadas** (ou navega por uma das jornadas: *Estude Mundo Afora*, *Do Mundo para a Unifor* ou *Mobilidade Docente*).

### P2. Exibir visão geral, mapa simplificado e indicadores agregados

O sistema apresenta a barra de filtros (público-alvo, modalidade, país, situação do edital e palavra-chave), o mapa-múndi interativo simplificado com destaque para os países conveniados, a lista de oportunidades vigentes e o painel de indicadores agregados de mobilidade (ex.: total de intercambistas enviados e recebidos por período/região, sem dados individuais conforme RN02).

### P3. Filtrar oportunidades ou selecionar país no mapa

O usuário aplica um ou mais filtros (por exemplo, público *Discente*, país *Portugal*, situação *Inscrições Abertas*) ou clica diretamente em um país no mapa-múndi simplificado.

### P4. Atualizar resultados filtrados

O sistema atualiza dinamicamente a listagem exibindo os cartões das oportunidades e instituições conveniadas correspondentes aos critérios selecionados, destacando prazos de inscrição e antecedência consular (RN05).

### P5. Selecionar uma oportunidade ou instituição

O usuário clica em uma oportunidade específica para visualizar seus detalhes completos.

### P6. Exibir ficha detalhada da oportunidade e canal oficial de inscrição

O sistema exibe a página da oportunidade contendo descrição, instituição parceira, público-alvo, requisitos gerais, cronograma com alertas de prazos consulares (RN05), documentos exigidos e o botão/link de direcionamento para o **Canal Oficial de Candidatura** (F2.5), além das opções de verificação preliminar de elegibilidade e manifestação de interesse quando aplicável.

## 7. Fluxos Alternativos

### A1. Pesquisar por termo livre (palavra-chave)

* **Ponto de entrada:** No passo P3, o usuário digita o nome de uma universidade parceira, programa (ex.: *Santander*) ou área de conhecimento no campo de busca textual.
* **A1.1.** O sistema realiza a busca por correspondência no título, instituição parceira, país e resumo das oportunidades publicadas.
* **Ponto de saída:** Segue para o passo P4 do fluxo principal.

### A2. Consultar oportunidades encerradas ou de fluxo contínuo

* **Ponto de entrada:** No passo P3, o usuário altera o filtro de situação para *Encerradas* ou *Fluxo Contínuo* para fins de planejamento histórico.
* **A2.1.** O sistema exibe os editais com a respectiva etiqueta de situação (*Encerrado* ou *Fluxo Contínuo*), mantendo desabilitada a opção de manifestação de interesse para editais encerrados.
* **Ponto de saída:** Segue para o passo P4 do fluxo principal.

### A3. Acessar link externo do canal oficial de candidatura

* **Ponto de entrada:** No passo P6, o usuário clica em **Acessar Canal Oficial de Inscrição**.
* **A3.1.** O sistema exibe breve aviso orientativo informando que o usuário será direcionado ao sistema oficial da Unifor ou da instituição/programa parceiro (ex.: portal Santander) e abre o endereço oficial em nova aba.
* **Ponto de saída:** Encerra o caso de uso.

## 8. Fluxos de Exceção

### E1. Nenhum resultado encontrado para os filtros aplicados

* **Ponto de entrada:** No passo P4, a combinação de filtros selecionados não corresponde a nenhuma oportunidade ou instituição cadastrada.
* **E1.1.** O sistema exibe a mensagem: *"Nenhuma oportunidade encontrada com os filtros selecionados. Limpe os filtros para visualizar todas as oportunidades disponíveis."* e apresenta o botão **Limpar Filtros**.
* **Ponto de saída:** Retorna ao passo P2 após o usuário acionar o botão ou alterar os filtros.

### E2. Oportunidade indisponível ou despublicada durante o acesso

* **Ponto de entrada:** No passo P5, o usuário tenta acessar via link direto uma oportunidade que foi removida ou suspensa após aprovação do Marketing.
* **E2.1.** O sistema exibe a mensagem: *"Esta oportunidade não está mais disponível para consulta pública."* e oferece retorno ao catálogo ativo.
* **Ponto de saída:** Retorna ao passo P2.

## 9. Pós-condições

1. O usuário visualiza as oportunidades, instituições conveniadas, indicadores agregados (em conformidade com a LGPD) e orientações de candidatura oficial.
2. Nenhum dado pessoal de alunos (nomes, matrículas ou documentos) é exibido publicamente (RN02).

## 10. Requisitos Não Funcionais

1. **Conformidade LGPD (RN02):** Os indicadores estatísticos devem exibir exclusivamente números consolidados (totais por ano, curso ou país), bloqueando qualquer dado nominativo.
2. **Padronização Visual:** Uso obrigatório dos componentes visuais e tipografia aprovados pelo Departamento de Marketing da Unifor.
3. **Acessibilidade e Responsividade:** O mapa-múndi simplificado deve possuir alternativa em lista pesquisável para leitores de tela e telas pequenas.

## 11. Ponto de Extensão

### PE1. Verificar Elegibilidade Preliminar

* **Ponto de extensão:** Passo P6 (quando o usuário é Estudante da Unifor e o edital possui critérios cadastrados).
* **Descrição:** Permite ao estudante acionar o **CDU06 — Verificar Elegibilidade Preliminar** para comparar seus dados acadêmicos autodeclarados com os requisitos do edital.

### PE2. Registrar Manifestação de Interesse

* **Ponto de extensão:** Passo P6 (quando o edital está com situação *Aberto* para estudantes da Unifor).
* **Descrição:** Permite ao estudante autenticado acionar o **CDU07 — Registrar Manifestação de Interesse** na oportunidade visualizada.

## 12. Frequência de Utilização

**Alta** — Ponto central de entrada e consulta do portal PUMI durante todo o ano letivo. Os itens mais acessados são editais com inscrições abertas, filtros por país, prazos e links de inscrição.

## 13. Interface Visual

### IV1. Tela de Catálogo de Oportunidades, Mapa Simplificado e Detalhes do Edital

* **Localização:** Portal Unifor > DRI > Oportunidades e Instituições.
* **Leiaute:**
  * Seção superior com painel de indicadores agregados da internacionalização Unifor (números consolidados).
  * Barra horizontal de filtros (Público, Modalidade, País, Situação, Busca).
  * Área visual com mapa-múndi interativo simplificado alternável com grade de cartões de oportunidades.
  * Página interna do edital com abas/blocos organizados: *Visão Geral*, *Requisitos*, *Cronograma e Alertas Consulares*, *Como se Candidatar (Canal Oficial)* e ações de *Verificar Elegibilidade* e *Manifestar Interesse*.

## 14. Observações

O catálogo contempla tanto programas próprios da Unifor quanto oportunidades de parceiros externos (como programas Santander), diferenciando claramente na ficha qual é o canal oficial de submissão da candidatura.

## 15. Referências

* Documento de Visão da Demanda (VD) — PUMI, Versão 2.0 (23/11/2026), Seções 3.2, 6 (F1.1, F1.4, F1.6, F2.5), 7 (RN01, RN02, RN05) e 8.1 (UC2).
* CDU06 — Verificar Elegibilidade Preliminar.
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
