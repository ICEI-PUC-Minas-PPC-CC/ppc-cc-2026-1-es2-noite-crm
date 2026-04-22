# Sprint 1 - Análise dos Requisitos e Identificação das Classes

<span style="color:red">Pré-requisitos: <a href="1-Documentação de Contexto.md"> Documentação de Contexto</a></span>

## Histórias de Usuários

<li><a href="/docs/EngSoftware-I/Salvou%20-%20Historias%20Detalhadas.pdf"> Histórias Detalhadas</a></li>

## Modelagem de Classes

Lista das classes identificadas e responsabilidades de cada classe:

<li><a href="/docs/EngSoftware-I/Salvou%20-%20Modelo%20de%20Classes.pdf"> Modelo de Classes</a></li>

## Como as histórias dos usuários se conectam com as classes?

As histórias de usuário presentes no backlog estão diretamente relacionadas ao modelo de classes, pois representam os requisitos funcionais do sistema, enquanto as classes definem como esses requisitos serão implementados na prática. Cada história descreve uma necessidade do usuário, e essa necessidade é traduzida em responsabilidades atribuídas a uma ou mais classes no diagrama.

Por exemplo, as histórias H1.1 e H1.2, que tratam do cadastro, edição, visualização de histórico, registro de observações e inativação de clientes, estão diretamente associadas à classe Cliente e às classes auxiliares HistoricoCliente e Observacao. A classe Cliente é responsável por armazenar e gerenciar os dados cadastrais, enquanto HistoricoCliente organiza as interações ao longo do tempo e Observacao permite registrar anotações específicas. Dessa forma, uma única história pode envolver a colaboração entre várias classes para atender completamente à funcionalidade desejada.

Da mesma forma, as histórias H2.1 e H2.2, relacionadas ao gerenciamento de compromissos e lembretes, estão conectadas principalmente à classe Compromisso. Essa classe concentra responsabilidades como registrar, reagendar e concluir tarefas, além de controlar seus status. A funcionalidade de lembretes, inicialmente modelada como uma classe separada, foi posteriormente incorporada como método, demonstrando uma decisão de refinamento no design sem perder o vínculo com a necessidade descrita na história.

As histórias H3.1 e H3.2, que envolvem filtragem de clientes e geração de relatórios, estão associadas às classes FiltroClientes e Relatorio. Essas classes são responsáveis por processar dados, aplicar critérios de segmentação e gerar informações úteis para tomada de decisão. Assim como no caso dos lembretes, a funcionalidade de filtragem também pode ser incorporada como método, evidenciando ajustes na modelagem.

Por fim, as histórias H4.1 e H4.2, relacionadas à autenticação e segurança do usuário, conectam-se às classes Usuario e Autenticador. A classe Usuario armazena as informações e mantém a sessão, enquanto Autenticador executa a validação de credenciais e gerencia processos como recuperação de senha, separando claramente os dados das regras de segurança.

Portanto, observa-se que as histórias de usuário orientam a definição das responsabilidades das classes, e o modelo de classes garante que todas as funcionalidades descritas sejam contempladas por meio da colaboração entre os elementos do sistema.
