---
layout: page
title: Exercícios
---

1. O arquivo [inteiro_oop.tar.gz]({{ site.baseurl }}/public/files/inteiro_oop.tar.gz) contém duas implementações distintas de uma interface `Inteiro`. A implementação de `implA.c` armazena o inteiro internamente em um valor do tipo `int`. A implementação de `implB.c` armazena um ponteiro para o predecessor do inteiro, sendo que para o valor zero esse ponteiro é nulo (pois este não possui predecessor). Em `main.c`, fazemos algumas operações sobre esses inteiros, porém a última operação de soma dá algum problema, pois não resulta no número 7 como esperado. O motivo desse erro está relacionado a uma violação do paradigma de orientação a objetos. Descubra o motivo e corrija o erro.

2. O programa apresentado no exercício 1 aloca memória mas nunca libera. Essa falha de programação é conhecida como *memory leak*. Para corrigi-la, insira um novo método chamado `destruir` à interface em `inteiro.h`, e implemente-o em `implA.c` e em `implB.c`. Modifique o programa para usar esse método para liberar toda memória que for alocada. Verifique, com o auxílio do Valgrind ou do sanitizador do Clang, se você conseguiu eliminar todos os *memory leaks*.

3. Faça duas implementações da estrutura Deque: uma usando um vetor para armazenar os dados, e outra usando uma lista ligada duplamente encadeada.

4. Implemente um conjunto de redes de ordenação (*sorting networks*) para entradas com tamanho igual a algumas potências de 2. Implemente uma rotina que use *merge sort* para quebrar uma entrada de tamanho arbitrário em pedaços que suas redes possam processar. Meça o desempenho da sua implementação com relação a outros algoritmos (e.g. *quicksort*).
