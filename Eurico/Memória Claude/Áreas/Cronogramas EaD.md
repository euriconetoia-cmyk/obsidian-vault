---
tags: [memoria-claude, area, cronograma, wordpress]
aliases: [Cronograma-WP]
fonte: memória do Claude
atualizado: 2026-11-01
---
# Cronogramas EaD

Sistema que o Eurico está construindo para a Unidigit@l (SENAI).

## Visão geral
- "Cronogramas EaD": plugin + tema WordPress; crédito "Criado pela Unidigit@l · By Eurico Cirilo"
- Quer subir para o repositório euriconetoia-cmyk/Cronograma-WP
- Código-fonte do frontend (React/Vite em ui/) está no repositório euriconetoia-cmyk/Cronograma-SENAI-WP (branches de release); quer que as correções da auditoria sejam aplicadas ao sistema
- Política de MFA e prazos de retenção da LGPD são decisões que ele mesmo vai estabelecer
- Pede para ver as especificações e uma prévia visual antes de implementar mudanças no sistema

## Infraestrutura
- O sistema vai enviar e-mails pela conta Microsoft 365 / Outlook da Unidigit@l
- O site WordPress do sistema está hospedado na HostGator

## Decisões
- Uma única instalação para vários estados (divisão por DR), com interlocutor por DR que só acompanha; o catálogo de cursos continua único
- Motivo de alteração obrigatório, em lista fechada
- Métrica de dashboard: % de UCs com data mudada, separando antes e depois do início
- **Aprendizagem:** o sistema calcula o cronograma do contrato completo (teoria + prática na empresa, férias, término); dados do contrato editáveis por turma; teoria EaD tratada como síncrona em todos os dias de teoria
- **Integração com Moodle:** no Moodle a turma inteira é um curso, com as UCs dentro, comparadas pelo nome; nome do curso no formato "código - Curso - nº/ano" (código do Moodle / nº do evento, não a OS); o Cronograma-WP vai exportar o código do curso no JSON; `terminoAva` vira o fim do curso no Moodle

Relacionado: [[Memória Claude/Áreas/Cronograma]] · [[Memória Claude/Áreas/Gestão da Tutoria EaD]] · [[Memória Claude/Áreas/Unidigit@l Assist]] · [[Memória Claude/Projetos/Cronogramas EaD - Repositórios]]
Ver também: [[Memória Claude/Índice]]
