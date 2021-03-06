# Desafio Stone

## Ferramentas

Para a resolução desses desafios foi utilizado Python com o auxílio do Jupyter e das bibliotecas: Pandas e Matplotlib.

## Processo

#### - What is the average age of the customers in the database?:
Primeiro verifiquei se havia a ocorrência de `customers_id` repetidos, após isso calculei a média da coluna `age` arredonda o seu valor para duas casas decimais. Obtendo o resultado da média de idade dos clientes igual a: 35,06 ≅ 35 anos

#### - How is the `card_family` ranked based on the `credit_limit` given to each card?:
Primeiro verifiquei se havia a ocorrência de `card_number` repetidos, após isso verifiquei os tipos de `card_family` existentes, o próximo passo foi separá-lo em grupos de acordo com sua `card_family` e verificar seus máximos e mínimos, para finalizar plotei boxplot para cada `card_family` para identificar outliers. 
Através desses métodos foi possivél determinar que o ranque baseado no `credit_limit` considera os intervalos a seguir:

- Gold = [ 2.000 ; 50.000 ]
 
- Platinum = [ 51.000 ; 200.000 ]
 
- Premium: Para o Premium não foi possível determinar um intervalo especifico, uma vez que não foram encontrados outliers dentro do boxplot e o limite minimo é de 108.000 que estaria dentro do intervalo Platinum, o que permite concluir que para o ranqueamento Premium não é só considerado o `card_limit`. Outra conclusão que pode ser obtida é que se o `card_limit` for superior a 200.000 a `card_family` será definida como Premium.

#### - For the transactions flagged as fraud, what are the ids of the transactions with the highest value?:
Primeiro fiz a seleção das transações fraudulentas dentro do data frame das transações, para que fosse possível obter o dado `value` para as transações fraudulentas, após isso ordenei o data frame gerado em ordem decrescente em relação ao `value`, para finalizar pedi para que me printasse o `id` e o `value` do primeiro valor desse data frame obtendo a conclusão: A maior transação fraudulenta, possui o id = CTID20567160 e o valor de = 49155R$

#### - Analyze whether or not the fraudulent transactions are somehow associated to other features in the dataset. Explain your results: 
Primeiro foram feitas diversas seleções utilizando os data frames: `fraud` e `transactions`, com isso utilizando os data frames gerados tentei identificar padrões entre `frauds` e `card_family`, sem sucesso decidi plotar um histograma considerando o `value`, com a vizualição do histograma foi possível verificar uma maior ocorrência de transferências fraudulentas no intervalo de valores entre 30.000 e 40.000. Comparando a quantidade de transferências fraudulentas no intervalo [30.000 - 40.000] com os outros intervalos foi possível determinar que no intervalo [30.000 - 40.000] há aproximadamente duas vezes mais ocorrência de fraudes que nos demais. Segue abaixo a tabela que ilustra as observações relatadas.

   ![Captura de Tela 2021-03-18 às 13 33 39](https://user-images.githubusercontent.com/62664736/111662305-8f3c6c00-87ee-11eb-85e6-95b70b74f289.png)

 




