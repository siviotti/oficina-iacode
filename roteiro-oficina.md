# Oficina de Decomposição de Problemas com IA Code

## Prática 1 - CNPJ Alfanumérico (Desafio 1)
1. Os alunos pedem para uma IA code que implemente um código de validação de dígitos verificadores do CNPJ com formato alfanumérico (novo, aceitando letras e números) sem mais recursos.
2. Os alunos avaliam se o código gerado já leva em consideração a nova regra que usa CNPJ com letras e números e não só números.
3. Se a regra estiver incorreta, os alunos buscam a regra de validação (PDF no site da Receita Federal ou Gov.br) e pedem novamente para geração do código de validação.
4. Os alunos pedem que a validação tenha uma cláusula de guarda para validar o formato do parâmetro de entrada usando uma regex.

* Takeaway - Os alunos refletem se a regex e a cláusula de guarda é um problema separado ou não do método de validação. Se pode ser reusado ou extraído para função separada.

## Prática 2 - Analisador de Complexidade em um Único Prompt (Desafio 2 - sem as regras de negócio A e B)
1. Os alunos pedem para uma IA code que realizem o desafio 2 conforme o enunciado abaixo:
```
Implementa um analisados de complexidade conforme descrito abaixo:
Implementa um analisados de complexidade conforme descrito abaixo:
1. O analisador de complexidade fará a leitura de um arquivo com código fonte, identificará as rotinas (métodos e/ou funções) e criará uma lista com estas rotinas;
2. Cada elemento da lista (cada rotina) deve conter o código fonte original em uma lista com as linhas de código encontradas no arquivo (incluindo comentários);
3. Cada rotina deve ser capaz de informar as linhas de código "puro" (sem comentários);
4. Cada rotina deve ser capa de informar uma lista de tokens válidos com base na linguagem do arquivo bem como uma lista somente com as palavras reservadas;
5. O analisador deve calcular a complexidade ciclomática para cada rotina com base nas palavras reservadas que desviam fluxo em cada linguagem;
6. O analisador deve calcular a complexidade cognitiva para cada rotina com base na regra do SonarQube;
7. O analisador deve gerar uma visualização com uma lista de rotinas para que possa ser escolhida uma para visualização indidual desta rotina;
8. O analisador deve gerar uma visualização das estatísticas de uma rotina (linhas originais, linhas de código, tokens, complexidade ciclomática, complexidade cognitiva).
```
2. Os alunos devem observar a avaliar o resultado gerado e o quanto ele funciona e atendeu o enunciado além de avaliar se o problema foi eficazmente desmembrado.
3. 3. Os alunos pedem que sejam implementados testes de unidade necessários.
4. Os alunos devem avaliar se os algoritimos de complexidade estão corretos, caso conheçam.

* Takeaway 1 - Vai funcionar rápido, mas o design está na mão da IA - não houve design humano
* Takeaway 2 - Partes do problema não são debatidos nem pensados pelos alunos
* Takeaway 3 - Pontos de extensão são ignorados (regra de negócio A e B)
* Takeaway 4 - Para uma divisão de tarefas como seria a divisão do código?
* Takeaway 5 - Complexidade não é de conhecimento dos alunos, mas eles precisam validar o código feito pela IA.

## Prática 3 - Decomposição do Analisador
1. Os alunos criam um prompt pedindo uma solução de decomposição do problema para o cenário completo (com regras A e B) conforme abaixo:
```
Implementa um analisados de complexidade conforme descrito abaixo:
1. O analisador de complexidade fará a leitura de um arquivo com código fonte, identificará as rotinas (métodos e/ou funções) e criará uma lista com estas rotinas;
2. Cada elemento da lista (cada rotina) deve conter o código fonte original em uma lista com as linhas de código encontradas no arquivo (incluindo comentários);
3. Cada rotina deve ser capaz de informar as linhas de código "puro" (sem comentários);
4. Cada rotina deve ser capa de informar uma lista de tokens válidos com base na linguagem do arquivo bem como uma lista somente com as palavras reservadas;
5. O analisador deve calcular a complexidade ciclomática para cada rotina com base nas palavras reservadas que desviam fluxo em cada linguagem;
6. O analisador deve calcular a complexidade cognitiva para cada rotina com base na regra do SonarQube;
7. O analisador deve gerar uma visualização com uma lista de rotinas para que possa ser escolhida uma para visualização indidual desta rotina;
8. O analisador deve gerar uma visualização das estatísticas de uma rotina (linhas originais, linhas de código, tokens, complexidade ciclomática, complexidade cognitiva).
Regras de negócio:
A. O analisador deve ser capaz de executar para arquivos com código fonte nas seguintes linguagens: Python, Javascript, Java, C e GO.
B. O analisador deve ser capaz de executar o cenário principal para vários arquivos de várias linguagens e acumular o resultado numa única lista.
```
2. Os alunos especificam a linguagem de sua preferência e pedem que a IA faça um design modular e que permita trabalho de várias pessoas nas várias partes do problema, incluindo os pontos de extensão das regra A e B.
3. Os alunos pedem que sejam implementados testes de unidade necessários
4. Os alunos devem avaliar se os algoritimos de complexidade estão corretos, caso conheçam.

* Takeaway 1 - É necessário criar um "modelo" com o objeto Rotina que é usado em várias partes do problema - especificar "Rotina" é caminho crítico
* Takeaway 2 - É necessário gerar pontos de extensão para as várias linguagens que são pedidas e as que provavelmente entrarão na lista (feature futura bem provável)
* Takeaway 3 - A decomposição facilita o teste das partes envolvidas
* Takeaway 4 - Complexidade não é de conhecimento dos alunos, mas eles precisam validar o código feito pela IA.

## Prática 4 - Implementar Soluções com base na Decomposição Padrão (10 Problemas)
1. Os alunos devem solicitar a implementação e testes de unidade dos problemas menores ja decompostos conforme listado abaixo.
2. Os alunos pedem a implementação e teste de unidade do "Problema 0" que é a integração dos demais problemas. 
```
Problema 1 - Ler um Arquivo com Código Fonte
Leia o conteúdo de um arquivo de qualquer linguagem de programação e obtenha o código fonte num formato texto.

Problema 2 - Conversão e Texto em Rotinas
A partir do texto de um código fonte, crie uma lista de objetos do tipo "Rotina" que representam as funções e métodos presentes no texto.

Problema 3 - Separação de Código dos Comentários
A partir de um texto do código fonte de uma rotina, extraia o código fonte sem comentários.

Problema 4 - Desmembramento de Tokens
A partir de um texto do código fonte (já sem comentários) de uma rotina, extraia todos os tokens válidos e palavras reservadas para a linguagem desta rotina.

Problema 5 - Calculo da Complexidade Ciclomática
A partir da lista de palavras reservadas presentes em uma rotina, calcule a complexidade cilomática desta rotina, contando um para a rotina e um para cada palavra reservada que gera desvio de fluxo conforme a regra de complexidade ciclomática.

Problema 6 - Calcular Complexidade Cognitiva
A partir do texto do código fonte sem comentários de uma rotina, calcule a complexidade cognitiva desta rotina.

Problema 7 - Listar as Rotinas e seus Atributos: Nome, Quantidade de Linhas de Código Fora Comentários (QL), Quantidade de Tokens (QT), Complexidade Ciclomática (CC) e Complexidade Cognitiva (CCOG)
A partir de uma lista de objetos do tipo Rotina, crie uma lista de rotinas utilizando os seguintes campos: Nome, Quantidade de Linhas de Código Fora Comentários (QL), Quantidade de Tokens (QT), Complexidade Ciclomática (CC) e Complexidade Cognitiva (CCOG)

Problema 8 - Mostrar os Detalhes de uma Rotina
A partir de um único objeto Rotina, crie uma visualização de seus campos: nome, código fonte com e sem comentários, lista de tokens, Complexidade Ciclomática (CC) e Complexidade Cognitiva (CCOG)

Problema 9 - Persistência em banco de Dados
A partir de um único objeto Rotina, faça a persistência em um banco de dados relacional Postgres deste objeto assumindo que os campos correspondem às colunas de uma tabela.

Problema 0 (nível mais alto) - Fazer a Aplicação do Analisador
A partir dos problemas de 1 a 9, implementa uma aplicação que orquestre as chamadas a cada parte do código gerada a partir de cada problema.
```
* Takeaway 1 - Os alunos devem perceber que os problemas tem esteriótipos padrão do DDD: Problemas de 2 a 6 são de domínio e negócio (Domain), problemas 7 e 8 são de visualização (View), problemas 1 e 9 são de infraestrutura (Infra) e o problema 0 é um controle ou a própria aplicação (App).
* Takeaway 2 - Os esteriótipos teriam cada um suas necessidades de RNF e preocupações particulares. Domain deveria usar o máximo de funções puras e testes pois são o ponto quente de mudanças, View e App (Portas) tendem a usar algum framework MVC ou similar e a Infra tende a fazer integração com outros ativos (BD, Serviços e adaptadores em geral)
  
