# Exercício em aula: escreva o seu CLAUDE.md em 40 minutos

Faça na ordem. Cada bloco tem um teto de linhas de propósito: arquivo curto obedece melhor.

## 1. Suas 5 hard rules (10 min)

Pense nos 5 erros que o agente já cometeu com você (ou que você mais teme). Cada um vira uma regra:

- Verificável: alguém consegue dizer se foi cumprida ou não.
- Gatilho + ação + exceção.
- NUNCA / SEMPRE só onde é inegociável.

Exemplo ruim: "Seja cuidadoso com mensagens."
Exemplo bom: "Mensagem pra cliente NUNCA sai sem 1 OK meu no chat, mesmo que eu tenha dito 'pode mandar' antes."

## 2. Quem eu sou (5 min, até 6 linhas)

- Nome, empresa, papel.
- Como você trabalha (direto ou detalhado; quer que faça ou que explique).
- Como você manda o pedido (texto ou áudio). Se áudio: a regra do erro de transcrição.
- Tom de resposta que você quer receber.
- O que é decisão SUA e o que o agente decide sozinho.

## 3. Três armadilhas do seu ambiente (10 min)

Três coisas que já quebraram na sua máquina ou nas suas ferramentas. Formato: **gatilho → regra → data → onde está o detalhe**.

Exemplo: "Exportar do CRM pelo botão X perde a coluna de telefone (03/09/2026) — usar a API; detalhe em `memoria/crm-export.md`."

## 4. Um gate de efeito externo (5 min)

Complete: "Antes de ___, o agente SEMPRE pede 1 OK meu no chat. Vale mesmo quando ___."

Lista de candidatos: publicar em produção, mandar mensagem pra mais de N pessoas, apagar registro, mexer em cobrança, escrever pra cliente, criar conta em serviço pago.

## 5. Teste (10 min)

1. Salve como `~/.claude/CLAUDE.md`.
2. Abra uma sessão nova do Claude Code.
3. Peça algo que uma das suas regras deveria barrar ou moldar. Não avise que é teste.
4. Obedeceu? Marque a regra como boa. Não obedeceu? Reescreva mais específica e teste de novo.

## Depois da aula

- Cada vez que o agente errar: a correção vira **uma linha** no arquivo, na hora, com a data. Nunca repita a correção na mão duas vezes.
- Anote o tamanho do arquivo hoje. Em 30 dias, meça de novo. Se cresceu mais de 30%, é hora da dieta: o que virou trava automática vira ponteiro; o que é detalhe vai pra memória; o que é conhecimento vai pra memória externa.
- Escreva um teto no cabeçalho. Sem número, a dieta reverte.
