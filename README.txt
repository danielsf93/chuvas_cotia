Tarefas:

-Baixar dados de pluviometro do CEMADEN na serie historica de cotia.
-Descobrir inicios dos dados
-Baixar shp de bacias hidrográficas
-Baixar dados de pluviometro do CEMADEN na serie historica dos outros municipios das mesmas bacias
-Organizar os dados csv em pastas por ano e arquivos por mesmas
-criar plataforma php/html para exibicao da página
-Criar mapa com graficos de cada ponto
-Crar graficos completos de serie historica, destacando eventos extremos
-Se possível, criar modelos matemáticos de previsão.


ANOTAÇÔES:
-Dados obtidos pelo estado mesmo.
-Dados de SP inicio em SET-2014 - 5 GB de tabelas csv. Dados brutos no google drive: https://drive.google.com/drive/folders/1kZaFcHMK8m0PjvJDC1hrY6PxFv6IJgMm?usp=sharing
-Dados de Cotia Inicio JUL-2014
-Fim de dados em abr-2024


-Dados podem ser obtidos diretamente pelo form, sem necessitar de mapa: http://www2.cemaden.gov.br/mapainterativo/download/download_form.php

-Para refinar os dados, cidade COTIA:
351300906A;SP;Santa Isabel;-23,585;-46,817
351300904A;SP;Caucaia do Alto;-23,691;-47,027
351300901A;SP;Monte Catine;-23,641;-47,0
351300907A;SP;Morro Grande;-23,65;-46,956
351300903A;SP;Jardim Adelina;-23,602;-46,931
351300905A;SP;Parque Miguel Mirizola;-23,5801;-46,9176
351300906H;SP;Rio Cotia;-23,6087;-46

Pesquisa por bacia e sub-bacia em https://datageo.ambiente.sp.gov.br/app/
Shapes: 
*Limite das Sub-Bacias Hidrográficas do Estado de São Paulo
*Limites Municipais do Estado de São Paulo 2021 (IGC)

Uni todos os csv no linux com:
"cat 2013-09.csv 2015-07.csv 2017-05.csv 2019-03.csv 2021-01.csv 2022-11.csv 2013-10.csv 2015-08.csv 2017-06.csv 2019-04.csv 2021-02.csv 2022-12.csv 2013-11.csv 2015-09.csv 2017-07.csv 2019-05.csv 2021-03.csv 2023-01.csv 2013-12.csv 2015-10.csv 2017-08.csv 2019-06.csv 2021-04.csv 2023-02.csv 2014-01.csv 2015-11.csv 2017-09.csv 2019-07.csv 2021-05.csv 2023-03.csv 2014-02.csv 2015-12.csv 2017-10.csv 2019-08.csv 2021-06.csv 2023-04.csv 2014-03.csv 2016-01.csv 2017-11.csv 2019-09.csv 2021-07.csv 2023-05.csv 2014-04.csv 2016-02.csv 2017-12.csv 2019-10.csv 2021-08.csv 2023-06.csv 2014-05.csv 2016-03.csv 2018-01.csv 2019-11.csv 2021-09.csv 2023-07.csv 2014-06.csv 2016-04.csv 2018-02.csv 2019-12.csv 2021-10.csv 2023-08.csv 2014-07.csv 2016-05.csv 2018-03.csv 2020-01.csv 2021-11.csv 2023-09.csv 2014-08.csv 2016-06.csv 2018-04.csv 2020-02.csv 2021-12.csv 2023-10.csv 2014-09.csv 2016-07.csv 2018-05.csv 2020-03.csv 2022-01.csv 2023-11.csv 2014-10.csv 2016-08.csv 2018-06.csv 2020-04.csv 2022-02.csv 2023-12.csv 2014-11.csv 2016-09.csv 2018-07.csv 2020-05.csv 2022-03.csv 2024-01.csv 2014-12.csv 2016-10.csv 2018-08.csv 2020-06.csv 2022-04.csv 2024-02.csv 2015-01.csv 2016-11.csv 2018-09.csv 2020-07.csv 2022-05.csv 2024-03.csv 2015-02.csv 2016-12.csv 2018-10.csv 2020-08.csv 2022-06.csv 2024-04.csv 2015-03.csv 2017-01.csv 2018-11.csv 2020-09.csv 2022-07.csv 2015-04.csv 2017-02.csv 2018-12.csv 2020-10.csv 2022-08.csv 2015-05.csv 2017-03.csv 2019-01.csv 2020-11.csv 2022-09.csv 2015-06.csv 2017-04.csv 2019-02.csv 2020-12.csv 2022-10.csv > serie.csv"

Iportar dados de serie.csv via mariadb para poder utilizar no phpMyadmin e tratar os dados.


inicial.ipynb usa tabela do drive abcd- os nomes nao devem ter espaços
