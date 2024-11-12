# Diretrizes para utilização de cores

Estas diretrizes orientam como utilizar cores nos componentes para complementar a transmissão visual de informação ao usuário.

---

## Diretrizes gerais

Cores transmitem significado. Um botão verde transmite ao usuário um significado diferente de um botão vermelho. E esse significado não é aleatório, para certas cores, há um significado implícito sedimentado na percepção dos usuários de forma tal que, mesmo com outros indicativos, como um rótulo ou texto, o significado da cor no componente irá se sobressair. Por isso, é imprescindível que o desenvolvedor respeite esses significados intrínsecos e os use para potencializar a comunicação com o usuário através dos componentes do sistema.

Além de aproveitar o significado intrínseco das cores combinando-as nos componentes da interface, é necessário que se adote um padrão por toda a aplicação.

Por exemplo, o vermelho é normalmente associado a coisas perigosas ou ruins, então use-o em todas as mensagens de erro, botões ou outros controles de exclusões, em campos com erros de validação ou para sinalizar áreas do sistema com comandos potencialmente perigosos para a integridade das informações.

Por outro lado, o verde é geralmente utilizado como marcador de sucesso. Por isso ele normalmente aparece em mensagens que mostram a conclusão com êxito de tarefas.

Em resumo, adote um padrão de cores de acordo com a mensagem que cada elemento da interface do sistema deve transmitir e mantenha esse padrão por toda a aplicação, observando os significados intrínsecos das cores.

Um bom padrão de cores idicativas é:

- Azul: como cor primária e usada em botões de ação padrão ou preferencial;

- Verde: para indicar sucesso;

- Vermelho: para indicar erro ou fracasso;

- Amarelo ou laranja: para indicar um aviso de potenciais riscos ou alertas;

- Cinza: pra indicar ações alternativas, não padrão ou não preferencial.

# Paleta de cores

Embora possamos falar de cores referindo-se aos nomes comuns (verde, vermelho, laranja etc), é muito importante adotar uma paleta de cores que seja não só agradável para a visualização do usuário, mas que também tenha coerência estética. Simplismente escolher qualquer tonalidade para a paleta de cor sem considerar a iteração entre cada uma das cores provavelmente levará a resultados ruins.

Um bom caminho é adotar paletas de cores já testadas e conhecidas, por exemplo a paleta de cores que grandes empresas usam (Google, Microsoft, por exemplo). Outro caminho é buscar paletas de cores prontas em sites especializados. Outra alternativa é utilizar a paleta de cores de algum framework CSS.

Também é importante não utilizar cores com um significado intrínseco consolidado como cor básica para sua aplicação. Uma cor básica é aquela que irá compor todo o visual da sua aplicação. Por exemplo, use uma cor básica para bordas, outra para testo, outra para background. Isso quer dizer que não se deve utilizar vermelho como cor básica se você for utilizar vermelho como cor indicativa de erro ou de falha. Isso vale para qualquer tonalidade de vermelho.

Além disso, não transforme sua aplicação em um arco-íris de cores. Use poucas cores básicas, além das cores indicativas, também em quantidade restrita.

Fuja de cores intensas, ois estas agridem os olhos dos usuários. Uma mensagem de erro exibida num componente com fundo avermelhado é muito mais clara que uma exibida com um vermelho intenso e vai chamar a atenção do usuário da mesma forma.

Tenha atenção ao contraste. Exibir uma mensagem com texto branco num fundo amarelo geralmente é uma escolha ruim.