# claude-md-do-eric — CLAUDE.md do projeto

Objetivo: material de aula da Mentoria Automações Inteligentes sobre o arquivo CLAUDE.md — o que é, o que entra, o que não entra e como ele se mantém pequeno. Traz o template pronto pra copiar e a versão comentada (e higienizada) do CLAUDE.md global do Eric.

- Repositorio canonico: github.com/Expert-Integrado-Ferramentas/claude-md-do-eric (cópia pro aluno em `Expert-Integrado-Alunos/claude-md-do-eric`, publicada pelo robô `publicador`).
- Escopo: `README.md` (a aula), `template/` (CLAUDE.md pra copiar + bloco opcional de memória externa), `exemplo-eric/` (o arquivo real, comentado, sem dado sensível), `exercicio-em-aula.md`.
- Fora de escopo: hooks, skills, MCPs e o repositório de configuração do Eric (claude-stack) — são aulas próprias.
- Regra de higiene: NADA de telefone, endereço, ID de sistema, nome de cliente, preço, pessoa da equipe ou segredo. Antes de commitar, `grep -nE '[0-9]{10,}|op://|@|R\$' -r .` tem que voltar só o que for exemplo genérico.
- Texto pro aluno com acentuação normal. O CLAUDE.md real do Eric é sem acento por convenção dele; o template não herda essa convenção.
