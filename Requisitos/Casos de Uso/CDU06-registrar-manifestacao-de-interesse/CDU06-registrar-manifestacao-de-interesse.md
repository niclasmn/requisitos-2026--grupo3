# CDU06 — Registrar Manifestação de Interesse

## 1. Nome do Caso de Uso
Registrar Manifestação de Interesse

## 2. Objetivo
Permitir que o estudante autenticado registre interesse em uma oportunidade, gerando protocolo para acompanhamento e orientação da DRI, sem substituir a candidatura oficial.

## 3. Atores
- **Primário:** Estudante da Unifor.
- **Secundários:** Serviço de Autenticação Institucional (SSO) e profissional da DRI.

## 4. Fluxo Principal
P1. O estudante aciona Registrar Manifestação de Interesse na oportunidade.
P2. O sistema verifica a autenticação e, se necessário, direciona ao SSO.
P3. O sistema apresenta formulário com dados institucionais e campos complementares, além do aviso de que o registro não é candidatura oficial.
P4. O estudante preenche os dados, confirma ciência e envia.
P5. O sistema valida o registro, salva a manifestação com status Recebida e gera protocolo.
P6. O sistema apresenta o protocolo, resumo e canal oficial de candidatura.

## 5. Checklist de Validação
- [ ] Nome iniciado com verbo no infinitivo.
- [ ] Objetivo claro e direto.
- [ ] Atores identificados.
- [ ] Fluxo principal coerente com o objetivo.
- [ ] Documento revisado.