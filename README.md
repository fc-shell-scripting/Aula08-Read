# Read
---

Na aula anterior, vimos como passar variávei pela linha de comando, por meio de argumentos. Mas, e se desejarmos solicitar ao usuário informações durante a execução do programa? Além disso, se precisarmos solicitar a senha do usuário? Passar estes dado por linha de comando é extremamente inseguro, pois o comando fica registrado no histórico, e permite a vizualização da senha na tela do usuário. Para estes casos, podemos usar o comando _read_. Este comando faz a leitura dos dados que o usuário digitar.

O comando read pode armazenar o valor diretamente em uma variável, usando a seguinte sintaxe:
```shell
read variavel
```
O comando acima mostra na tela tudo o que for digitado, e o programa continua sua execução após o usuário teclar _enter_.

Se desejarmos solicitar a entrada de dados ao usuário, sem mostrar na tela o que está sendo digitado, podemos passar o parâmetro _-s_, para realizar a tarefa:

```shell
read -s variavel
```
O comando acima não irá mostrar em tela o que foi digitado.

### Exemplo pronto
```shell {.line-numbers}
#!/bin/bash

echo "Digite seu nome: "
read usuario
echo "Olá $usuario"
```

Para ver o conteúdo da variável, podemos usar o comando _echo "$variavel"_, que vimos em aulas passadas.

Já sabíamos como mostrar informações na tela. E agora aprendemos como buscar informações do usuário... Então temos tudo o que é necessário para criar um programa interativo...

## Exercícios
1. Crie um programa que leia o nome de um usuário e diga se este usuário está cadastrado no /etc/passwd
2. Crie um programa que leia o nome do usuário, e sua data de nascimento, e verifique se ele possui idade suficiente para dirigir.
3. Crie um programa que leia um usuário e traga todos os dados disponíveis no /etc/passwd para este usuário, utilizando awk para cortar e formatar os dados. Crie uma janela para colocar os dados dentro. Ex:

| nome    | usuario | 
| :-----: |  :---: | 
| Home    | /home/usuario |
| Shell   | /bin/bash | 

## Desafio
1. Crie um programa que funcione como uma calculadora. Ele precisa ler dois números e uma operação(+ - / *), e mostre na tela o resultado da operação.
2. Crie um arquivo que funcione como um mercado: O usuário vai digitar um produto, e o programa deve retornar o preço e a quantidade em estoque. Para armazenar os dados iniciais, crie um arquivo texto. (Iremos usar este programa em aulas futuras)
