# GradientBoosting
## Intro
Rusty Bargain is a used car sales service that is developing an app to attract new customers. In this app, you can quickly find out the market value of your car. You have access to historical data, technical specifications, trim versions and prices. You need to build the model to determine the value.
Rusty Bargain is interested in:

the quality of the prediction

the speed of prediction

the time required for training

### Notes:
- Use the REQM metric to evaluate the models.
- You can use a special command to find the execution time of the cell code in Jupyter Notebook.


### Data description
* DateCrawled - date on which the profile was downloaded from the database
* VehicleType - vehicle body type
* RegistrationYear - year the vehicle was registered
* Gearbox - type of transmission
* Power - power (hp)
* Model - vehicle model
* Mileage - mileage (measured in km due to the regional specificities of the dataset)
* RegistrationMonth - vehicle registration month
* FuelType - fuel type
* Brand - vehicle make
* NotRepaired - vehicle repaired or not
* DateCreated - profile creation date
* NumberOfPictures - number of photos of the vehicle
* PostalCode - postal code of the profile owner (user)
* LastSeen - date of the user's last activity

**Target**
* Price - (Euro)

## Libraries used

import **pandas** as pd

import **numpy** as np

import **seaborn** as sns

from **matplotlib** import pyplot as plt

from **sklearn.model_selection** import train_test_split 

import **lightgbm** as lgb

from **sklearn** import metrics

from **sklearn.model_selection** import cross_val_score

from **sklearn.metrics** import mean_squared_error

from **sklearn.ensemble** import RandomForestRegressor

from **catboost** import CatBoostRegressor

import **xgboost** as xgb

from **sklearn.model_selection** import GridSearchCV

## Conclusion

The best model was catboost with the hyperparameters: {'depth': 10, 'iterations': 300, 'l2_leaf_reg': 1, 'learning_rate': 0.2}. Obtaining a score of -1747.204790443197 in negative root mean squared error.

This means that the training set was 1747.204790443197 Euros away from the ideal price. And the prediction, together with the test set, was 1739.5135540945873 Euros away from the ideal price, achieving even better performance and all this in just 51.2 seconds for the best model fit, which is excellent.

For example, if you put your car in this project it would be approximately 1739.5135540945873 Euros away from the ideal price. Considering this dataframe's price range of up to 20000, a variance of less than 2000 is a good performance, as it is less than 10%.

# GradientBoosting
## Introdução
A Rusty Bargain é um serviço de venda de carros usados que está desenvolvendo um aplicativo para atrair novos clientes. Nesse aplicativo, você pode descobrir rapidamente o valor de mercado do seu carro. Você tem acesso a dados históricos, especificações técnicas, versões de acabamento e preços. Você precisa construir o modelo para determinar o valor.
A Rusty Bargain está interessada em:

a qualidade da previsão

a velocidade da previsão

o tempo necessário para o treinamento

### Observações:
- Use a métrica REQM para avaliar os modelos.
- Você pode usar um comando especial para encontrar o tempo de execução do código da célula no Jupyter Notebook.


### Descrição dos dados
* DateCrawled - data em que o perfil foi baixado do banco de dados
* VehicleType - tipo de carroceria do veículo
* RegistrationYear - ano em que o veículo foi registrado
* Gearbox (Caixa de câmbio) - tipo de transmissão
* Potência - potência (hp)
* Model - modelo do veículo
* Mileage - quilometragem (medida em km devido às especificidades regionais do conjunto de dados)
* RegistrationMonth - mês de registro do veículo
* FuelType - tipo de combustível
* Brand - marca do veículo
* NotRepaired - veículo consertado ou não
* DateCreated - data de criação do perfil
* NumberOfPictures - número de fotos do veículo
* PostalCode - código postal do proprietário do perfil (usuário)
* LastSeen - data da última atividade do usuário

**Alvo**
* Preço - (Euro)

## Bibliotecas usadas

import **pandas** as pd

import **numpy** as np

import **seaborn** as sns

from **matplotlib** import pyplot as plt

from **sklearn.model_selection** import train_test_split 

import **lightgbm** as lgb

from **sklearn** import metrics

from **sklearn.model_selection** import cross_val_score

from **sklearn.metrics** import mean_squared_error

from **sklearn.ensemble** import RandomForestRegressor

from **catboost** import CatBoostRegressor

import **xgboost** as xgb

from **sklearn.model_selection** import GridSearchCV

## Conclusão

O melhor modelo foi o catboost com os hiperparâmetros: {'depth': 10, 'iterations': 300, 'l2_leaf_reg': 1, 'learning_rate': 0,2}. Obtendo uma pontuação de -1747,204790443197 na raiz negativa do erro quadrático médio.

Isso significa que o conjunto de treinamento estava 1747,204790443197 euros distante do preço ideal. E a previsão, juntamente com o conjunto de teste, ficou a 1739,5135540945873 euros do preço ideal, obtendo um desempenho ainda melhor e tudo isso em apenas 51,2 segundos para o melhor ajuste do modelo, o que é excelente.

Por exemplo, se você colocasse seu carro nesse projeto, ele estaria a aproximadamente 1.739,5135540945873 euros de distância do preço ideal. Considerando a faixa de preço desse dataframe de até 20.000, uma variação de menos de 2.000 é um bom desempenho, pois é inferior a 10%.


