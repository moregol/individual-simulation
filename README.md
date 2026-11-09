# Introdução
A simulação foi feita utilizando um foguete criado no openrocket com um apogeu de 4024 metros.

# Metodo
O foguete foi criado no OpenRocket com todas suas peças sendo arbitrárias sendo o único ponto observado seu apogeu, contém uma estabilidade de 2.74.

Para ser comparado os resultados com o RocketPY, foi utilizada a biblioteca [Rocket Serializer](https://github.com/RocketPy-Team/RocketSerializer) gerando um notebook ja pronto com os foguetes e as peças.

# Resultado 
A principal diferenças de ambos é a drag curve(RASAero) e o fator enviroment, o que causou uma diferença final de 400 metros totais.

Entretanto, caso sejam mantidas o drag curve do OpenRocket e o enviroment padrão, a diferença cai para 3 metros totais.

Foram executadas 4 simulações, uma com o mesmo env e drag, uma com o mesmo env mas com o drag curve do RASAero, uma com o mesmo drag curve e diferente env e uma com ambos parametros diferentes.

Os notebooks estão abaixo para visualização dos resultados. (Não há necessidade de rodar o notebook, os resultados ja estão salvos no arquivo)

# Notebooks

Sem diferença de parametro: [link](https://colab.research.google.com/github/moregol/individual-simulation/blob/main/v5/nodiffSim.ipynb)

Diferença apenas no Env: [link](https://colab.research.google.com/github/moregol/individual-simulation/blob/main/v5/EnvDiffSim.ipynb)

Diferença apenas na Drag Curve: [link](https://colab.research.google.com/github/moregol/individual-simulation/blob/main/v5/dragDiffSim.ipynb)

Ambos parametros diferentes: [link](https://colab.research.google.com/github/moregol/individual-simulation/blob/main/v5/dragEnvSim.ipynb)
