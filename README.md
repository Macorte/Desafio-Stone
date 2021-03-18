# Desafio Stone

## Ferramentas

Para a resolução desses desafios foi utilizado Python com o auxílio do Jupyter e das bibliotecas: Pandas e Matplotlib.

## Processo

#### What is the average age of the customers in the database?:
Primeiro verifiquei se havia a ocorrência de `customers_id` repetidos, após isso calculei a média da coluna `age` arredonda o seu valor para duas casas decimais. Obtendo o resultado da média de idade dos clientes é igual a: 35,06 anos

#### How is the `card_family` ranked based on the `credit_limit` given to each card?:
Primeiro verifiquei se havia a ocorrência de `card_number` repetidos, após isso verifiquei os tipos de `card_family` existentes, o próximo passo foi separá-lo em grupos de acordo com sua `card_family` e verificar seus máximos e mínimos, para finalizar plotei boxplot para cada `card_family` para identificar outliers. 
Através desses métodos foi possivél determinar que o ranque baseado no `credit_limit` considera os intervalos a seguir:

- Gold = [ 2.000 ; 50.000 ]
 
- Platinum = [ 51.000 ; 200.000 ]
 
- Premium: Para o Premium não foi possível determinar um intervalo especifico, uma vez que não foram encontrados outliers dentro do boxplot e o limite minimo é de 108.000 que estaria dentro do intervalo Platinum, o que permite concluir que para o ranqueamento Premium não é só considerado o card_limit. Outra conclusão que pode ser obtida é que se o card_limit for superior a 200.000 a card_family será definida como Premium.
