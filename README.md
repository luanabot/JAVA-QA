# Plano de teste

## Introdução

Foi realizado um teste do código utilizando a IDE IntelliJ. Ao tentar rodar o projeto, foi identificado um erro de conexão com o banco de dados. O teste unitário focou principalmente no arquivo application.properties, onde estavam definidos os parâmetros necessários para essa conexão. Constatou-se que a URL configurada no arquivo não era compatível com a URL do banco de dados utilizado no projeto.

## Ambiente de teste

1. IntelliJ IDEA (utilizando o JDK versão 11)

2. Dbeaver

3. Postman

## Abordagem de teste

Ao tentar rodar código no inteliji, o erro de conexão com banco de dados foi evidenciado.

![image](https://github.com/user-attachments/assets/f1a9efd3-1d45-4cd1-ae14-5a237392c7dd)

Foi realizado um teste de caixa branca para verificar o código que foi programado, identificar erros, realizar testes unitários e testar as funções. O teste foi focado nas funções no contexto das classes do código. Neste caso, foi feita uma verificação direta no application.properties, onde se encontram as configurações de conexão com o banco de dados, e foi identificada uma inconformidade.

### CORREÇÃO

db.datasource.jdbcurl=jdbc:mysql://cleberleao.com:3306/cleberleao_oficina?allowPublicKeyRetrieval=true&useSSL=false
db.datasource.username=cleberleao_oficina
db.datasource.password=mysql123oficina

![image](https://github.com/user-attachments/assets/79a04fe4-5fa7-410d-823a-40b542d6d094)

Após o teste foi realizado a conexão no Dbeaver

![image](https://github.com/user-attachments/assets/3b085640-c28d-43a2-be1d-1600e8a31f4f)

E verificado se o banco de dados estava correto utilizando o comando "select * from tb_user"

![image](https://github.com/user-attachments/assets/ad702923-2248-4729-8142-696185ea3d8e)


Além disso, foi realizado um teste de caixa preta com a utilização do Postman, uma ferramenta que permite testar requisições HTTP de forma prática e visual, sendo muito utilizada para validar endpoints de APIs e simular o comportamento do usuário final sem acesso direto ao código-fonte.

Criação de usuário:

![image](https://github.com/user-attachments/assets/ad86090e-51ee-4985-9558-ed203bae9298)

Login:

![image](https://github.com/user-attachments/assets/d14015a2-7e0a-4511-afeb-1975c90f48a0)

Verificação de usuário:

![image](https://github.com/user-attachments/assets/64811566-bca1-44d3-9e66-85a5d0d3ba77)

Verificação no banco de dados:

![image](https://github.com/user-attachments/assets/d0dfe501-44d1-4515-84f1-f1bf3d3077e9)

### Resumo

1. Abrir o projeto na IDE IntelliJ.

2. Garantir que o JDK 11 esteja configurado corretamente.

3. Executar o projeto utilizando o modo Debug do IntelliJ.

4. Monitorar os logs para identificar falhas de conexão.

5. Utilizar o DBeaver para validar as credenciais e a URL de conexão com o banco.

6. Usar o Postman para testar os endpoints da aplicação (caso o projeto envolva APIs).


## Conclusão

O erro identificado foi solucionado por meio da correção dos parâmetros de conexão, permitindo que o sistema voltasse a rodar corretamente e os cadastros fossem realizados com sucesso. A abordagem de teste unitário foi eficaz para detectar falhas no código, enquanto o teste de caixa preta, realizado com o Postman, complementou a validação ao simular o comportamento do cliente. Com isso, foi possível garantir um bom funcionamento do sistema, entregando um resultado satisfatório.


