.. Elo7 Classification documentation master file, created by
   sphinx-quickstart on Thu Jun 17 17:47:39 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Documentação Classificação Dados Elo7
=====================================

Autores
-------

* Lucas Buk Cardoso - RA: 20.84113-2

* Leonardo Vila Franca Silva - RA: 20.84071-3

* Lívia Zanfelici Fanucchi - RA: 20.84109-4

Introdução
----------

Documentação do projeto realizado na disciplina de Mineração de Dados da Pós-Graduação em Ciência de Dados e Inteligência Artificial, tem o intuito de realizar a predição de produtos em 6 categorias possíveis, sendo elas:

* Decoração;

* Papel e Cia;

* Outros;

* Bebê;

* Lembrancinhas;

* Bijuterias e Jóias.

As etapas utilizadas para atingir o objetivo do trabalho foram a leitura e análise dos dados, como correlação entre as variáveis, verificação de valores nulos e dos tipos de cada variável. Quando a etapa de divisão do dataset foi feita, os dados foram organizados de forma que o conjunto de treino tivesse os produtos mais antigos, avaliando a coluna de data da criação do mesmo, e, por consequência, o conjunto de teste contém os dados mais recentes. Após a obtenção do conjunto de dados dividido foi iniciado o pré-processamento dos dados, primeiro separando dia, mês e ano em três colunas diferentes nos dados de treinamento, depois foi realizado o processo de NLP nas colunas `query` e `title`. 

.. note::
   A coluna `concatenated_tags` não foi utilizada pois possui um valor muito grande de tags diferentes e também diversas palavras escritas com grafias incorretas, resultando em um tratamento mais trabalhoso se essa coluna fosse ser utilizada no treinamento do modelo, além de levar em conta que os modelos serão treinados com as colunas `title` e `query` principalmente, pois ambas possuem as informações textuais fundamentais.

A seguir, foi realizado a normalização das colunas numéricas, são elas: `product_id`, `seller_id`, `search_page`, `position`, `price`, `weight`, `express_delivery`, `minimum_quantity`, `view_counts`, `order_counts`, incluindo também as colunas do dia, mês e ano. A última etapa foi a de balanceaento utilizando o método de oversampling, com a finalidade de igualar a quantidade de exemplo de cada classe dos labels.
O treinamento e validação dos modelos estão apresentados em suas respectivas seções, contendo os detalhes de escolha dos modelos e também a discussão dos resultados.

.. toctree::
   :maxdepth: 2
   :caption: Projeto

   Classification