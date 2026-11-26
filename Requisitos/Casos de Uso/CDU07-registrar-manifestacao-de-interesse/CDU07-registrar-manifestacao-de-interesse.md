# Especificação de Requisitos Funcionais

## Caso de Uso (CDU) - LAPIS

## Histórico de Versões

<!-- markdownlint-disable MD060 -->
| Data       | Versão | Descrição                                                                                                                                    | Autor    |
| ---------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| 26/11/2026 | 1.0    | Criação da especificação do CDU07 (UC7) com base na Visão da Demanda v2.0 do Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI). | Equipe 3 |
<!-- markdownlint-enable MD060 -->

## 1. Nome do Caso de Uso

Registrar Manifestação de Interesse

## 2. Objetivo

Permitir que o estudante da Unifor autenticado registre de forma simplificada sua manifestação de interesse em uma oportunidade publicada, gerando um número de protocolo para acompanhamento e triagem pela DRI, com aviso explícito de que o registro não substitui a candidatura oficial.

## 3. Tipo de Caso de Uso

Concreto

## 4. Atores

### 4.1 Primário

Estudante Unifor (estudante regularmente vinculado à Universidade de Fortaleza — Persona: Lucas).

### 4.2 Secundário

1. Serviço de Autenticação Institucional Unifor / SSO (valida a identidade do estudante).
2. Profissional da DRI (recebe o registro na fila de atendimento para triagem e orientação — CDU09).

## 5. Precondições

1. O estudante possui vínculo ativo e credenciais válidas no ambiente institucional da Unifor.
2. A oportunidade selecionada está publicada e com período de interesse aberto no portal PUMI (RN01).

## 6. Fluxo Principal

### P1. Iniciar registro de manifestação de interesse

Na página de uma oportunidade ativa (CDU02 ou após o CDU06), o estudante aciona o botão **Registrar Manifestação de Interesse**.

### P2. Verificar autenticação institucional

O sistema verifica se o estudante possui sessão autenticada; caso não esteja autenticado, redireciona para o login institucional da Unifor (SSO) e retorna à oportunidade após autenticação bem-sucedida.

### P3. Exibir formulário simplificado e termo informativo

O sistema exibe o formulário pré-preenchido com os dados institucionais básicos do estudante (nome, matrícula, curso e e-mail institucional, protegidos sob LGPD conforme RN02), campos complementares de triagem (telefone/WhatsApp opcional, disponibilidade de semestre e breve dúvida/observação) e o **Aviso Obrigatório** informando que a manifestação de interesse serve para orientação inicial da DRI e **não equivale à candidatura oficial** (F3.1).

### P4. Preencher informações complementares e confirmar envio

O estudante revisa seus dados, marca o aceite de ciência sobre o caráter orientativo e tratamento de dados (LGPD), e clica em **Confirmar Manifestação de Interesse**.

### P5. Validar dados, persistir registro e gerar protocolo

O sistema valida a ausência de duplicidade ativa para a mesma oportunidade, grava a manifestação com status inicial **"Recebida"**, registra data/hora e gera um código único de protocolo.

### P6. Exibir comprovante de protocolo e direcionamento oficial

O sistema apresenta a tela de confirmação contendo o número do protocolo gerado, o resumo da solicitação, o lembrete de prazos consulares (RN05) e o botão destacado com o link e instruções do **Canal Oficial de Candidatura** (F2.5).

## 7. Fluxos Alternativos

### A1. Consultar manifestações de interesse já registradas pelo próprio estudante

* **Ponto de entrada:** No passo P1 ou após o passo P6, o estudante acessa a área **Minhas Manifestações de Interesse**.
* **A1.1.** O sistema lista exclusivamente as manifestações vinculadas à matrícula do estudante autenticado, exibindo protocolo, oportunidade, data de envio e situação atual (*Recebida*, *Em orientação*, *Concluída* ou *Cancelada*).
* **Ponto de saída:** Encerra o fluxo ou retorna ao catálogo de oportunidades.

### A2. Cancelar manifestação de interesse ainda não concluída

* **Ponto de entrada:** No fluxo alternativo A1, o estudante seleciona uma manifestação com status *Recebida* ou *Em orientação* e clica em **Cancelar Manifestação**.
* **A2.1.** O sistema solicita confirmação, atualiza o status do registro para **"Cancelada"** e registra a data/hora da alteração.
* **Ponto de saída:** Retorna à listagem do fluxo alternativo A1.

## 8. Fluxos de Exceção

### E1. Falha na autenticação institucional (SSO)

* **Ponto de entrada:** No passo P2, o estudante informa credenciais inválidas ou não possui vínculo discente elegível.
* **E1.1.** O serviço de autenticação exibe mensagem de erro de credenciais ou perfil não autorizado, impedindo o acesso ao formulário de manifestação.
* **Ponto de saída:** Encerra o fluxo mantendo o usuário na visão pública da oportunidade.

### E2. Manifestação de interesse já registrada para a mesma oportunidade

* **Ponto de entrada:** No passo P5, o sistema identifica que o estudante já possui uma manifestação ativa (*Recebida* ou *Em orientação*) para o mesmo edital.
* **E2.1.** O sistema impede a criação de registro duplicado e exibe a mensagem: *"Você já possui uma manifestação de interesse ativa para esta oportunidade (Protocolo nº XXXXX). Acompanhe o andamento em Minhas Manifestações."*
* **Ponto de saída:** Encerra o fluxo direcionando para o acompanhamento do protocolo existente.

### E3. Campos obrigatórios ou aceite de ciência não marcados

* **Ponto de entrada:** No passo P4, o estudante tenta confirmar o envio sem preencher campo obrigatório ou sem marcar o termo de ciência.
* **E3.1.** O sistema destaca os itens pendentes e exibe a mensagem: *"Para registrar seu interesse, preencha os campos obrigatórios e confirme ciência de que este registro não substitui a inscrição oficial."*
* **Ponto de saída:** Retorna ao passo P4.

## 9. Pós-condições

1. A manifestação de interesse fica armazenada com protocolo único e status **"Recebida"** na fila de atendimento da DRI (CDU09).
2. O estudante recebe o número de protocolo e o link direto para o canal oficial de candidatura.
3. Os dados pessoais coletados permanecem restritos ao ambiente autenticado e à equipe autorizada da DRI (RN02).

## 10. Requisitos Não Funcionais

1. **Segurança e Privacidade (LGPD - RN02):** Tráfego criptografado (HTTPS), acesso restrito ao próprio estudante e aos perfis autorizados da DRI, sem qualquer exposição pública.
2. **Integração Institucional:** Uso do mecanismo de autenticação oficial da Unifor (SSO), sujeito à definição técnica final com a equipe de TI.
3. **Confiabilidade:** Garantia de unicidade do número de protocolo gerado.

## 11. Ponto de Extensão

Não se aplica.

## 12. Frequência de Utilização

**Alta** — Durante os períodos de editais abertos, concentrando o fluxo inicial de triagem que anteriormente ocorria por e-mails dispersos.

## 13. Interface Visual

### IV1. Formulário de Manifestação de Interesse e Comprovante de Protocolo

* **Localização:** Portal Unifor > DRI > Oportunidade > Manifestar Interesse.
* **Leiaute:**
  * Cabeçalho com identificação da oportunidade selecionada.
  * Caixa de destaque informativo: *"Atenção: este registro facilita o atendimento orientativo pela DRI, mas NÃO substitui sua inscrição no canal oficial do edital."*
  * Dados acadêmicos pré-carregados (somente leitura) + campo de observação/dúvida + checkbox de ciência.
  * Tela final de sucesso com cartão do **Número de Protocolo**, status *Recebida* e botão primário **Ir para Candidatura Oficial**.

## 14. Observações

A integração técnica do Single Sign-On (SSO) está sinalizada na nota de elaboração da Visão da Demanda v2.0 para validação final com a equipe de TI da Unifor.

## 15. Referências

* Documento de Visão da Demanda (VD) — PUMI, Versão 2.0 (23/11/2026), Seções 2.2, 3.2, 5.1 (Persona Lucas), 6 (F2.5, F3.1), 7 (RN01, RN02, RN05) e 8.1 (UC7).
* CDU02 — Consultar Editais, Instituições e Mapa.
* CDU09 — Gerenciar Manifestações de Interesse.

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
