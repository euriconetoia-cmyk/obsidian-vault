---
tags: [projeto, moodle, senai, extensao-chrome]
aliases: [Assistente-EaD-SENAI, Assistente-Tutor-SENAI]
repositorio: https://github.com/euriconetoia-cmyk/Assistente-EaD-SENAI
versao: 3.7.16
fonte: README do GitHub (consultado em 10/10/2026)
---
# Assistente EaD SENAI 3.7.16

Extensão Chrome (Manifest V3) para acompanhamento da tutoria nos ambientes Moodle autorizados do SENAI e da FIEG.

- Repositório: https://github.com/euriconetoia-cmyk/Assistente-EaD-SENAI (público, 45 commits, 12 issues, 3 PRs)
- Domínios autorizados: `https://ead.senai.br/*` e `https://ead.fieg.com.br/*`
- Repositório antigo: https://github.com/euricociriloia-dotcom/Assistente-Tutor-SENAI

## Recursos
- Painel isolado por Shadow DOM, responsivo, acessível, com temas claro, escuro e do sistema
- Acompanhamento de alunos, atividades, notas, pendências, histórico e fechamento de UC
- "Minha jornada" na Visão geral: análise, correção, acompanhamento, lançamento, conferência e auditoria, com até três próximas ações e fila completa
- Importação contextual com prévia, validação de notas e confirmação em duas etapas
- Correção em lote transacional, retomável após suspensão do service worker e bloqueada quando houver correspondência incompleta
- Conferência pós-salvamento: relê nota e feedback no Moodle e mostra divergências por aluno
- Associação de atividades somente por CMID ou nome normalizado exato (sugestões aproximadas nunca são salvas automaticamente)
- Exportações CSV protegidas contra fórmulas de planilha
- Retenção local configurável e opção de desativar o armazenamento do texto das mensagens
- Central de Gestão em página própria: dez áreas, filtros globais, calendário, fila de trabalho, histórico e relatórios CSV, JSON e PDF
- Auditoria Local em linha do tempo, com filtros por período, resultado, tipo de ação e pesquisa
- Pasta de evidências com autorização explícita do Chrome (fallback em ZIP)
- Pacote de auditoria: relatório HTML, CSV, JSON, manifesto e hashes SHA-256
- Pacote para correção com IA: texto da tarefa, anexos, recurso Arquivo "SAP" da mesma UC, critérios, nota máxima, manifesto e ZIPs das entregas

## Correção por IA e notas
- O CSV pode trazer `desempenho_0_100` por aluno, com `nota` vazia
- O importador calcula `desempenho_0_100 ÷ 100 × nota_maxima` e permite editar a nota final antes do envio
- A escala máxima deve ser confirmada na atividade ou no manifesto; conflito ou falta de confirmação impede a conversão
- Nunca preencher `nota` e `desempenho_0_100` na mesma linha
- Desempenho zero ou atividade incorreta gera somente feedback; SENAI Play validado segue a regra da nota máxima confirmada

## Operações que alteram o Moodle
- O painel começa em **Modo de consulta**
- Importações e lotes mostram prévia, deixam sobrescrita desativada e exigem confirmação explícita
- Só considera sucesso quando o Moodle apresenta confirmação verificável; sem confirmação, fica como erro para revisão manual

## Instalação para homologação
1. Abrir `chrome://extensions`
2. Ativar o modo do desenvolvedor
3. **Carregar sem compactação** e selecionar a pasta
4. Conferir a versão `3.7.16`; ao atualizar, substituir os arquivos, clicar em **Recarregar** e atualizar as abas do Moodle
5. Validar primeiro em curso de homologação, com uma atividade e um aluno de teste

## Validação e integridade
- `npm test`, `npm run validate`, `npm run integrity`, `npm run checksums`
- `CHECKSUMS.sha256` identifica o conteúdo versionado
- Contribuições devem manter os créditos em `CREDITOS.md` e descrever alterações em `CHANGELOG.md`

## Estrutura do repositório
- `background/service-worker.js`: coordenador transacional e retomável
- `content/shared-validation.js`: parser, validações, associação exata e proteção CSV
- `content/importer/`: importação contextual na avaliação rápida
- `content/ui.js` e `content/styles.css`: painel isolado e sistema visual
- `dashboard/`: Central de Gestão (inclui `directory-access.js` e `audit-export.js`)
- `tests/`: testes unitários, de integração simulada e estruturais
- `scripts/validate-extension.js`: auditoria automática do pacote
- `docs/`: especificações, planos e relatórios (há um índice em `docs/README.md`)
- Arquivos na raiz: `CHANGELOG.md`, `CLAUDE.md`, `CREDITOS.md`, `PRIVACIDADE.md`, `VALIDACAO.md`, `manifest.json`, `package.json`

## Privacidade
- Dados acadêmicos ficam no armazenamento local do navegador pelo período configurado
- Senhas e tokens não são coletados
- O texto das mensagens é guardado localmente por padrão em instalações novas (pode ser desativado em Diagnóstico)

Ver também: [[Memória Claude/Áreas/Moodle e Apoio ao Docente]] · [[Memória Claude/Índice]]
