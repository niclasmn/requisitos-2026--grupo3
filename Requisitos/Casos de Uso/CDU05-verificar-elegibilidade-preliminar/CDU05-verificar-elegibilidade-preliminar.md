# Especificação de Requisitos Funcionais

## Caso de Uso (CDU) - LAPIS

## Histórico de Versões

<!-- markdownlint-disable MD060 -->
| Data       | Versão | Descrição                                                                                                                                    | Autor    |
| ---------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| 26/11/2026 | 1.0    | Criação da especificação do CDU06 (UC6) com base na Visão da Demanda v2.0 do Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI). | Equipe 3 |
<!-- markdownlint-enable MD060 -->

## 1. Nome do Caso de Uso

Verificar Elegibilidade Preliminar

## 2. Objetivo

Permitir que o estudante da Unifor realize uma autodeclaração rápida de seus critérios acadêmicos (como Performance Média Geral — PMG, curso, semestre cursado e nível de proficiência em idioma) para compará-los de forma orientativa com os requisitos exigidos em uma oportunidade de intercâmbio selecionada.

## 3. Tipo de Caso de Uso

Concreto

## 4. Atores

### 4.1 Primário

Estudante Unifor (estudante da Universidade de Fortaleza avaliando sua aderência preliminar a um edital — Persona: Lucas).

### 4.2 Secundário

Não se aplica.

## 5. Precondições

1. O estudante está visualizando uma oportunidade publicada que possui critérios de elegibilidade cadastrados no sistema (originado a partir do CDU02).
2. A oportunidade está ativa/publicada no portal PUMI (RN01).

## 6. Fluxo Principal

### P1. Acionar o verificador preliminar de elegibilidade

Na página de detalhes de uma oportunidade (CDU02), o estudante da Unifor clica no botão **Verificar Minha Elegibilidade Preliminar**.

### P2. Exibir formulário de autodeclaração e aviso orientativo

O sistema exibe o formulário simplificado de autodeclaração contendo os parâmetros exigidos pelo edital (ex.: curso de graduação, semestre atual, Performance Média Geral — PMG, proficiência em idioma) acompanhado de aviso destacado informando o caráter exclusivamente orientativo da simulação (RN06).

### P3. Informar dados acadêmicos autodeclarados

O estudante preenche os campos com seus dados acadêmicos atuais e aciona o comando **Simular Elegibilidade**.

### P4. Validar entradas e comparar com requisitos do edital

O sistema valida o formato dos dados informados (ex.: PMG dentro da escala institucional) e compara cada critério autodeclarado com os parâmetros mínimos cadastrados para a oportunidade.

### P5. Exibir resultado comparativo orientativo

O sistema apresenta o diagnóstico item a item (ex.: *Atende ao requisito*, *Abaixo do mínimo sugerido* ou *Requer comprovação documental*), exibe novamente o aviso explícito de que o resultado não garante aprovação nem substitui a conferência documental oficial da DRI (RN06) e disponibiliza atalho para registrar manifestação de interesse (CDU07) ou acessar o canal oficial de inscrição.

## 7. Fluxos Alternativos

### A1. Simular elegibilidade com novos valores

* **Ponto de entrada:** No passo P5, o estudante deseja testar outro cenário (por exemplo, projeção de PMG ao final do semestre ou certificação de idioma).
* **A1.1.** O estudante clica em **Refazer Simulação**, altera os valores no formulário e reenvia.
* **Ponto de saída:** Retorna ao passo P4 do fluxo principal.

### A2. Prosseguir diretamente para Manifestação de Interesse após diagnóstico positivo

* **Ponto de entrada:** No passo P5, o estudante clica em **Registrar Manifestação de Interesse**.
* **A2.1.** O sistema direciona o estudante para o fluxo do **CDU07 — Registrar Manifestação de Interesse** vinculado à mesma oportunidade.
* **Ponto de saída:** Encerra este caso de uso e inicia o CDU07.

## 8. Fluxos de Exceção

### E1. Valores autodeclarados fora do intervalo válido

* **Ponto de entrada:** No passo P4, o estudante informa um valor inválido (ex.: PMG negativa, acima da nota máxima institucional ou semestre inválido).
* **E1.1.** O sistema bloqueia o cálculo, destaca o campo inválido e exibe a mensagem: *"Informe valores acadêmicos válidos conforme a escala oficial da Unifor (ex.: PMG entre 0,0 e 10,0)."*
* **Ponto de saída:** Retorna ao passo P3 para correção pelo estudante.

### E2. Oportunidade sem critérios objetivos parametrizados

* **Ponto de entrada:** No passo P1, a oportunidade selecionada possui critérios subjetivos ou específicos avaliados integralmente por edital externo.
* **E2.1.** O sistema exibe a mensagem: *"Esta oportunidade possui critérios específicos avaliados diretamente pelo edital parceiro. Consulte a seção de Requisitos e o Canal Oficial de Candidatura."*
* **Ponto de saída:** Encerra o fluxo retornando à visualização do edital.

## 9. Pós-condições

1. O estudante recebe feedback imediato e transparente sobre sua aderência preliminar aos requisitos do edital.
2. Fica registrado visualmente o caráter não vinculante da simulação (RN06), sem armazenamento de dados sensíveis não autorizados (RN02).

## 10. Requisitos Não Funcionais

1. **Privacidade e Minimizacão de Dados (RN02 - LGPD):** Os valores autodeclarados na simulação ocorrem em sessão e não são persistidos em base pública nem vinculados a rankings.
2. **Clareza de Regra de Negócio (RN06):** O aviso de caráter orientativo deve estar visível tanto antes quanto no resultado da verificação.
3. **Tempo de Resposta:** Cálculo e exibição do resultado em menos de 1 segundo.

## 11. Ponto de Extensão

### PE1. Registrar Manifestação de Interesse

* **Ponto de extensão:** Passo P5 (e fluxo alternativo A2).
* **Descrição:** Permite ao estudante que concluiu a verificação preliminar iniciar imediatamente o **CDU07 — Registrar Manifestação de Interesse** na oportunidade consultada.

## 12. Frequência de Utilização

**Alta** — Utilizado pela maioria dos estudantes da Unifor antes de iniciar o processo de candidatura ou manifestar interesse em um edital.

## 13. Interface Visual

### IV1. Modal / Painel de Verificação Preliminar de Elegibilidade

* **Localização:** Portal Unifor > DRI > Detalhes da Oportunidade > Verificar Elegibilidade Preliminar.
* **Leiaute:**
  * Faixa superior de aviso institucional: *"Simulação Orientativa: este resultado não garante aprovação nem substitui a conferência documental oficial da DRI."*
  * Formulário limpo com campos objetivos (Curso, Semestre, PMG, Idioma/Nível).
  * Quadro de resultado com indicadores visuais por critério (ícone verde de conformidade / ícone de atenção) e botões de ação: *Refazer Simulação* e *Registrar Manifestação de Interesse*.

## 14. Observações

Conforme nota de elaboração da Visão da Demanda v2.0, detalhes operacionais específicos como a nota mínima de PMG por edital são parametrizados pela DRI no cadastro de cada oportunidade e sujeitos à validação final do edital vigente.

## 15. Referências

* Documento de Visão da Demanda (VD) — PUMI, Versão 2.0 (23/11/2026), Seções 5.1 (Persona Lucas), 6 (F2.4), 7 (RN02, RN06) e 8.1 (UC6).
* CDU02 — Consultar Editais, Instituições e Mapa.
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
