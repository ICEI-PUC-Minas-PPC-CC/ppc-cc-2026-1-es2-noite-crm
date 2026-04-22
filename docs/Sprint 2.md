# Sprint 2 - Modelagem de Classes e Relacionamentos

<span style="color:red">Pré-requisitos: <a href="Sprint 1.md"> Sprint 1 - Análise de Requisistos e Identificação das Classes</a></span>

## Diagramas de Classes

Diagrama de classes está na última página do documento: 

<li><a href="/docs/EngSoftware-I/Salvou%20-%20Modelo%20De%20Classes.pdf"> Diagrama de Classes</a></li>

## Explicação dos Relacionamentos e Justificativa das Decisões

A classe Cliente ocupa um papel central no modelo, estabelecendo relacionamento com diversas outras classes, como HistoricoCliente, Observacao, Compromisso e Relatorio. Essa decisão de modelagem é justificada pelo fato de que o cliente é o núcleo do sistema de CRM, já que praticamente todas as funcionalidades giram em torno do gerenciamento do relacionamento com ele. Assim, outras classes dependem do Cliente para existir ou para fazer sentido dentro do domínio.

A relação entre Cliente e HistoricoCliente pode ser entendida como uma associação forte, próxima de uma agregação, pois o histórico existe em função do cliente e armazena todas as interações realizadas com ele. Essa separação em uma classe própria foi uma decisão importante de modelagem para garantir melhor organização dos dados e facilitar consultas, como ordenação por data e análise da evolução do relacionamento.
Da mesma forma, a classe Observacao também se relaciona com Cliente e HistoricoCliente, representando anotações específicas vinculadas ao cliente. A separação dessa responsabilidade em uma classe independente evita sobrecarga na classe Cliente e segue o princípio de responsabilidade única, tornando o sistema mais modular e fácil de manter.

A classe Compromisso possui associação com Cliente e HistoricoCliente, pois cada compromisso está vinculado a um cliente e, quando concluído, alimenta o histórico. Essa relação demonstra um fluxo de informação dentro do sistema, onde ações realizadas (compromissos) impactam diretamente o registro histórico. Além disso, a existência de status e possibilidade de reagendamento justificam a modelagem dessa entidade como uma classe própria, e não apenas como um atributo.

A classe Lembrete, inicialmente modelada separadamente e depois incorporada como método, indica uma decisão de simplificação do modelo. Isso ocorre porque sua responsabilidade (gerar notificações) está diretamente ligada ao comportamento de compromissos e clientes, não sendo necessário mantê-la como uma entidade independente. Essa mudança reduz a complexidade do diagrama sem perder funcionalidade.

O mesmo ocorre com FiltroClientes, que foi transformado em método. A justificativa é que filtragem não representa um objeto do domínio, mas sim uma operação sobre os dados de clientes. Portanto, sua incorporação como comportamento da classe Cliente ou de serviços relacionados torna o modelo mais coeso.

A classe Relatorio se relaciona com Cliente, Compromisso e FiltroClientes, pois depende de dados provenientes dessas entidades para gerar informações consolidadas. Essa é uma associação de dependência funcional, já que o relatório não mantém estado próprio relevante sem os dados das demais classes.

Por fim, as classes Usuario e Autenticador possuem uma relação de associação bem definida, onde o Autenticador é responsável pelas regras de validação e segurança, enquanto o Usuario armazena os dados. Essa separação foi uma decisão importante de modelagem para desacoplar regras de negócio (autenticação) dos dados, seguindo boas práticas de segurança e organização.
> - [Slack](https://slack.com/)
> - [Github](https://github.com/)
