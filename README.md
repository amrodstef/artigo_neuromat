# artigo_neuromat

## Apresentação
Estes códigos se referem à metodologia utilizada em uma publicação submetida à Revista Eletrônica de Comunicação, Informação e Inovação em Saúde (RECIIS), da Fundação Oswaldo Cruz (Fiocruz). O desenvolvimento do artigo contou com apoio da Fundação de Amparo à Pesquisa do Estado de São Paulo (FAPESP), Brasil, processo nº 2025/01835-6, como parte das atividades do Centro de Pesquisa, Inovação e Difusão em Neuromatemática  (CEPID NeuroMat) da FAPESP, processo nº 2013/07699-0. A pesquisa de João Alexandre Peschanski, um dos autores, é apoiada pelo projeto "Bridging AI and cultural heritage for a better future" (European Commission Grant Agreement ID: 101203096).

O artigo apresenta o título provisório de "Entre exposição e busca: mídia, Wikipédia e circulação do conhecimento científico em ecossistemas digitais" e  buscou explorar as relações temporais entre a ocorrência de determinados termos de interesse, dentro do contexto do CEPID NeuroMat, e o acesso a verbetes da Wikipédia correspondentes aos termos identificados.

O artigo submetido tem autoria de André M. Rodeguero Stefanuto; João Alexandre Peschanski e Fernando J. da Paixão.

## Composição
O repositório conta com arquivos utilizados para as análises descritas. São eles:
1. "artigo_neuromat.Rproj" --> Representa o arquivo de gerenciamento do projeto, utilizado junto ao RStudio.<br> <br>
2. "artigo_wiki_midia.Rmd" --> É o arquivo de texto (Rmarkdown) que contém códigos e instruções de execução, assim como outros comentários;<br> <br>
3. "dados_publicacoes.csv" --> Arquivo que contémas publicações que compõem o _corpus_ da pesquisa. Ele contém variáveis:
  - a.  data: data da publicação;
  - b. link_direto: link de acesso à publicação, tanto direto na página do veículo quanto via wayback machine;
  - c. status_direto: identificando se o texto foi obtido pelo link direto (functinoal) ou via wayback machine (wayback);
  - d. texto_completo: contém o texto coletado manualmente das publicações acessadas e armazenado em planilha para importação no Rstudio e análise
  - e. idioma: contém apenas publicações em PT-BR;
  - f. data_mes: contém a redução da data de publicação a apenas períodos mensais, agrupados sempre no primeiro dia do mês.<br> <br>
4. "freq_tokens.csv" --> apresenta a frequência geral dos termos no texto e foi gerado durante as análises, conforme "artigo_wiki_midia.Rmd". As variáveis são:
  - feature: o termo avaliado;
  - frequency: o número de ocorrências no banco de dados;
  - rank: a posição de ranqueamento da frequencia dentro do banco de dados;
  - docfreq: o número de documentos em que aquele termo aparece;
  - group: "all" representa que a contagem foi realizada em todo o banco de dados, sem agrupamentos internos.<br> <br>
5. "pageviews.csv" --> arquivo também exportado durante a execução dos códigos. Faz referência aos verbetes analisados.
  - termo: contém uma nomenclatura unificada com os termos analisados para identificar a correspondência com so termos;
  - data_mes: contém a redução da data a apenas períodos mensais, agrupados sempre no primeiro dia do mês;
  - views: número de visualizações naqueles verbete e mês;<br> <br>
6. "relacao_agrupamentos.odt" --> Contém a relação de termos agrupados durante o processo de contagem dos termos. Esses dados também podem ser conferidos junto ao fluxo em "artigo_wiki_midia.Rmd".<br><br>
## Instruções
As análises foram realizadas com apoio da linguagem R de programação (versão 4.5.1), em sua interface Rstudio (versão 2026.01.1+403), em Windows. Por isso, são esses são requisitos para a reprodução do fluxo de análise.
Os pacotes necessários para a execução do código também devem ser instalados, conforme apresentado em "artigo_wiki_midia.Rmd".

As análises foram realizadas em projetos criados dentro da própria interface. Por isso, para reproduzir o conteúdo, recomenda-se:

1. Baixar localmente todo o conteúdo deste repositório, em uma mesma pasta.
2. Executar o arquivo "artigo_neuromat"(Rstudio Project File). Isso dará acesso a todos os demais arquivos diretamente no RStudio, desde que eles estejam no mesmo diretório do computador.
3. Em seguida, siga as etapas indicadas no próprio código, presente em "artigo_wiki_midia.Rmd". Tratando-se de um arquivo Rmarkdown, é possível inserir tanto textos quanto códigos de forma complementar. Assim, as etapas estarão descritas no próprio documento. Isso inclui a instalação dos pacotes
