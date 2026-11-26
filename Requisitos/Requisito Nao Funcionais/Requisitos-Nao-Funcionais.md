# Especificação de Requisitos Não Funcionais — Portal Unificado de Oportunidades e Mobilidade Internacional (PUMI)

**Instituição:** Universidade de Fortaleza (Unifor)  
**Disciplina / Contexto:** T193-16 — Requisitos e Modelagem de Sistemas  

---

## Histórico de Versões

| Data | Versão | Descrição | Autor |
|---|---:|---|---|
| 23/11/2026 | 1.0 | Especificação inicial dos Requisitos Não Funcionais (RNF) do PUMI a partir da Visão da Demanda v2.0 e do Glossário. | Equipe 3 |

---

## Requisitos Não Funcionais

| ID | Categoria | Requisito Não Funcional | Critério / Diretriz de Verificação |
|---|---|---|---|
| **RNF01** | Integração Institucional | O PUMI deve operar como módulo integrado ao ecossistema web oficial da Unifor e da DRI, e não como site externo isolado. | Navegação, cabeçalho/identidade e URLs integrados ao domínio/ambiente institucional da Unifor. |
| **RNF02** | Identidade Visual e Marca | Todas as interfaces públicas e pré-visualizações devem seguir o guia de marca vigente e os padrões gráficos aprovados pelo Departamento de Marketing da Unifor. | Validação editorial e visual nas telas de jornada, quiz, comparador, catálogos e guias (RN01). |
| **RNF03** | Segurança e Privacidade (LGPD) | A aplicação deve cumprir a LGPD (Lei nº 13.709/2018), utilizando HTTPS, minimização de dados, controle de acesso por perfil e anonimização estrita de estatísticas públicas. | Nenhuma exposição pública de dados individuais; registros de interesse acessíveis apenas a perfis autorizados (RN02). |
| **RNF04** | Controle de Acesso e Governança | O sistema deve impor segregação de papéis entre Visitante, Estudante Unifor, Estudante Estrangeiro, Docente, Profissional da DRI e Analista de Marketing. | Somente Analista de Marketing aprova/publica no portal; dados de protocolos restritos à DRI e ao titular (RN01, RN02). |
| **RNF05** | Responsividade | A aplicação web deve adaptar-se adequadamente a diferentes resoluções e dispositivos (desktop, tablet e smartphone), incluindo tabelas comparativas e guias de campo. | Layout sem quebra horizontal em telas móveis e visualização clara das fichas comparativas e mapas/listas. |
| **RNF06** | Acessibilidade (WCAG) | As páginas e componentes devem atender às diretrizes de acessibilidade web (WCAG), com suporte a navegação por teclado, contraste adequado e estrutura semântica. | Alternativa textual/lista acessível para o mapa-múndi simplificado e rótulos semânticos em formulários. |
| **RNF07** | Desempenho | As consultas de catálogo, filtros, cálculos de afinidade do quiz e verificações preliminares de elegibilidade devem responder com agilidade. | Tempo de resposta percebido em até 2 segundos em condições normais de uso (e < 1 segundo na simulação de elegibilidade). |
| **RNF08** | Internacionalização e Idioma | O portal deve priorizar conteúdo em inglês nas páginas essenciais para mobilidade de entrada, manuais e visão institucional, mantendo clareza sobre o escopo de tradução. | Páginas da jornada de entrada, alertas legais essenciais e guia de Fortaleza disponíveis em inglês (RN07). |
| **RNF09** | Rastreabilidade e Auditoria | Operações de criação, submissão, aprovação/rejeição editorial e alteração de status de manifestações devem registrar autoria, data/hora e histórico básico. | Log de movimentações nos rascunhos/aprovações (DRI/Marketing) e nos protocolos de manifestação de interesse. |
