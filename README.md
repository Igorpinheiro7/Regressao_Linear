# Regressao_Linear

# Base_de_dados
Utilizamos como inspiração a famosa base de dados [House Price do Kaggle](https://www.kaggle.com/code/ahmedmahmoud16/house-prices-regression). Fiz algumas transformações na base de dados apresentada neste projeto. a base de dados utilizada está dísponivel no repositório para download.


![Image](https://github.com/user-attachments/assets/935d8b79-1dbc-4aff-a144-5dd82bef3fb7)


Confira abaixo os campos disponíveis para análise:

area_primeiro_andar: Refere-se à área do primeiro andar da propriedade, medida em metros quadrados.

existe_segundo_andar: Esta variável é binária, indicando se a propriedade possui ou não um segundo andar. Pode ser representada como 1 para "sim" e 0 para "não".

area_segundo_andar: Se a propriedade tiver um segundo andar, esta variável representa a área total do segundo andar, medida em metros quadrados.

quantidade_banheiros: Indica o número total de banheiros na propriedade.

capacidade_carros_garagem: Esta variável indica a capacidade da garagem da propriedade, ou seja, o número máximo de carros que podem ser estacionados na garagem.

qualidade_da_cozinha_Excelente: Esta é uma variável categórica que avalia a qualidade da cozinha na propriedade. Neste caso, assume-se que se a cozinha for considerada "Excelente" é representada por 1, e caso contrário, por 0.

preco_de_venda: Este é o preço de venda da propriedade em reais. É a variável alvo que se tenta prever usando os outros atributos da propriedade.

# Introdução
Neste repositório, estabelecemos o preço de venda de casas, analisando as diversas características que influenciam sua precificação. Para alcançar esse objetivo, utilizei a regressão linear como metodologia. Vale lembrar que todas as análises foram realizadas no Colab para facilitar o processo.


# Análise Visual dos Dados
Olhando para a distribuição dos pontos azuis, podemos tirar algumas conclusões rápidas de análise de dados:

Tendência Positiva: Existe uma correlação positiva clara. À medida que a "Area do primeiro andar" aumenta (indo para a direita), o "Preço de venda" também tende a subir (indo para cima).

Concentração: A maior densidade de imóveis está concentrada em áreas entre 50 e 150 unidades de tamanho, custando até 1.5 milhão.

Outliers (Valores Discrepantes): Há alguns pontos isolados no topo. Por exemplo, um imóvel com cerca de 170 de área foi vendido por mais de 3 milhões (um valor bem acima da média para aquele tamanho), enquanto outros imóveis com área maior (próximos a 200) foram vendidos por valores menores.


<img width="683" height="743" alt="Image" src="https://github.com/user-attachments/assets/9b92ec14-68bf-4f72-9067-a986a935c7f0" />


# Explicando a Reta

Ajustamos uma reta entre o  $m^2$ do primeiro andar e o preço da casa. Queremos explicar o preço da casa a partir do seu tamanho, por isso dizemos que:

Variável explicativa/independente: Área do primeiro andar

Variável resposta/dependente: Preço da casa

<img width="1425" height="450" alt="Image" src="https://github.com/user-attachments/assets/c0ba04b7-e469-4468-8532-133e1f896408" />

# Distribuição do Preço de Vendas

Assimetria à Direita (Right-Skewed / Positive Skew): A maior parte dos imóveis está concentrada entre 500 mil e 1 milhão (onde estão as barras mais altas). Conforme o preço aumenta, a "cauda" do gráfico vai se alongando de forma tênue para a direita, estendendo-se até os 3 milhões. Isso é extremamente comum em dados imobiliários, onde a maioria dos imóveis tem preços moderados e poucos têm valores muito elevados (imóveis de luxo).

Moda/Pico: O preço mais frequente (o pico do gráfico) está ligeiramente acima de 500 mil, por volta de 700 mil.

<img width="595" height="726" alt="Image" src="https://github.com/user-attachments/assets/bc53925a-182f-4bb5-8a04-3396cecc59a2" />
