# Funções

Funções são interessantes para quando você precisa fazer uma
determinada coisa várias vezes num mesmo script.

Uma função é como se fosse um script dentro do script, sendo assim ele
também usa o mesmo esquema de parâmetros de um script comum ($1 para
primeiro parâmetro, $2 para segunda, e todas aquelas regras explicadas em
2.4. Parâmetros com a exceção do $0, que não retorna o nome da função!).
Uma função também é capaz de retornar um valor usando o
"return ValorDeRetorno", sendo que ValorDeRetorno ficará armazenado em
"$?", vale observar também que só é possível retornar valores inteiros.
Por exemplo, se na função tiver "return 123" depois da execução desta
instrução "$?" valerá 123.

Bem... explicar com um código sempre é mais fácil! Se você acha que
vai se safar do poderoso "Hello World" está muito enganado! Aí vai ele:

{% codesnippet "./src/hello.sh" %}{% endcodesnippet %}

 Uhmmm... Sem falar muito eu já emendo outro código:

{% codesnippet "./src/maior.sh" %}{% endcodesnippet %}

Só umas informações adicionais:

- O return quando executado interrompe a execução da função e a execução
  passa para a instrução imediatamente posterior a qual a função foi
  chamada;
- O valor mais alto que uma função pode retornar é 256 e o mais baixo...
  bem, é um número de módulo grande. :P Se precisar de valores positivos
  maiores que 256 retorne-o como negativo e depois converta-o para
  positivo novamente (como? ah meu amigo... saia da frente do computador
  e vá procurar um livro de matemática!);
- Se quer saber mais detalhes sobre funções o capítulo 23 do Advanced
  Bash-Scripting Guide vai lhe ser muito útil.


Fique com mais este código que eu achei bem interessante. ;-)

{% codesnippet "./src/romano.sh" %}{% endcodesnippet %}

Ah! Deixa eu dizer só mais uma coisinha: é possível declarar
função(ões) dentro de função. Desta vez não darei exemplos, faça os
testes por conta própria! :-)

