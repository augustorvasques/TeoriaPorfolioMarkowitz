# TeoriaPorfolioMarkowitz
Criado com a intenção de aplicar os conceitos da Teoria de Portfolio de Markowitz para a alocação de ativos em uma carteira de investimento. Dessa forma, o usuário informa os tickers dos ativos que deseja coletar as cotações.
A partir desses dados, são separadas as cotações de fechamento que foram definidas como as que serão utilizadas, e assim feitas algumas etapas de análise exploratória.
O usuário também informa uma composição inicial da carteira para que seja feito o cálculo do retorno do portfólio de forma ponderada. Além disso, o risco seguindo a fórmula da teoria também é calculado:
![image](https://github.com/augustorvasques/TeoriaPorfolioMarkowitz/assets/166548437/fb21b055-414d-4487-94e4-ef2a510619f5)

Assim é calculdo o Índice Sharpe considerando o risco livre como zero neste caso, já que o foco estará na comparação de carteiras.
![image](https://github.com/augustorvasques/TeoriaPorfolioMarkowitz/assets/166548437/f359dc32-8684-45c5-bdc3-e5a3f92b832f)

em que:

Rp é a rentabilidade do portfólio,

Rf é o retorno livre de risco a ser considerado,

σp é o risco que o cálculo foi indicado acima.

Posteriormente é definida uma função que cria aleatoriamente pesos para os ativos informados e faz novos cálculos do risco e retorno destes, obtendo também o Índice Sharpe.
Essa geração de grande número de carteiras permite criar um gráfico em que é possível ver a fronteira eficiente, na qual indica que para os riscos tolerados indicados no eixo x
existe um valor máximo de retorno que está nessa fronteira. Ou seja, carteiras que estão verticalmente abaixo dessa linha são ineficientes já que existe uma outra carteira, com
esses mesmos ativos mas em composição diferente que pode entregar um retorno maior correndo o mesmo ou até mesmo menos risco. Retornos superiores aos da linha são considerados
improváveis.

Como podem existir diferentes investidores e estratégias, criei uma outra função que agora calcula novas carteiras mas busca por alocações que atinjam retornos maiores que os
da carteira atual informada, mas com um risco igual ou menor. Por fim, caso exista uma ou mais carteiras que satisfaçam esses requisitos, é plotado um novo gráfico agora comparativo
para mostrar a diferença dentre a carteira atual e essa com melhor desempenho considerando o risco máximo = risco atual, além de uma tabela com as 3 carteiras: atual, mais eficiente
com risco limitado, e a mais eficiente segundo o índice sharpe.
