# Desafio - Construindo um modelo de Regressão para marketing:
### Índice

- [Contextualização](#contextualização)
- [Metodologia Aplicada](#metodologia-aplicada)
- [Entendimento do Negócio Aplicada](#metodologia-aplicada)
  - [Metricas](#metricas)
- [Entendimento dos Dados](#entendimento-dos-dados)
  - [Variáveis](#variáveis)
  - [Shape](#shape)
  - [Describe](#describe)
  - [Verificando Valores Nulos](#verificando-valores-nulos)
  - [Verificando Valores Duplicados](#verificando-valores-duplicados)
  - [Verificando Tipos](#verificando-tipos)
  - [Verificando a distribuição da coluna 'sales'](#verificando-a-distribuição-da-coluna-sales)
  - [Identificando outliers](#identificando-outliers)
  - [Identificando correlação](#identificando-correlação)
  - [Investimento por plataforma](#investimento-por-plataforma)

- [Preparação dos Dados](#preparação-dos-dados)

- [Modelagem](#modelagem)

- [Avaliação](#avaliação)
- [Implantação](#implantação)

- [Ambiente virtual e Dependências](#ambiente-virtual-e-dependências)


### Contextualização:
Uma empresa está investindo mensalmente em plataformas de publicidade online,
como Youtube, Facebook e newspaper, para a prospecção de leads (pessoas
interessadas em seus produtos). A fim de acompanhar o desempenho desses
investimentos, a empresa registra todos os gastos com publicidade e todos os retornos
de vendas gerados a partir desses investimentos.

### Metodologia Aplicada:
A análise foi realizada utilizando o modelo CRISP-DM, o CRISP-DM (Cross Industry Standard Process for Data Mining) é um modelo padrão de processo para projetos de mineração de dados que define um conjunto de fases e tarefas que devem ser executadas para desenvolver soluções de mineração de dados efetivas.

![CRISP-DM](/core/img/CRISP-DM.png)

O modelo CRISP-DM é uma abordagem sistemática e estruturada para a mineração de dados que ajuda as empresas a desenvolver soluções de mineração de dados de maneira eficiente e eficaz, reduzindo o tempo e os custos do projeto.

## Entendimento do Negócio:

### Objetivo:
Para entender melhor a relação entre as variáveis presentes nesses registros e
identificar os fatores que mais impactam na geração de leads, a empresa solicitou a
análise de um especialista em dados. Além disso, a empresa busca criar um
modelo de predição de valores para estimar o retorno de vendas que pode ser gerado
a partir de um determinado investimento em publicidade.

### Variavel Targat:
identificar os fatores que mais impactam na geração de leads.

### Metricas:
A análise da correlação entre o investimento em marketing por plataforma, juntamente com a verificação dos valores investidos em cada uma delas, é fundamental.

## Entendimento dos Dados:
### Variáveis:
![Data Frame](/core/img/dataframe.png)

### Shape:
![Data Frame](/core/img/shape.png)

### Describe:
![Data Frame](/core/img/describe.png)

### Verificando Valores Nulos:
![Data Frame](/core/img/nulos.png)

### Verificando Valores Duplicados:
![Data Frame](/core/img/duplicados.png)

### Verificando Tipos:
![Data Frame](/core/img/tipos.png)

### Verificando a distribuição da coluna 'sales':
![Data Frame](/core/img/distribuição.png)

### Identificando outliers:
![Data Frame](/core/img/outliers.png)

### Identificando correlação:
![Data Frame](/core/img/correlação.png)

### Investimento por plataforma:
![Data Frame](/core/img/investimento_por_plataforma.png)

## Preparação dos Dados:
Após uma busca detalhada, concluí que os dados estavam suficientemente limpos.

## Modelagem:
### Verificando o desempenho do modelo:
![Data Frame](/core/img/modelo.png)

## Avaliação:
Com base no estudo realizado, percebemos que o investimento em jornais `newspaper` apresenta a menor correlação em relação às vendas. No entanto, é o segundo maior investimento em marketing definido pela empresa. Por outro lado, o `Facebook` possui uma correlação maior em relação ao `newspaper`, mesmo com um investimento 21% menor. Já o `YouTube` possui um valor investido em marketing 61% maior do que o investimento combinado do `Facebook` e do `newspaper`. Além disso, a correlação entre as vendas e o investimento no `YouTube` é a maior em relação a todas as outras plataformas citadas. No entanto, isso pode ser consequência do alto investimento no `YouTube` em comparação com as demais plataformas.

Com base nesses resultados, recomendamos aumentar o investimento no `Facebook` em 21% e monitorar o desempenho das vendas após o aumento. É importante verificar a correlação entre as vendas e o investimento no `Facebook`. Em relação ao investimento em jornais, ele deve ser reduzido em 21%. Aconselhamos também uma diminuição gradual no investimento no `YouTube` e realocação desses recursos no `Facebook`. Caso a correlação entre as vendas e o investimento no `YouTube` não diminua, isso indica que estamos no caminho certo. Além disso, é importante observar se a taxa de conversão através do `YouTube` não está diminuindo.

Para aprimorar a coleta de dados, é aconselhável registrar a data em que cada um desses investimentos foi feito, para que possamos avaliar o tempo de observação. Dessa forma, poderemos replicar essas análises no próximo estudo sobre o `Facebook`. Outra adição importante seria considerar a taxa de conversão por plataforma.

Em conclusão, recomendamos seguir as orientações mencionadas acima e monitorar as KPIs citadas para verificar os resultados das recomendações.

## Implantação:
Iniciando a etapa de implementação do modelo em produção.

## Ambiente virtual e Dependências:
Criando ambiente virtual:
```
python3 -m venv core/.venv
```

Entrando no ambiente virtual:
```
source core/.venv/bin/activate
```

Instale as dependências:
```
pip install -r core/requirements.txt
```
---
Linkedin: <https://www.linkedin.com/in/samuel-barbosa-dev/> 

E-mail: <samueloficial@protonmail.com>