---
tags: [memoria-claude, projeto, skills]
aliases: [skill-creator]
fonte: memória do Claude
atualizado: 2026-09-09
---
# Empacotamento de Skills

Detalhes técnicos para criar, validar e empacotar skills do Claude.

- Trabalha em um ambiente de projeto do Claude que suporta empacotamento de skills
- Os scripts devem ser executados a partir de `/mnt/skills/examples/skill-creator/` como diretório de trabalho (dependência de import relativo)
- Validar uma skill: `cd /mnt/skills/examples/skill-creator && python3 -m scripts.quick_validate <caminho-absoluto-da-pasta-da-skill>`
- Empacotar uma skill: `python3 -m scripts.package_skill <caminho-absoluto-da-pasta-da-skill> <pasta-de-saída>`

## Regras do frontmatter do SKILL.md
- `name` deve estar em kebab-case e ter até 64 caracteres, sem sublinhados, maiúsculas ou caracteres especiais
- `description` deve ter até 1.024 caracteres e não pode conter `<` ou `>` (ângulos no corpo do texto são permitidos)

Voltar: [[Visão Geral]]
