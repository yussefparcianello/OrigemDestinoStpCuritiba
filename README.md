# Protótipo de visualização de Origem-Destino do Sistema de Transporte Público
<img src="https://raw.githubusercontent.com/yussefparcianello/OrigemDestinoStpCuritiba/master/images/fig02.jpg">
https://www.youtube.com/watch?v=KOzFHRc7lXA

## Principais arquivos da aplicação
+ **index.php**: é o arquivo inicial da aplicação. É responsável por dividir a interface de usuário verticalmente ao meio, estabelecendo à esquerda da tela a região do mapa e do menu, e à direita da tela a região dos gráficos

+ **tela_inicial.php**: é o arquivo responsável pela construção do menu de busca da aplicação

+ **bd_rois.php**: contém o script escrito em linguagem PHP responsável por montar sentença SQL responsável buscar na tabela transporte_dinamico.yp_rois os dados referentes aos contornos das Regiões de Interesse oferecidas pela aplicação para explorar os dados de OD do STP de Curitiba

+ **bd_terminais.php**: contém o script escrito em linguagem PHP responsável por montar sentença SQL responsável buscar na tabela transporte_dinamico.yp_terminais os dados referentes aos terminais de embarque e desembarque do STP de Curitiba

+ **bd_movimentacao.php**: contém o script escrito em linguagem PHP responsável por montar sentença SQL responsável buscar na tabela transporte_dinamico.np_movimentacao os dados referentes ao embarque e desembarque dos usuários do STP de Curitiba

+ **bd_pontos_de_onibus.php**: contém o script escrito em linguagem PHP responsável por montar sentença SQL responsável buscar na tabela transporte_dinamico.yp_pontos_onibus os dados referentes aos pontos de ônibus do STP de Curitiba

+ **index_main.php**: é arquivo mais importante da aplicação. Nele está contida toda a lógica de programação referente a criação dos gráficos, criação do mapa e também das camadas que podem ser adicionadas e removidas do mapa. As consultas quando disparadas são realizadas via chamada _Query.ajax_, a qual requisita os arquivos _bd_XXXXXX.php_ para obter os dados armazenados na base.


## Dicionário de dados das tabelas utilizadas pelo protótipo
| Tabela | Campo | Descrição |
| :--- | :--- | :--- |
| rois | id | Identificador da tupla |
| rois | lat | Coordenada de latitude (SRID 4326) |
| rois | lng | Coordenada de longitude (SRID 4326) |
| rois | geom | Geometria
| pontos_onibus | id | Identificador da tupla
| pontos_onibus | lat | Coordenada de latitude (SRID 4326) |
| pontos_onibus | lng | Coordenada de longitude (SRID 4326) |
| pontos_onibus | geom | Geometria (SRID 29192)|
| terminais | id | Identificador da tupla |
| terminais | nome | Descrição do terminal |
| terminais | lat | Coordenada de latitude (SRID 4326) |
| terminais | lng | Coordenada de longitude (SRID 4326) |
| terminais | geom | Geometria (SRID 29192) |
| movimentacao | codlinha | Código da linha operada pelo ônibus |
| movimentacao | nomelinha | Nome da linha operada pelo ônibus |
| movimentacao | codveiculo | Código do veículo em operação |
| movimentacao | cartao_numero | Número do cartão do passageiro |
| movimentacao | cartao_datahora | Data-hora do uso do cartão do passageiro |
| movimentacao | cartao_data | Data do uso do cartão do passageiro |
| movimentacao | cartao_hora | Hora do uso do cartão do passageiro | 
| movimentacao | cartao_data_nascimento | Data de nascimento do passageiro | 
| movimentacao | cartao_sexo | Sexo do passageiro | 
| movimentacao | origem_lat | Coordenada de latitude da origem (SRID 4326) | 
| movimentacao | origem_lng | Coordenada de longitude da origem (SRID 4326) | 
| movimentacao | origem_datahora | Data-hora do embarque |
| movimentacao | destino_lat | Coordenada de latitude do destino (SRID 4326) | 
| movimentacao | destino_lng | Coordenada de longitude do destino (SRID 4326) |
| movimentacao | destino_datahora | Data-hora do desembarque |
| movimentacao | origem | Geometria do ponto de origem (SRID 29192) |
| movimentacao | destino | Geometria do ponto de destino (SRID 29192) |
| movimentacao | idade | Idade do passageiro | 
