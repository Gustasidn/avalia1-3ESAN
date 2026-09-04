# avalia1-3ESAN -n
## Orientações de entrega

1.	Trabalhe em um repositório criado especificamente para cada exercício. 
2.	Antes de cada operação que altere o histórico ou publique conteúdo, registre o estado observado com comandos de inspeção adequados.
3.	Nunca inclua senha, Personal Access Token, arquivo .env real ou outro segredo nas evidências. Credenciais expostas devem ser revogadas, não apenas apagadas do último commit.
4.	Entregue os artefatos pedidos em cada exercício. Capturas de tela devem mostrar o contexto suficiente para identificar repositório, ramificação e resultado.
5.	Justifique decisões de histórico, revisão, aceitação ou não de pull requests.
6.	Vale, até 0,5 pontos na nota da primeira avaliação. 

# A main avançou enquanto o pull request estava aberto

Desafio: resolver uma divergência real entre contribuições válidas, manter a proposta original atualizada e demonstrar que a política da main transforma a revisão em um mecanismo executável.
Cenário
O repositório oficial frankalcantara/avalia1-3ESAN contém uma tabela vazia em um arquivo markdown. Aluno 1 e Aluno 2 (dois alunos de exemplo) fizeram um fork deste repositório e criaram branches a partir do mesmo commit. Ambos inserem sua linha imediatamente após o separador da tabela, garantindo que as propostas disputem a mesma região. O objetivo é criar um conflito.

## Participantes

| Nome | RA |
|:---|:---|

Aluno 2 e Aluno 1 terão direito de criar branches nos seus repositórios locais, mas não terão direito de fazer push no branch main, toda colaboração será aceita por meio de pull request. A ideia é que dois alunos façam pull-requests nos repositórios trocados.

## Tarefas

O administrador configura uma política para main que exija pull request, uma aprovação e resolução das conversas, além de impedir exclusão e force push. Não habilite uma verificação de estado inexistente.
1.	Aluno 1 e Aluno 2 sincronizam suas bases, criam ramificações distintas e abrem propostas separadas. Cada proposta deve adicionar apenas uma linha a participantes.md e conter a RA.
2.	O administrador aprova e integra primeiro o pull request de Aluno 2. Sem fechar o pull request de Aluno 1, a equipe demonstra que upstream/main só se torna conhecida no repositório local depois de uma atualização explícita das referências.
3.	Aluno 1 incorpora a nova upstream/main ao próprio branch por uma mesclagem explícita. Ao resolver o conflito, deve preservar as duas participantes, remover todos os marcadores e verificar problemas de espaços antes do commit de resolução.
4.	Aluno 1 publica o commit de resolução no mesmo branch. A equipe confirma que o pull request existente foi recalculado, identifica se a aprovação anterior continua válida conforme a política configurada e executa a revisão necessária.
5.	Antes da segunda integração, a equipe compara merge commit, squash and merge e rebase and merge. Escolha uma estratégia para o exercício e preveja, por desenho do grafo, quais commits permanecerão alcançáveis pela main.
6.	Um participante tenta deliberadamente publicar um commit direto em main. A tentativa deve ser recusada pela plataforma. Preserve a mensagem de erro como evidência e recupere a mudança em um branch apropriado, sem force push e sem perder o trabalho.

## Perguntas de auditoria
•	Qual referência aponta para cada ponta antes e depois do fetch?
•	Quais são as três versões usadas pelo Git para detectar o conflito?
•	Por que escolher apenas um dos lados apagaria uma contribuição válida?
•	O que mudou no diff do pull request depois da resolução?
•	Qual regra social do README também foi transformada em bloqueio técnico?
Evidências obrigatórias
•	Captura do ruleset ou proteção da main e mensagem de rejeição do push direto.
•	Grafos do histórico antes da primeira integração, durante o conflito e após a integração final.
•	Trecho do conflito original e conteúdo resolvido, com justificativa para a preservação das duas linhas.
•	Comparação das três estratégias de integração e desenho previsto para a estratégia escolhida. 
•	Todas as entregas devem ser feitas em arquivos de texto no formato markdown, com o padrão usado no Github.
