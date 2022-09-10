# Estrutura de inicialização do angular

No angular o arquivo *main.ts* chama o módulo da aplicação (AppModule). Dentro de uma aplicação angular é organizada uma árvore de componentes, de forma modularizada.

AppModule será chamado para inicializar a aplicação. Dentro de AppModule, temos um atributo chamado bootstrap, cuja função é referenciar o AppComponent e a partir deste componente, toda a árvore de componente será chamado.

