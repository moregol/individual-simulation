# Introdução
Simulação de foguetemodelismo a fim de comparar resultados númericos entre openrocket e rocketpy. A simulação foi feita utilizando um foguete criado no openrocket com um apogeu de 4024 metros.

# Metodo
O foguete foi criado no OpenRocket com todas suas peças sendo arbitrárias sendo o único ponto observado seu apogeu, contém uma estabilidade de 2.74.

Para ser comparado os resultados com o RocketPY, foi utilizada a biblioteca [Rocket Serializer](https://github.com/RocketPy-Team/RocketSerializer) gerando um notebook ja pronto com os foguetes e as peças.

# Resultado 
A principal diferenças de ambos é a drag curve(RASAero) e o fator enviroment, o que causou uma diferença final de 450 metros totais.

Entretanto, caso sejam mantidas o drag curve do OpenRocket e o enviroment padrão, a diferença cai para 3 metros totais.

Foram executadas 4 simulações, uma com o mesmo env e drag, uma com o mesmo env mas com o drag curve do RASAero, uma com o mesmo drag curve e diferente env e uma com ambos parametros diferentes.

Os notebooks estão abaixo para visualização dos resultados. (Não há necessidade de rodar o notebook, os resultados ja estão salvos no arquivo)

# Notebooks

Sem diferença de parametro: [link](https://colab.research.google.com/github/moregol/individual-simulation/blob/main/v5/nodiffSim.ipynb) - 3 metros de diferença - OrK: 4024m - RocketPY: 4021m

Diferença apenas no Env: [link](https://colab.research.google.com/github/moregol/individual-simulation/blob/main/v5/EnvDiffSim.ipynb) - 13 metros de diferença - OrK: 4024m - RocketPY: 4037m

Diferença apenas na Drag Curve: [link](https://colab.research.google.com/github/moregol/individual-simulation/blob/main/v5/dragDiffSim.ipynb)  - 424 metros de diferença - OrK: 4024m - RocketPY: 4444m

Ambos parametros diferentes: [link](https://colab.research.google.com/github/moregol/individual-simulation/blob/main/v5/dragEnvSim.ipynb) - 452 metros de diferença - OrK: 4024m - RocketPY: 4476m

# Explicação dos Arquivos

Todos os arquivos utilizados estão na pasta v5, abaixo está o que cada um representa para caso desejam testar individualmente.

| Arquivo           | Explicação                                                           |
|-------------------|----------------------------------------------------------------------|
| IndividualV5.ork  | Arquivo do foguete do OpenRocket                                     |
| drag_curve.csv    | Arquivo da curva de arrasto do OpenRocket                            |
| poweron.csv       | Arquivo da curva de arrasto com power on do RASAero                  |
| poweroff.csv      | Arquivo da curva de arrasto com power off do RASAero                 |
| thrust_source.csv | Arquivo do motor do OpenRocket                                       |
| nodiffsim.ipynb   | Arquivo da simulação com os mesmos parametros                        |
| dragDiffSim.ipynb | Arquivo da simulação com diferença na drag curve usando a do RASAero |
| EnvDiffSim.ipynb  | Arquivo da simulação com diferença no enviroment metereologico       |
| dragEnvSim.ipynb  | Arquivo da simulação com diferença em ambos parametros.              |
