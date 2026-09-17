> **Publicado pela Expert Integrado — versão 2026-09-17-a727664.** Cópia pública de `claude-md-do-eric`, gerada automaticamente a partir da fonte interna (sem histórico) pelo robô publicador. Issues e pull requests aqui não são acompanhados; contato em expertintegrado.com.br.

# CLAUDE.md: as regras da sua empresa dentro do agente

Material da aula da **Mentoria Automações Inteligentes** de 15/09/2026, por **Eric Luciano**. O texto abaixo segue a aula como ela foi dada, na mesma ordem das quatro partes que estão no Portal do Aluno.

Este repositório é o que eu mostrei na tela: uma referência de como o meu CLAUDE.md está construído, sem os meus segredos, pra vocês usarem como norte. Não é pra copiar. No fim tem o jeito certo de usar.

| O que tem aqui | Pra que serve |
|---|---|
| `README.md` (este arquivo) | A aula em texto, nas 4 partes |
| `exemplo-eric/CLAUDE-do-eric-comentado.md` | O meu CLAUDE.md global, higienizado, com o porquê de cada seção |
| `template/CLAUDE.md` | Um esqueleto com as seções que eu uso, pra sua IA se basear (não pra você preencher na mão) |
| `template/bloco-memoria-externa.md` | Bloco extra pra quem usa o Expert Brain ou outra memória externa |
| `prompt-para-o-seu-claude.md` | O prompt pra colar no seu Claude e começar a conversa de meia hora |
| `exercicio-em-aula.md` | O exercício: meia hora com o seu Claude ajustando o seu arquivo |

---

## Parte 1. A regra da empresa e a regra da sala

Toda ferramenta de agente tem um arquivo grande de regras em Markdown. No Claude Code é o **CLAUDE.md**. No Codex do GPT é o **AGENTS.md**. No OpenClaw é o **SOUL.md**. Muda o nome, a ideia é a mesma: é o arquivo com as regras de uso da sua empresa.

Pense assim: você entra na porta da empresa e tem uma placa lá em cima. "Aqui a gente valoriza o trabalho em conjunto." "Aqui a gente valoriza o crescimento contínuo." É quase missão, visão e valores. Essa é a **regra da empresa**. Aí você entra numa sala e tem outra placa: "proibido entrar com comida", "proibido notebook". Essa é a **regra da sala**.

O agente funciona igual:

- **CLAUDE.md global** = a regra da empresa. Como eu trabalho, no meu Claude Code como um todo.
- **CLAUDE.md do projeto** = a regra da sala. Fica dentro da pasta do projeto (ou do repositório) e vale só ali.

Se você usa ChatGPT ou Claude no navegador, você já conhece isso: é o botão "Instruções" nas configurações. Quando você leva pro computador, essa instrução vira o arquivo.

**O que vai lá dentro:** tudo o que você quer que a IA sempre lembre quando começar a falar com você. Meu nome. Minha profissão. Como eu gosto que ela me chame. Se eu gosto de texto longo ou curto. Se eu quero termo técnico ou não. Quais as ferramentas principais que eu uso. Qual é o meu CRM. Quem são as pessoas da equipe.

Não confunda com o segundo cérebro. O Expert Brain guarda as informações do dia a dia do negócio, tem de tudo lá dentro. O CLAUDE.md é o **top 10, top 20**: aquilo que o agente não pode esquecer por nada.

**Como funciona por baixo:** cada vez que ele abre uma conversa nova, a primeira coisa que faz é ler o CLAUDE.md inteiro. Você fala "oi", ele pensa uns segundinhos antes de responder. É isso que ele está fazendo. Primeiro lê a regra da empresa: "entendi, o Eric trabalha com IA, tem tantos anos, mora em tal lugar, gosta que eu fale desse jeito, usa esse CRM, a equipe é essa". Depois, se você está dentro de um projeto, lê a regra da sala: "esse projeto é o Expert Brain, está no GitHub, roda no Cloudflare, o objetivo é tal". Ou: "esse projeto é a campanha de Black Friday de 2026, acontece em tal dia, meta de tantos reais, regra principal: só clientes que já existem, nada de cliente novo". Quando você falou "oi", ele já entendeu tudo isso. Ele fica mais inteligente.

Não é sobre memória. É sobre a **regra que eu criei pra minha memória**.

---

## Parte 2. Ele se preenche sozinho e engorda

Se você instalar o Claude Code e não fizer absolutamente nada, só sair trabalhando, o CLAUDE.md **se preenche sozinho**. Só que ele se preenche com o que a própria ferramenta decidir. Sem regra de como você quer.

É a receita de bolo da avó. Ela colocou uma colherinha de vinagre no meio, ficou bom, virou a receita. O seu CLAUDE.md vai ter o **seu tempero**. Por isso é difícil eu te entregar o meu: ele vai te chamar com as palavras que eu uso, vai escrever termo técnico que você não queria, ou vai escrever texto grande quando você queria curto.

**Como eu alimento o meu (e o que eu recomendo):**

- Eu não abro o arquivo e fico digitando. Eu não gosto de digitar nada. Eu mando o próprio agente se retroalimentar. Você pede "encurta esse texto", ele encurta. Na próxima conversa escreve grande de novo. Se você quer que ele sempre faça de um jeito, tem que falar:

  > Salva no teu CLAUDE.md que eu sempre quero textos curtos.

  > Salva no teu CLAUDE.md que XYZ.

- O caminho é ir refinando o documento até ele ficar exatamente do jeito que você quer, pra alinhar o comportamento do agente com o que você espera.
- Eu deixo **uma aba sempre aberta** no Claude Code só pra isso. Toda vez que decido mudar uma regra ou fazer algo diferente, vou lá e mando ele mesmo ajustar o arquivo. Não arrumo uma vez e largo lá: são as regras da minha empresa, têm que estar atualizadas.
- Onde fica: dentro da pasta `.claude` do seu usuário, num lugarzinho meio escondido. Não precisa procurar. Pede pro seu Claude: "abre o meu CLAUDE.md".

**Por que ele não pode engordar.** Lembra que ele lê o arquivo inteiro? Não é só na abertura. **Toda vez que você envia uma mensagem, ele relê o CLAUDE.md inteiro e a conversa inteira.** Por isso a conversa longa fica mais cara. Encher o arquivo de regra tem dois custos:

1. Você gasta mais token em cada mensagem.
2. Quanto mais informação você enfia, mais chance ele tem de esquecer ou se perder em alguma.

Existe um limite recomendável de tamanho. Estamos falando de uns **30 KB**, um arquivinho minúsculo, mas o limite existe. O meu está no limite do recomendável, e eu faço reciclagem dele sempre.

Caso real: em 1º de agosto o meu tinha 24 KB. Em cinco semanas, uma regrinha de cada vez, subiu pra 41 KB. Ficou gordo demais. Em 11 de setembro eu fiz uma dieta: de 41 pra **32 KB**. E deixei um **teto numérico**: toda vez que passar de 32 KB ele me avisa, e ele mesmo avalia o que não faz mais sentido e o que dá pra compactar.

---

## Parte 3. As doze regras que nunca falham

Agora o meu arquivo aberto na tela. Ele é o global, tem uma cacetada de regras. A estrutura:

**No topo, as regras inegociáveis.** São doze. Se tudo der errado, essas doze ele nunca falha. Alguns exemplos com o porquê:

- **Nunca inventar nem inverter fato.** Nome, valor, data, desfecho (ganho ou perdido), versão, se um repositório ou domínio existe. Eu estou reforçando: não inventa nada. Não zera a chance da IA falar besteira, mas diminui muito.
- **Não declarar sucesso sem verificar o resultado.** A IA fala "fiz, está feito, testei" e não verificou. Regra: antes de dizer que resolveu, você tem que ter uma prova. Abre o navegador e vê se o software está feito de verdade. Se o site foi pro ar de verdade. Se a mensagem foi enviada de verdade. Se ela não tem prova, ela reporta: "não consegui provar".
- **Circuit breaker.** Se a mesma ferramenta deu o mesmo erro duas vezes, para. Não tenta a terceira igual. Tenta de outro jeito ou faz outro diagnóstico comigo. (A terceira tentativa idêntica já é barrada por uma trava automática; falo disso na Parte 4.)
- **OK meu antes de qualquer coisa externa e irreversível.** A minha IA é muito autônoma, mas coisa externa e irreversível ela sempre me pede. Publicar site, mandar mensagem em massa, apagar dado. Tem coisa que ela poderia fazer sozinha e ainda assim me pede. Isso ajuda muito.
- **Sem gambiarra.** Caminho oficial, ou para e pede OK. Senão ela emenda um cabo no outro, faz um puxadinho e "resolve", e eu fico construindo um monte de coisa quebrada. Ou tenta o caminho real, ou fala "Eric, não consegui, consigo fazer uma gambiarra aqui, posso?".
- **Sem emoji.** A IA mete emoji do nada. Mas aqui tem uma sacada: eu criei um **vocabulário fixo de sinalização**, um farol. Quando ele termina algo, bolinha verde. Quando está processando ou esperando algo, amarela. Quando precisa que eu decida alguma coisa, vermelha. Aí ele me manda um texto grande e, só pela bolinha, eu já sei se preciso interagir ou não.
- **Senha nunca aqui dentro.** Proibido. Eu não dito senha pra ele e ele não digita senha pra mim. As senhas ficam no cofre (1Password), e a regra só diz onde ele busca.

**Depois vêm os blocos:**

- **Quem é o Eric.** Onde eu moro, como eu trabalho, o que eu gosto.
- **Ambiente.** Que máquina é. Eu tenho o CLAUDE.md do computador e o do notebook, cada um sabe em que máquina está.
- **Comportamento do agente.** Como ele trabalha comigo.
- **Brain, meu segundo cérebro.** O que fica lá dentro. Pra consultar, usa `recall`. Pra salvar, usa `save_note`. Várias regras pro robô não errar.
- **Tarefas.** Eu sempre coloco as tarefas no Brain. Quando copia pro ClickUp. Quando completa. No início de toda sessão ele lê as atividades do Brain.
- **WhatsApp.** Como ele usa.

**Ponteiros: o arquivo cita outros arquivos.** Como eu tenho limite de tamanho, em vários momentos eu não escrevo a regra inteira, eu cito onde ela está:

- "Onde você procura senhas e chaves" aponta pro cofre.
- "Como é o processo de venda" aponta pra outro arquivo. Se ele quiser ler mais sobre vendas, vai lá.
- "No dia a dia use o estilo Eric Executivo" aponta pro documento do estilo.
- **Aviso de voz.** Tem uma regra: só me chama quando eu preciso agir, nunca pra status. Senão ele vem "Eric, terminei a fase 1, vou pra fase 2". Cara, você precisa de mim? Não? Então não me chama. E o gatilho é exato: se eu falo "me avisa por voz", ele dispara um áudio no meu computador ("Eric, estou te esperando pra resolver tal coisa"). Se eu falo só "me avisa", não dispara. A regra do aviso de voz tem umas cinquenta linhas, então no CLAUDE.md fica uma linha: "quando o Eric pedir aviso de voz, leia esse arquivo". Se eu pedir, ele me liga no telefone.

**Uma regra que cria outro CLAUDE.md.** Eu já falei pra ele: toda vez que eu inicio um projeto de desenvolvimento, uma das coisas que precisa acontecer é criar o CLAUDE.md daquele projeto. Então eu crio a pasta, ele mesmo olha a pasta, me faz as perguntas que precisa e cria a regra da sala. Eu tenho o global e vários de projeto, e quem cria os de projeto é ele.

---

## Parte 4. Copiar o meu não resolve

Existe jeito certo e errado? Não. Existem **recomendações**. O Dario, dono da Anthropic, divulgou o CLAUDE.md dele. O Boris, que faz o Claude Code, divulgou o dele. Ajuda, mas eles usam pra desenvolver software, então está cheio de regra de desenvolvedor. Se você é empresário, você precisa de regras do **seu** uso.

As recomendações que valem pra todo mundo:

**Não muito longo.** É orçamento de contexto, não lista aditiva. Cada linha é reenviada ao modelo em toda mensagem.

**Informação vitalícia, não pontual.** O que **entra**:

- Regra de comportamento. Tudo que deu errado, toda cagada num jeito de usar, sobe pra lá em uma linha.
- Efeito externo: o que ele nunca faz sem o meu OK. Publicar, mensagem em massa, tudo que é crítico.
- Convenções onde a IA viaja: meu fuso horário, qual canal usar ("manda WhatsApp" é uma coisa, "manda no chat da equipe" é outra).
- Ponteiro de uma linha pro detalhe: "regra X, detalhe nesse arquivo".

O que **não entra**:

- Como instalar ferramenta, caminho, onde está o token. Isso fica na memória do computador.
- Estado do projeto. "O agente de WhatsApp está 70% pronto" muda toda semana e eu não preciso lembrar. Vai pro histórico do projeto.
- Decisões e o porquê delas. Vai pra memória externa (Brain).
- Segredo, senha. Nunca.
- Estatística. "O Eric usa o CRM 70% das vezes" não faz diferença nenhuma.
- Regra que uma trava automática já cumpre. O WhatsApp Agent já tem a própria trava de não disparar sem confirmar; não precisa repetir no CLAUDE.md.

**Como a regra é escrita (do jeito que a minha IA avaliou o meu arquivo):**

- Verificável e específica: o que fazer, o que nunca fazer, com data.
- Gatilho, ação, exceção: "quando X, faz Y, exceto Z".
- NUNCA e SEMPRE em maiúscula só onde é inegociável. Use pouco. Se tudo for maiúsculo, para de funcionar.
- Origem entre parênteses: de onde veio a decisão, com data. Ele vai no segundo cérebro, entende o que aconteceu naquele dia e a regra vira uma linha mais um ponteiro.

Entendam: eu não decidi esse formato. Eu fui mexendo, mexendo, mexendo, e a própria IA foi escrevendo assim. Ficou muito bom. Pra mim funciona. Não posso garantir que "escreve NUNCA em maiúsculo" vai funcionar pra você. **Teste.**

**Texto versus trava automática.** Regra 100% em texto falha em sessão longa: quando a conversa fica grande, o contexto compacta e a IA esquece. Tudo que é crítico e verificável vira **hook**, uma trava automática que não depende do CLAUDE.md estar bem nutrido. Quando eu abro a sessão, quando compacta, quando mando mensagem, quando chega um e-mail, quando abro um arquivo: qualquer coisa objetiva que acontece no computador pode virar um gatilho. Tudo que é trava eu quero por hook, não por texto. Vai ter uma aula só de hooks.

**Ciclo de vida.**

- Correção minha vira linha na hora: "fiz assim e o Eric mandou mudar, deixa eu memorizar pra não esquecer mais".
- Revisão periódica, a dieta. Com trava anti-reengorda: passou de 32 KB, ele me avisa.
- Entrou uma regra, sai uma equivalente. Regra nova = ele busca se já tem parecida pra compactar.
- Antipadrões que eu mesmo cometi: arquivo gigante que ninguém relê; a mesma regra em dois lugares (eu tinha 3 KB duplicados); a história inteira do incidente no lugar da regra.

**Sobre a seção "Quem é o Eric" no exemplo:** é a que mais muda o comportamento no dia a dia e quase nada dela é técnico. Um exemplo: eu dito 90% dos pedidos por áudio. O agente já executou literalmente uma palavra que era erro de transcrição. Então avisei: "eu não digito, eu dito; se vier uma palavra fora de contexto, desconfia, me pergunta 'você quis dizer isso?' antes de executar". Outro: uma aba aberta pro projeto A recebeu um pedido do projeto B. Virou a regra de sessões temáticas. É assim que o arquivo cresce.

Aqui dentro eu estou passando o meu segredo sem passar o meu segredo. O exemplo comentado traz o que é público e tirou o que não é.

---

## Como aplicar (o jeito que eu ensinei)

Não copie o meu. Pode copiar, mas não vai servir pra nada: é a minha empresa, a minha regra, a minha forma de trabalhar. Serve de norte.

O caminho é: **pega a URL deste repositório, joga dentro do seu Claude e gasta meia hora trocando ideia com ele.** O prompt pra começar (também está em `prompt-para-o-seu-claude.md`):

```
Quero mexer no meu CLAUDE.md pra ele ficar bom.
Use como referência o repositório https://github.com/Expert-Integrado-Alunos/claude-md-do-eric (leia o README, o exemplo comentado e o template).
Mas as regras têm que ser as MINHAS: meu trabalho não é o do Eric.
Me faça as perguntas que precisar, uma de cada vez: quem eu sou, como eu gosto que você me responda, quais ferramentas eu uso, o que você nunca pode fazer sem me perguntar, o que já deu errado entre nós.
Depois escreva o meu CLAUDE.md global, curto, com as regras inegociáveis no topo, e me mostre antes de salvar.
```

Depois disso, a manutenção é uma frase por vez, sempre que ele errar:

```
Salva no teu CLAUDE.md que eu sempre quero textos curtos.
```

O exercício completo está em `exercicio-em-aula.md`.

## Relação com outras aulas

- **Hooks no Claude Code**: as travas automáticas da Parte 4.
- **A stack de memória do seu agente**: CLAUDE.md, memória local e Brain, o que mora em cada um.
- **Sincronização entre computadores**: o mesmo CLAUDE.md valendo no PC, no notebook e no servidor.
- **Playbook Claude**: [playbookclaude.expertintegrado.com.br](https://playbookclaude.expertintegrado.com.br), o uso do Claude no dia a dia.

## Licença

MIT. Use, adapte e ensine. Autoria: Eric Luciano, Mentoria Automações Inteligentes (Expert Integrado).
