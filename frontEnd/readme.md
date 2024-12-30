/assets/
Objetivo: Armazenar arquivos estáticos, como imagens, fontes, vídeos, ícones, etc.
Exemplo: Imagens de produtos, ícones para botões, fontes personalizadas.
Detalhamento: Arquivos estáticos não relacionados ao código funcional da aplicação, mas necessários para a interface de usuário.

/components/ (View)
Objetivo: Armazenar componentes reutilizáveis, como botões, formulários, tabelas, etc.
Exemplo: Um botão que pode ser usado em várias páginas ou uma tabela de dados reutilizável.

Detalhamento: Cada componente deve ser autocontido com seus próprios arquivos de HTML, CSS e JavaScript, garantindo que possa ser facilmente importado e utilizado em diferentes partes da aplicação.

/tests/
Objetivo: Contém os testes unitários e de integração.
Exemplo: Testar se os componentes estão renderizando corretamente, se os ViewModels estão manipulando os dados como esperado e se os serviços estão realizando as requisições HTTP corretamente.
Detalhamento: Aqui você pode usar ferramentas como Jest, Mocha ou Jasmine para criar testes que garantem que a aplicação funciona corretamente.

/views/ (View)
Objetivo: Representar as páginas ou telas principais da aplicação, onde a visualização de dados ocorre.
Exemplo: Páginas de login, dashboard, página de produto.
Detalhamento: As views são as responsáveis por compor os componentes e mostrar as informações ao usuário. Elas devem ser simples e focadas apenas em mostrar o que é necessário, chamando os componentes e interagindo com o ViewModel.

 /viewmodels/ (ViewModel)
Objetivo: Gerenciar o estado da aplicação e a lógica de apresentação. Essa camada é responsável por interagir com os serviços e manipular os dados para exibição na view.
Exemplo: Gerenciar os dados de login, controle do estado do usuário, manipulação de listas de produtos, etc.
Detalhamento: Os ViewModels podem ser usados para conectar a View com os dados fornecidos pelos serviços, processando ou formatando as informações antes de enviá-las para a View.

/services/ (Model)
Objetivo: Lidar com a lógica de negócios e comunicação com APIs. A camada de serviço é responsável por fazer as requisições HTTP para o backend (como os microserviços), manipular a resposta e fornecer os dados ao ViewModel.
Exemplo: Serviço de autenticação, serviço de produtos, serviço de carrinho de compras.
Detalhamento: Cada serviço deve ser separado e deve expor funções que podem ser chamadas pelos ViewModels para obter ou modificar dados.

Como funciona o padrão MVVC (Model-View-ViewModel-Controller) nesse contexto?
Model (Serviços): Toda a lógica de interação com dados é feita nos serviços, que se comunicam com a API e fornecem as informações necessárias.
View (Componentes e Views): A interface com o usuário, composta por HTML e CSS, é responsável apenas pela exibição e coleta de entradas do usuário.
ViewModel: Manipula o estado da aplicação, recebendo dados do modelo (serviços) e preparando-os para a exibição na View.
Controller: Nesse padrão simplificado de MVVC, a função do Controller pode ser desempenhada pelas funções de interação nos ViewModels, controlando como os dados devem ser apresentados.