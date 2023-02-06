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

## Referências 

* Estudo desenvolvido acompanhando o curso [Deep Learning: previsão com Keras](https://cursos.alura.com.br/course/deep-learning-previsao-keras), da Alura.

:seedling:
