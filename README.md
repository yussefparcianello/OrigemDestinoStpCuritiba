# OrigemDestinoStpCuritiba
Protótipo de visualização de dados de Origem-Destino do Sistema de Transporte Público de Curitiba


## Principais arquivos da aplicação
+ **index.php**: é o arquivo inicial da aplicação. É responsável por dividir a interface de usuário verticalmente ao meio, estabelecendo à esquerda da tela a região do mapa e do menu, e à direita da tela a região dos gráficos

+ **tela_inicial.php**: é o arquivo responsável pela construção do menu de busca da aplicação

+ **bd_rois.php**: contém o script escrito em linguagem PHP responsável por montar sentença SQL responsável buscar na tabela transporte_dinamico.yp_rois os dados referentes aos contornos das Regiões de Interesse oferecidas pela aplicação para explorar os dados de OD do STP de Curitiba

+ **bd_terminais.php**: contém o script escrito em linguagem PHP responsável por montar sentença SQL responsável buscar na tabela transporte_dinamico.yp_terminais os dados referentes aos terminais de embarque e desembarque do STP de Curitiba

+ **bd_movimentacao.php**: contém o script escrito em linguagem PHP responsável por montar sentença SQL responsável buscar na tabela transporte_dinamico.np_movimentacao os dados referentes ao embarque e desembarque dos usuários do STP de Curitiba

+ **bd_pontos_de_onibus.php**: contém o script escrito em linguagem PHP responsável por montar sentença SQL responsável buscar na tabela transporte_dinamico.yp_pontos_onibus os dados referentes aos pontos de ônibus do STP de Curitiba

+ **index_main.php**: é arquivo mais importante da aplicação. Nele está contida toda a lógica de programação referente a criação dos gráficos, criação do mapa e também das camadas que podem ser adicionadas e removidas do mapa. As consultas quando disparadas são realizadas via chamada __Query.ajax__, a qual requisita os arquivos __bd_XXXXXX.php__ para obter os dados armazenados na base.
