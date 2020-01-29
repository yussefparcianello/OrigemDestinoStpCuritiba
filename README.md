# OrigemDestinoStpCuritiba
Protótipo de visualização de dados de Origem-Destino do Sistema de Transporte Público de Curitiba


## Principais arquivos da aplicação
+ **index.php**: é o arquivo inicial da aplicação. É responsável por dividir a interface de usuário verticalmente ao meio, estabelecendo à esquerda da tela a região do mapa e do menu, e à direita da tela a região dos gráficos

+ **tela_inicial.php**: é o arquivo responsável pela construção do menu de busca da aplicação

+ **bd_rois.php**: contém o script escrito em linguagem PHP responsável por montar sentença SQL responsável buscar na tabela transporte_dinamico.yp_rois os dados referentes aos contornos das Regiões de Interesse oferecidas pela aplicação para explorar os dados de OD do STP de Curitiba

+ **bd_terminais.php**: contém o script escrito em linguagem PHP responsável por montar sentença SQL responsável buscar na tabela transporte_dinamico.yp_terminais os dados referentes aos terminais de embarque e desembarque do STP de Curitiba

+ **bd_movimentacao.php**: contém o script escrito em linguagem PHP responsável por montar sentença SQL responsável buscar na tabela transporte_dinamico.np_movimentacao os dados referentes ao embarque e desembarque dos usuários do STP de Curitiba

+ **bd_pontos_de_onibus.php**: contém o script escrito em linguagem PHP responsável por montar sentença SQL responsável buscar na tabela transporte_dinamico.yp_pontos_onibus os dados referentes aos pontos de ônibus do STP de Curitiba

+ **index_main.php**: é arquivo mais importante da aplicação. Nele está contida toda a lógica de programação referente a criação dos gráficos, criação do mapa e também das camadas que podem ser adicionadas e removidas do mapa. As consultas quando disparadas são realizadas via chamada _Query.ajax_, a qual requisita os arquivos _bd_XXXXXX.php_ para obter os dados armazenados na base.


## Dicionário de dados das tabelas utilizadas pelo protótipo
|   Esquerda   |  Centralizado  |    Direita    |
| :---         |     :---:      |          ---: |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |



\hline
\multicolumn{1}{|c|}{\textbf{Tabela}}           & \multicolumn{1}{c|}{\textbf{Campo}} & \multicolumn{1}{c|}{\textbf{Descrição}}        \\ \hline
\multicolumn{1}{|c|}{\multirow{4}{*}{rois}} & id                                  & Identificador da tupla                         \\ \cline{2-3} 
\multicolumn{1}{|c|}{}                          & lat                                 & Coordenada de latitude (SRID 4326)             \\ \cline{2-3} 
\multicolumn{1}{|c|}{}                          & lng                                 & Coordenada de longitude (SRID 4326)            \\ \cline{2-3} 
\multicolumn{1}{|c|}{}                          & geom                                & Geometria (SRID 29192)                         \\ \hline

%\multicolumn{1}{|c|}{\textbf{Tabela}}           & \multicolumn{1}{c|}{\textbf{Campo}} & \multicolumn{1}{c|}{\textbf{Descrição}}        \\ \hline
\multirow{4}{*}{pontos\_onibus}             & id                                  & Identificador da tupla                         \\ \cline{2-3} 
                                                & lat                                 & Coordenada de latitude (SRID 4326)             \\ \cline{2-3} 
                                                & lng                                 & Coordenada de longitude (SRID 4326)            \\ \cline{2-3} 
                                                & geom                                & Geometria (SRID 29192)                         \\ \hline

%\multicolumn{1}{|c|}{\textbf{Tabela}}           & \multicolumn{1}{c|}{\textbf{Campo}} & \multicolumn{1}{c|}{\textbf{Descrição}}        \\ \hline
\multirow{5}{*}{terminais}                  & id                                  & Identificador da tupla                         \\ \cline{2-3} 
                                                & nome                                & Descrição do terminal                          \\ \cline{2-3} 
                                                & lat                                 & Coordenada de latitude (SRID 4326)             \\ \cline{2-3} 
                                                & lng                                 & Coordenada de longitude (SRID 4326)            \\ \cline{2-3} 
                                                & geom                                & Geometria (SRID 29192)                         \\ \hline

%\multicolumn{1}{|c|}{\textbf{Tabela}}           & \multicolumn{1}{c|}{\textbf{Campo}} & \multicolumn{1}{c|}{\textbf{Descrição}}        \\ \hline
\multirow{18}{*}{movimentacao}              & codlinha                            & Código da linha operada pelo ônibus            \\ \cline{2-3} 
                                                & nomelinha                           & Nome da linha operada pelo ônibus              \\ \cline{2-3} 
                                                & codveiculo                          & Código do veículo em operação                  \\ \cline{2-3} 
                                                & cartao\_numero                      & Número do cartão do passageiro                 \\ \cline{2-3} 
                                                & cartao\_datahora                    & Data-hora do uso do cartão do passageiro       \\ \cline{2-3} 
                                                & cartao\_data                        & Data do uso do cartão do passageiro            \\ \cline{2-3} 
                                                & cartao\_hora                        & Hora do uso do cartão do passageiro            \\ \cline{2-3} 
                                                & cartao\_data\_nascimento            & Data de nascimento do passageiro               \\ \cline{2-3} 
                                                & cartao\_sexo                        & Sexo do passageiro                             \\ \cline{2-3} 
                                                & origem\_lat                         & Coordenada de latitude da origem (SRID 4326)   \\ \cline{2-3} 
                                                & origem\_lng                         & Coordenada de longitude da origem (SRID 4326)  \\ \cline{2-3} 
                                                & origem\_datahora                    & Data-hora do embarque                          \\ \cline{2-3} 
                                                & destino\_lat                        & Coordenada de latitude do destino (SRID 4326)  \\ \cline{2-3} 
                                                & destino\_lng                        & Coordenada de longitude do destino (SRID 4326) \\ \cline{2-3} 
                                                & destino\_datahora                   & Data-hora do desembarque                       \\ \cline{2-3} 
                                                & origem                              & Geometria do ponto de origem (SRID 29192)      \\ \cline{2-3} 
                                                & destino                             & Geometria do ponto de destino (SRID 29192)     \\ \cline{2-3} 
                                                & idade                               & Idade do passageiro                            \\ \hline
%\end{tabular}
\end{tabular}%
}
\end{table}
