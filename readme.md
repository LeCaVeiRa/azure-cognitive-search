# Azure Cognitive Search: Utilizando AI Search para indexação e consulta de Dados

## Introdução

O objetivo desse laboratório é testar algumas ferramentas de indexação, pesquisa e *document intelligence* com o recurso Azure AI Search. 

Esses experimentos foram baseados nos guias da Microsoft Learn. Para informações mais detalhadas, consulte a página [Explore an Azure AI Search index (UI)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html).


## Procedimento
Para realizar o procedimento de Document Intelligence desse exercício são necessários três recursos Azure: **Azure AI Search**, **Azure AI Services** e **Storage account**.

- Azure AI Search: esse recurso gerencia a indexação e pesquisa dos documentos.
- Azure AI Services: esse recurso contém as funcionalidades de IA necessárias para enriquecer os dados dos documentos com insights.
- Storage account: É o recurso no qual os documentos estão armazenados (em *blob containers*).


### Upload dos dados e criação do Index


As *reviews*, ou avaliações, utilizadas nesse experimento estão disponíveis [nesse link](https://aka.ms/mslearn-coffee-reviews). Uma vez criado o container de armazenamento, foi feito o upload das avaliações para o mesmo.

Com os documentos no armazenamento, temos tudo pronto para utilizar o Azure AI Search para criar um *index* e começar a extrair *insights* dos documentos. Isso pode ser feito através de um assistente presente no portal Azure, na visão geral do recurso.

Nessa etapa, é importante selecionar o *storage* em que os documentos estão armazenados, bem como as *skills* que serão usadas para enriquecer a extração de conhecimento dos documentos. Existem diversas *skills* disponíveis, é preciso selecionar aquelas que se adequam melhor ao contexto dos documentos analisados.


### Pesquisas (queries) no Index
O recurso Azure AI Search também fornece um assistente para realizar pesquisas no Index recém criado. Os resultados são retornados em JSON.

Na imagem abaixo, podemos ver uma pesquisa simples, filtrando os resultados que estão localizados na cidade de Chicago.


<div align="center">
   <img src="./assets/1.png" alt="Query by location" width="600"/>
</div>


Podemos ir além e pesquisar pelas avaliações que possuem um tom negativo de acordo com a análise de sentimentos extraída dos documentos.


<div align="center">
   <img src="./assets/2.png" alt="Sentiment analysis" width="600"/>
</div>


É interessante notar ainda as frases-chave (*keyphrases*) extraídas das avaliações. São sentenças, ou palavras chave, também obtido no processo de enriquecimento, que tentam extrair o máximo de significado do texto analisado. Apenas por meio delas é possível ter uma boa compreensão sobre o sentido geral da avaliação.


## Conclusão e Insights
Na era da informação, não basta apenas ter terabytes de dados sem ser capaz de analisá-los e extrair algo disso. É nesse contexto que as técnicas de Document Intelligence se destacam. Através dessas ferramentas é possível tornar úteis e valiosas as informações em massa que não poderiam ser analisadas individualmente por pessoas. A análise desses grandes conjuntos de dados podem revelar insights valiosos para empresas que os detém, o que faz dessa área muito proveitosa no presente contexto.