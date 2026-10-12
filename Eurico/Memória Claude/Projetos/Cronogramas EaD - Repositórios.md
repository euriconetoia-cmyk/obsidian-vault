---
tags: [projeto, cronograma, wordpress, github]
fonte: GitHub (consultado em 10/10/2026)
---
# Cronogramas EaD — Estado dos Repositórios

Situação em 10/10/2026, lida diretamente do GitHub.

| Repositório | Estado | Observações |
|---|---|---|
| [Cronograma](https://github.com/euriconetoia-cmyk/Cronograma) | Público, 1 commit, só README (vazio) | Site publicado em https://cronograma-azure.vercel.app; 13 pull requests abertos |
| [Cronograma-WP](https://github.com/euriconetoia-cmyk/Cronograma-WP) | **Vazio** (sem nenhum commit) | Era o destino planejado para o plugin + tema + interface WordPress |
| [Cronograma-SENAI-WP](https://github.com/euriconetoia-cmyk/Cronograma-SENAI-WP) | Público, 1 commit na main, 3 PRs | README: "Repositório institucional do sistema Cronogramas EaD para WordPress"; versão 2.19.0 RC1 será publicada em branch de release e validada por Pull Request antes de integrar à main |

## Pontos de atenção
- O `Cronograma-WP` está vazio; o código do sistema parece estar em branches de release do `Cronograma-SENAI-WP` e nos PRs
- O `README.md` do `Cronograma` está em branco

## Decisões já tomadas
- Nome "Unidigital" no lugar de "NIEaD" nos textos
- Crédito: "Criado pela Unidigit@l · By Eurico Cirilo"
- Frontend em React/Vite na pasta `ui/`
- MFA e prazos de retenção da LGPD serão definidos por você

## Fluxo planejado
1. A Unidigit@l cria o cronograma conforme a unidade escolar solicita
2. A unidade valida (ajusta só o cronograma da sua turma)
3. Depois de validado, fica travado até a Unidigit@l reabrir (volta para validação)
4. Exportação em Excel e PDF; login/acessos por unidade

Ver também: [[Memória Claude/Áreas/Cronograma]] · [[Memória Claude/Áreas/Cronogramas EaD]] · [[Memória Claude/Índice]]
