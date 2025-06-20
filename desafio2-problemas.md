# Problemas Desmembrados do Desafio 2

Os problemas devem ser lidos como possíveis prompts e antes de cada um imagine que está a expressão "Faça um código em {LANG} que..."

## Problema 1 - Ler um Arquivo com Código Fonte
Leia o conteúdo de um arquivo de qualquer linguagem de programação e obtenha o código fonte num formato texto.

## Problema 2 - Conversão e Texto em Rotinas
A partir do texto de um código fonte, crie uma lista de objetos do tipo "Rotina" que representam as funções e métodos presentes no texto.

## Problema 3 - Separação de Código dos Comentários
A partir de um texto do código fonte de uma rotina, extraia o código fonte sem comentários.

## Problema 4 - Desmembramento de Tokens
A partir de um texto do código fonte (já sem comentários) de uma rotina, extraia todos os tokens válidos e palavras reservadas para a linguagem desta rotina.

## Problema 5 - Calculo da Complexidade Ciclomática
A partir da lista de palavras reservadas presentes em uma rotina, calcule a complexidade cilomática desta rotina, contando um para a rotina e um para cada palavra reservada que gera desvio de fluxo conforme a regra de complexidade ciclomática.

## Problema 6 - Calcular Complexidade Cognitiva
A partir do texto do código fonte sem comentários de uma rotina, calcule a complexidade cognitiva desta rotina.

## Problema 7 - Listar as Rotinas e seus Atributos: Nome, Quantidade de Linhas de Código Fora Comentários (QL), Quantidade de Tokens (QT), Complexidade Ciclomática (CC) e Complexidade Cognitiva (CCOG)
A partir de uma lista de objetos do tipo Rotina, crie uma lista de rotinas utilizando os seguintes campos: Nome, Quantidade de Linhas de Código Fora Comentários (QL), Quantidade de Tokens (QT), Complexidade Ciclomática (CC) e Complexidade Cognitiva (CCOG)

## Problema 8 - Mostrar os Detalhes de uma Rotina
A partir de um único objeto Rotina, crie uma visualização de seus campos: nome, código fonte com e sem comentários, lista de tokens, Complexidade Ciclomática (CC) e Complexidade Cognitiva (CCOG)

## Problema 9 - Persistência em banco de Dados
A partir de um único objeto Rotina, faça a persistência em um banco de dados relacional Postgres deste objeto assumindo que os campos correspondem às colunas de uma tabela.

## Problema 0 (nível mais alto) - Fazer a Aplicação do Analisador
A partir dos problemas de 1 a 9, implementa uma aplicação que orquestre as chamadas a cada parte do código gerada a partir de cada problema.
