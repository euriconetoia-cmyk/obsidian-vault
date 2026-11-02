---
tags: [memoria-claude, area, extensao-chrome, moodle, senai]
aliases: [extensão Chrome por blocos, extensão orquestradora, Ferramentas EaD SENAI, Blocos EaD SENAI]
fonte: memória do Claude
atualizado: 2026-11-01
---
# Unidigit@l Assist (extensão do Chrome)

Extensão do Chrome que reúne as ferramentas do Eurico para o Moodle num só lugar. Começou como ideia de uma extensão por blocos (Blockly) que chamaria outras extensões (pesquisa inicial em out/2026).

## Linha do tempo das decisões
- **30/10** — Reunir todas as extensões numa única extensão (não comandar as outras). Primeira ideia: editor em painel lateral, 1ª versão com os blocos do Importar Notas; módulo "Alunos e notas" (somente leitura) depois; nome provisório "Blocos EaD SENAI".
- **30/10 (correção)** — Botão sempre na lateral da página do Moodle e, dentro dele, as aplicações (Pendências, Correção, Acompanhamento, Alunos e notas), cada uma executada ao clicar. O editor de blocos fica como mais um item do menu, para depois. Nome provisório "Ferramentas EaD SENAI".
- **30/10** — Menu do botão lateral flutuante, com cards (estilo de exemplo que ele mandou). Em vez de "Fechamento da UC", um "Relatório da UC" (desempenho e notas por aluno). Quer integrar também a extensão "Ajustar datas Moodle" (1.3.4), possivelmente num botão Configurações, após análise de viabilidade, confiabilidade, acessibilidade e integração.
- **30/10** — Manter salvas as versões atuais das extensões avulsas (Importar Notas, Assistente EaD) e, daqui em diante, atualizar sempre a ferramenta modular, integrando as outras num único lugar. Quer também saída em página HTML animada a partir de Notas.
- **30/10** — Telas o mais simples, eficientes e intuitivas possível; botão de "continuar" nas partes que falharam em toda tela que exige leitura de dados (como no Importar Notas). A saída de Notas será HTML para baixar, mantendo as telas do painel. "Ajustar datas Moodle" fica para depois.
- **31/10** — Nome escolhido: **"Unidigit@l Assist"** (substitui o provisório). Quer repositório git no GitHub (conta euriconetoia-cmyk) para facilitar as atualizações.
- **31/10** — Repositório euriconetoia-cmyk/Unidigit-l-Assist, **público, licença MIT**; quer um pedido de ⭐ nas instruções de instalação do README (não dentro da extensão).
- **31/10** — Do repositório senai-extensoes (Julio Alves) quer aproveitar o Excel (.xlsx) e o relatório de notas por turma; descartou o módulo Drive PDF; quer incluir o Kahoot (importar perguntas por CSV) num novo campo "Ferramentas" no menu, onde caibam outras utilidades.
- **31/10** — Julio Alves entra como coautor ao lado dele nos créditos. Gostou das sugestões de evolução: relatório de compatibilidade, modelos de mensagem, retornos agendados, comparativo entre leituras, resumo do dia, ajustes/régua de nota, backup "Meus dados" e tela "Sobre". Perguntou sobre publicar na loja do Edge para atualização automática gratuita (todos os tutores usariam Edge, a confirmar).
- **31/10** — Adiou a publicação na loja do Edge ("por enquanto não vamos fazer a parte do Edge"); distribuição segue por ZIP/GitHub. Mandou publicar no GitHub as versões até a 0.16 (Resumo do dia, Ajustes por UC e régua de nota já feitos).
- **31/10** — Retomou "Ajustar datas": a extensão deve ler o cronograma da página do curso e as datas das atividades no Moodle, comparar e permitir ajustar (editável, com sugestões pelo cronograma). Viu o mockup e aguarda decidir regras de campos, tipos de atividade e se começa só por ler/comparar. Pediu manter a mesma numeração de versão (0.16.0) por enquanto.

Relacionado: [[Memória Claude/Áreas/Moodle e Apoio ao Docente]] · [[Memória Claude/Projetos/Assistente EaD SENAI]] · [[Memória Claude/Áreas/Cronogramas EaD]]
Ver também: [[Memória Claude/Índice]]
