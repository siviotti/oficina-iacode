# Desafio 1 CNPJ Alfanumérico

Implementar uma validação dos dígitos verificadores de um CNPJ com base na regra nova que suporta CNPJ com letras e números.

A regra de validação está descrita no arquivo [calculodvcnpjalfanaumerico.pdf](calculodvcnpjalfanaumerico.pdf) e pode ser obtida no link abaixo:
https://www.gov.br/receitafederal/pt-br/centrais-de-conteudo/publicacoes/documentos-tecnicos/cnpj/manual-dv-cnpj.pdf/view

O desafio deve ser realizado seguindo estes 3 passos:
1. Ler e compreender a documentação da regra de valização
2. Implementar uma rotina (função ou método) que efetue a validação recebendo um número de CNPJ como parâmetro e retornando um valor booleano ou erro conforme abaixo:
  * True se o CNPJ tiver seus dois dígitos válidos
  * False se o CNPJ não tiver dígitos válidos
  * Erro em caso de CNPJ inválido (tamanho, letras inválidas etc). Utilize cláusulas de guarda para verificação destes erros.
3. Criar um teste de unidade para testar a rotina (função ou método) nos seus vários cenários possíveis conforme o item 2
