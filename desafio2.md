# Analisador de Complexidade

## Cenário principal: 
1. O analisador de complexidade fará a leitura de um arquivo com código fonte, identificará as rotinas (métodos e/ou funções) e criará uma lista com estas rotinas;
2. Cada elemento da lista (cada rotina) deve conter o código fonte original em uma lista com as linhas de código encontradas no arquivo (incluindo comentários);
3. Cada rotina deve ser capaz de informar as linhas de código "puro" (sem comentários);
4. Cada rotina deve ser capa de informar uma lista de tokens válidos com base na linguagem do arquivo bem como uma lista somente com as palavras reservadas.
5. O analisador deve calcular a complexidade ciclomática para cada rotina com base nas palavras reservadas que  desviam fluxo em cada linguagem;
6. O analisador deve calcular a complexidade cognitiva para cada rotina com base na regra do SonarQube;
7. O analisador deve gerar uma visualização com uma lista de rotinas para que possa ser escolhida uma para visualização indidual desta rotina.
8. O analisador deve gerar uma visualização das estatísticas de uma rotina (linhas originais, linhas de código, tokens, complexidade ciclomática, complexidade cognitiva);

## Regras de negócio:
A. O analisador deve ser capaz de executar para arquivos com código fonte nas seguintes linguagens: Python, Javascript, Java, C e GO.
B. O analisador deve ser capaz de executar o cenário principal para vários arquivos de várias linguagens e acumular o resultado numa única lista.
