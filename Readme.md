# :busts_in_silhouette: Previsão de fluxo de clientes em um aeroporto

[Link do Google Colab](https://colab.research.google.com/drive/1Lna_c5YRh7R7HjZQpWZKgwpneyMkqlbY?usp=sharing)

#### Sobre o projeto

O projeto consiste em uma previsão sobre o fluxo de clientes em um aeroporto fictício, com base nos padrões presentes em uma Série Temporal. Este tipo de planejamento futuro pode ser útil para escolher o momento certo para expansão de um negócio, saber quando a demanda de matéria prima e mão de obra será maior, quando fazer uma promoção ou captação ativa de clientes, e afins.

#### Dataset 

[Material do curso (referência)](https://raw.githubusercontent.com/alura-cursos/deeptime/aula1/Passageiros.csv) 

Quantidade de passageiros computados em um determinado mês e ano.

## Pré-processamento

* Há tanto um padrão de crescimento global, quanto um outro padrão que se repete anualmente.

<div align="center">
  <img src="https://github.com/Tathy/Previsao_fluxo_de_clientes/blob/main/imgs/graph_temporal_dataset.png?raw=true"/>
</div>

* Os dados foram escalonados para serem melhor interpretados pelo modelo posteriormente.
## Regressão Linear

* O modelo utilizando Regressão Linear gerou uma reta crescente que acompanha o aumento gradativo de clientes do aeroporto, ano após ano.

* Entretanto, apenas com o modelo linear não é possível representar o padrão de picos anuais. É necessário um modelo mais complexo.

* Como os dados são escalonados, é necessário fazer uma transformação inversa para voltar à escala de mundo real.

<div align="center">
  <img src="https://github.com/Tathy/Previsao_fluxo_de_clientes/blob/main/imgs/graph2_real_x_predito.png?raw=true"/>
</div>

* Na predição com os dados do conjunto de teste a reta seguiu a mesma tendência do treino.

<div align="center">
  <img src="https://github.com/Tathy/Previsao_fluxo_de_clientes/blob/main/imgs/graph3_real_x_predito_test.png?raw=true"/>
</div>

## Ativação Sigmoid

* Função não-linear, para tentar ensinar ao modelo os padrões dos dados.

* Apesar do modelo estar se tornando mais complexo, a perda estava aumentando.

<div align="center">
  <img src="https://github.com/Tathy/Previsao_fluxo_de_clientes/blob/main/imgs/graph4_sigmoid.png?raw=true"/>
</div>

## Utilizando histórico de quantidade de passageiros

* Os dois modelos seguintes foram treinado apenas com o histórico de passageiros. 

* Os modelos conseguiram aprender sobre o padrão que se repete ao longo dos meses, além da tendência global de aumento no número de passageiros.

<div align="center">
  <img src="https://github.com/Tathy/Previsao_fluxo_de_clientes/blob/main/imgs/graph5_historico1.png?raw=true"/>
</div>

<div align="center">
  <img src="https://github.com/Tathy/Previsao_fluxo_de_clientes/blob/main/imgs/graph6_historico4.png?raw=true"/>
</div>

## Referências 

* Estudo desenvolvido acompanhando o curso [Deep Learning: previsão com Keras](https://cursos.alura.com.br/course/deep-learning-previsao-keras), da Alura.

:seedling:
