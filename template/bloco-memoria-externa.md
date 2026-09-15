# Bloco opcional: memória externa (Expert Brain ou similar)

Cole no fim do seu `CLAUDE.md` se você usa uma memória externa acessível por MCP (o Expert Brain é a que a mentoria usa). Sem memória externa, ignore este bloco: o CLAUDE.md e a memória local do Claude Code já cobrem regra e reflexo; o que falta é conhecimento acumulado, e é isso que este bloco adiciona.

---

## Memória externa — conhecimento (o MCP já explica o próprio schema)

- **Consultar (`recall`):** pergunta temática ou estratégica, decisão com trade-off, "eu já devo ter pensado nisso". Consulta curta, 3 a 7 palavras. NÃO usar em tarefa puramente operacional.
- **Salvar (`save_note`):** decisão (alternativas + por que ganhou), regra, insight, padrão, fato com data, pergunta aberta. Depois de reunião: participantes + decisões + ações. Resumo concreto em uma frase.
- **NÃO salvar:** tarefa (vai pra lista de tarefas), estado que muda toda semana (vira museu), credencial (cofre), debug pontual (commit), duplicata (atualizar a original).
- **Regra-mãe:** só sobrevive o que foi gravado. Anotação mental não passa da compactação de contexto: salvar AGORA, uma ideia por nota, ligada às notas relacionadas.

## Tarefas na memória externa — rota única

- Atividade que eu peço = tarefa: criar ao começar → atualizar nos marcos (não a cada passo) → fechar com o resultado escrito. Antes de criar, buscar se já existe.
- Tarefa nasce com responsável e data. Sem urgência = próxima revisão semanal.
- Entrega que depende da minha aprovação não fecha direto: vai pra "validação humana" e me avisa.
- Insight, decisão e feedback viram nota, não tarefa.

## A divisão que evita bagunça

| Tipo | Onde mora | Quem escreve | Quando carrega |
|---|---|---|---|
| Regra (o que nunca / sempre fazer) | CLAUDE.md | Eu | Toda sessão, inteiro |
| Reflexo (macete de ferramenta, correção de comportamento) | Memória local (`memory/`) | O agente, durante o trabalho | Índice sempre; detalhe sob demanda |
| Conhecimento (decisão com porquê, conceito, contexto de cliente) | Memória externa (Brain) | Os dois | Só quando a pergunta pede (`recall`) |
