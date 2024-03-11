# ms-ai900-challenge-1

Documento redigido como requisito para completar desafio do curso Microsoft Azure AI Fundamentals da DIO.

1. Na primeira etapa após criar o acesso a Azure, criei meu primeiro workspace de machine learning.
2. Com o workspace criado e com acesso ao Azure ML Studio começo a definir como nosso treinamento de modelo será feito.
3. Na primeira tela preencho dados básicos de identificação do job de treinamento como nome e descrição.
4. Na segunda tela defini o tipo de trabalho que é regressão já que quero estudar números passados para poder tirar conclusões.
5. Ainda nessa tela defini a fonte de dados que é a url com os dados fornecidos pela microsoft e defini o formato tabular, delimitação, cabeçalhos e o schema dos dados a ser utilizados com sua devida tipagem.
6. Definis nas telas seguinte a métrica matemática a ser utilizada e quais tipos de modelos deverão ser gerados.
7. Defini também os limites para evitar sobreutilização da máquina virtual.
8. Quaso no último paço de configuração defini como será feita a validação e teste dos modelo.
9. E por último somente escolho em qual tipo de máquina irei rodar o treinamento do modelo.
10. Após o modelo ser gerado, temos na aba de métricas os gráficos `predicted_true` e `residuals` que demonstram a performace do modelo quando testamos contra os dados reais.
11. Em seguida implantei o modelo em web service e procedi para teste.
12. Já no painel do nosso endpoint (ponto de extremidade se assim preferirem) faço o teste com o JSON abaixo retirado da documentação do LAB mas posso modificar esses parâmetros para qualquer outro.

```
{
 "Inputs": { 
   "data": [
     {
       "day": 1,
       "mnth": 1,   
       "year": 2022,
       "season": 2,
       "holiday": 0,
       "weekday": 1,
       "workingday": 1,
       "weathersit": 2, 
       "temp": 0.3, 
       "atemp": 0.3,
       "hum": 0.3,
       "windspeed": 0.3 
     }
   ]    
 },   
 "GlobalParameters": 1.0
}
```
E obtendo o seguinte resultado:
```json
{
  "Results": [
    334.52050709282594
  ]
}
```

13. Basicamente podemos entrar quais quer valores de teste para receber a previsão da quantidade de aluguéis de bicicleta a depender do dia, mês, ano estação do ano, se é feriado, dia da semana, se é dia útil, previsão do tempo, temperatura, humidade, vento...
