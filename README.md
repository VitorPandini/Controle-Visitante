# Home

O repositório `controle-visitantes` é destinado a armazenar o código referente ao projeto desenvolvido 



## Conhecendo o processo

O projeto [controle-visitantes](https://github.com/djangoframeworknapratica/controle-visitantes) tem o objetivo informatizar o processo de registro e administração de visitantes do condomínio Montanhas Azuis.

Hoje o condomínio conta com um processo manual e por meio de cadernos que são utilizados para registrar as informações referentes aos visitantes e informatizar esse processo é importante para ganhar tempo no processo, melhorar a experiência de trabalho dos porteiros e ainda armazenar as informações de forma segura e confiável.

O projeto consiste em uma ou mais páginas web em que seja possível registrar visitantes e visualizar suas informações. Além disso, precisamos disponibilizar algumas funcionalidades que seguem os fluxos executados pelo porteiro assim que um visitante chega à portaria e quando o mesmo deixa as dependências do condomínio.



## Principais funcionalidades

### Registro de visitantes

O formulário de registro de visitantes deve abstrair a etapa 01 do processo, onde o visitante informa **nome completo**, **CPF**, **data de nascimento**, o **número da casa** que deseja visitar e ainda a **placa do veículo**, se estiver utilizando durante a visita. Além desta informações, o formulário salva o **horário de chegada** do visitante automaticamente.

![Tela de registro de visitante com formul&#xE1;rio para inser&#xE7;&#xE3;o das informa&#xE7;&#xF5;es](docs/images/screenshot-from-2020-05-11-14-09-52.png)

### Listagem de visitantes

A listagem de visitantes exibe, por meio de uma tabela, os visitantes recentes classificados por horário de chegada, do mais recente para o mais antigo.

![Tela com lista de visitantes recentes](docs/images/screenshot-from-2020-05-11-16-26-59.png)

### Widgets para resumo de informações

O widgets da página inicial da dashboard têm a função de exibir um resumo dos números referentes aos visitantes em cada status e ainda o número total de visitantes registrados no mês.

![Captura de tela de widgets para resumo de informa&#xE7;&#xF5;es de visitantes](docs/images/screenshot_2020-04-08_12-21-52%20%281%29.png)

### Visualização de informações de visitante

A partir da tabela que lista os visitantes recentes, é possível acessar a página que exibe as informações detalhadas de cada visitante. No exemplo abaixo um visitante com a visita já finalizada:

![Tela de informa&#xE7;&#xF5;es de visitante](docs/images/screenshot-from-2020-05-11-16-41-43.png)

### Autorização de entrada

A tela de informações de vistante é importante pois a partir dela é possível utilizar as funcionalidades de autorização de entrada e finalização de visita.

Quando um visitante está aguardando autorização, o botão para autorizar a entrada fica disponível na tela de informações deste visitante e, para autorizar a entrada, basta clicar no botão para abrir o formulário que deve ser preenchido com o nome do morador que autorizou a entrada do visitante e confirmar a ação.

No exemplo a seguir o visitante está aguardando autorização:

![Tela de informa&#xE7;&#xF5;es de visitante com bot&#xE3;o para autorizar a entrada](docs/images/screenshot-from-2020-05-11-16-42-04.png)

Assim como quando o porteiro anotava o nome do morador responsável por autorizar a entrada e o horário de contato com esse morador, a funcionalidade recebe o nome do morador através de um formulário e salva o horário de contato e autorização de forma automática ao concluir a ação.

![Tela de informa&#xE7;&#xF5;es de visitante ao fundo com alerta exibindo formul&#xE1;rio de cadastro de morador respons&#xE1;vel](docs/images/screenshot-from-2020-05-11-16-42-33.png)

### Finalização de visita

Assim como conseguimos utilizar a funcionalidade para autorizar a entrada do visitante, podemos finalizar sua visita. A funcionalidade funciona de forma parecida, com a diferença que é necessário apenas confirmar a ação, sem necessidade de informações adicionais.

Ao clicar no botão para finalizar uma visita, um alerta é exibido solicitando que o porteiro confirme a ação.

![Tela de informa&#xE7;&#xF5;es de visitante com bot&#xE3;o para finalizar visita](docs/images/screenshot-from-2020-05-11-16-42-56.png)

Ao confirmar a ação clicando no botão "finalizar visita", o porteiro encerra o processo referente a este visitante e o horário em que a ação ocorreu é registrada.

![Tela de informa&#xE7;&#xF5;es de visitante ao fundo com alerta exibindo a confirma&#xE7;&#xE3;o de que o usu&#xE1;rio realmente deseja encerrar a visita](docs/images/screenshot-from-2020-05-11-16-43-16.png)

Os botões "autorizar entrada" e "finalizar visita" são exibidos somente quando é possível executar a ação para o visitante em questão. Caso contrário, como quando o visitante já deixou as dependências do condomínio, nenhum botão é exibido.

## Tecnologias utilizadas

O projeto [controle-visitantes](https://github.com/djangoframeworknapratica/controle-visitantes) utiliza as seguintes tecnologias e recursos de código aberto:

* [Django framework](https://www.djangoproject.com/)
* [Django widget tweaks](https://github.com/jazzband/django-widget-tweaks)
* [Start Bootstrap - SB Admin 2](https://github.com/BlackrockDigital/startbootstrap-sb-admin-2)


