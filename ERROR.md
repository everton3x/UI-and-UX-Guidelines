# Diretrizes para exibição de erros para o usuário

Esta diretirzes detalham como comunicar erros (ou avisos, ou alertas) para o usuário.

Nas referências a *erro*, entenda-se quaisquer mensagens que tratem de acontecimentos inesperados ou problemas e dificuldades encontradas pela aplicação ao processar comandos do usuário.

Assim, quando um arquivo não for encontrado, quando faltarem permissões, não for possivel gravar alterações ou dados incorretos forem fornecidos ou omitidos quando requeridos, isso são erros. Por outro lado, quando as alterações forem salvas, quando arquivos forem carregados ou quando os dados de um formulário estiverem corretos, mensagens informativas dessas situações não são erros.

Em resumo: quando algo não ocorrer como o esperado, temos um erro; quando tudo ocorrer conforme se espera, não temos erro.

---

## Erros na execução de tarefas

A exibição de erros não deve ser bloqueante, ou seja, o componente que exibe o erro não pode bloquear a tela do usuário, como um pop-up faz, por exemplo.

*Toasts* não são adequados porque podem não ser facilmente percebidos pelo usuário. O ideal é usar *Alerts*, movendo o foco da página para a mensagem.

Essa abordagem é ideal para erros gerais da tarefa do usuário, tais como falha na gravação de dados ou na carga de dados para a tela, na geração de uma consulta ou relatório etc.

## Erros no preenchimento de formulários

Para erros em preenchimento de campos de dados em formulários ou campos de filtragem e configuração de consultas e relatórios, o ideal é exibir a mensagem de erros próximo do campo ao qual ela se refere. Uma boa solução é destacar o campo com uma cor indicativa de erro, ou adicionar um *Ícone* discreto e apresentar num *Tooltip* uma breve mensagem explicando o que está errado.

## Quando exibir os erros?

Quando se trata de erro na execução de tarefa (gravar um arquivo, salvar os dados, gerar um relatório etc), o erro deve ser exibido para o usuário no momento em que o sistema tenta concluir a tarefa.

Quando se trata de erros em formulários relacionados ao preenchimento incorreto de campos ou a omissão de campos requeridos, duas abordagens podem ser adotadas:

A primeira é exibir o erro logo que o campo perder o foco, porém sem alterar o fluxo de trabalhao do usuário (apenas mostra o indicador e mensagem de erro, sem forçar o usuário permanecer com o foco no campo, por exemplo).

A outra abordagem é a de exibir os erros penas na conclusão da tarefa, por exemplo, num formulário de inserção de dados, apenas quando o formulário tenta gravar os dados inseridos. Nesse caso, antes de gravar os dados, a rotina de validação é executada e os campos com erros de validação são sinalizados. O desejado é que o primeiro campo com erro receba o foco e, se possível, que a sequência de tabulação (passagem de um campo para outro) seja composta apenas com os campos com erros, evitando que o usuário precise passar por toda a sequência normal dos campos.

## O que mostrar na mensagem de erro?

As mensagens de erro devem conter informações adequadas ao usuário, evitando informações sobre a implementação, tais como códigos SQL ou informações de back trace. Essas informações e demais detalhes do erro devem ser gravadas em arquivos de log ou equivalente para estarem disponíveis apenas para os desenvolvedores.

Ao usuário normalmente interessa saber que um erro ocorreu, qual o motivo do erro (arquivo não encontrado, falta de permissões, dados incorretos etc) e como corrigir o erro ou como entrar em contato com o suporte da aplicação. Adicionalmente pode ser fornecido um código ou identificador do erro para que os desenvolvedores possam identificar o erro no log.

Caso exista uma solução dentro da própria aplicação para abertura de chamado ou requisição de suporte, um link direto pode ser fornecido já na mensagem de erro, o qual direcionará o usuário para a ferramenta de suporte, preferencialmente já pré-preenchendo a abertura do ticket ou chamado com os dados principais (usuário, data/hora, onde ocorreu o erro, código do erro no log etc).