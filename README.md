# Plano de teste

## Introdução

Foi realizado um teste do código utilizando a IDE IntelliJ. Ao tentar rodar o projeto, foi identificado um erro de conexão com o banco de dados. O teste unitário focou principalmente no arquivo application.properties, onde estavam definidos os parâmetros necessários para essa conexão. Constatou-se que a URL configurada no arquivo não era compatível com a URL do banco de dados utilizado no projeto.

## Ambiente de teste

1. IntelliJ IDEA (utilizando o JDK versão 11)

2. Dbeaver

3. Postman

## Abordagem de teste

Ao temtar rodar código no inteliji, o erro de conexão com banco de dados foi evidenciado.



Foi realizado um teste de caixa branca para verificar o código que foi programado, identificar erros, realizar testes unitários e testar as funções. O teste foi focado nas funções no contexto das classes do código. Neste caso, foi feita uma verificação direta no application.properties, onde se encontram as configurações de conexão com o banco de dados, e foi identificada uma inconformidade.

Ao temtar rodar código no inteliji, o erro de conexão com banco de dados foi evidenciado.

Além disso, foi realizado um teste de caixa preta com a utilização do Postman, uma ferramenta que permite testar requisições HTTP de forma prática e visual, sendo muito utilizada para validar endpoints de APIs e simular o comportamento do usuário final sem acesso direto ao código-fonte.

Abrir o projeto na IDE IntelliJ.

Garantir que o JDK 11 esteja configurado corretamente.

Executar o projeto utilizando o modo Debug do IntelliJ.

Monitorar os logs para identificar falhas de conexão.

Utilizar o DBeaver para validar as credenciais e a URL de conexão com o banco.

Usar o Postman para testar os endpoints da aplicação (caso o projeto envolva APIs).

## Conclusão

O erro identificado foi solucionado por meio da correção dos parâmetros de conexão, permitindo que o sistema voltasse a rodar corretamente e os cadastros fossem realizados com sucesso. A abordagem de teste unitário foi eficaz para detectar falhas no código, enquanto o teste de caixa preta, realizado com o Postman, complementou a validação ao simular o comportamento do cliente. Com isso, foi possível garantir um bom funcionamento do sistema, entregando um resultado satisfatório.


