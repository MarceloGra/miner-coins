Mineração de dinheiros virtuais
==========

1) Crie uma conta no portal MinerGate, ela será necessária para você minerar moedas digitais.

2) Crie uma conta no Changelly, será usado posteriormente para transferir as moedas para uma carteira.

Basicamente, minera-se as moedas de menor valor para conversão no Bitcoin ou no Ethereum, pois minerar as citadas não compensa pelo alto consumo de energia e fraco resultado.

### Configurando um ambiente

Processo realizado com o Ubuntu 14.04 LTS.

* Rode no terminal isso para atualizar o S.O:
`sudo apt-get upgrade`
`sudo apt-get update`

* Instale as dependências
`sudo apt-get install build-essential autotools-dev autoconf libcurl3 libcurl4-gnutls-dev`

* Instale o GIT (se não tiver ainda) e baixe repositório:
`git clone https://github.com/OhGodAPet/cpuminer-multi`

* No diretório...
`cd cpuminer-multi/`

* Dê a permissão para executar
`chmod +x autogen.sh`

* Rode esse arq
`./autogen.sh`

* Defina as flags 
`CFLAGS="-march=native" ./configure`

* Execute o make (Instale se não tiver ainda)
`make`

* Do instalation...
`sudo make install`

### Executando o minerador no ambiente

NOTA: Todas as "Threads -1" serão utilizadas, certifique-se de ter ao menos 2 CPUs se for rodar em uma VM.

* Execute o algoritmo cryptonight, para isso será usado a conta criada anteriormente...
`./minerd -a cryptonight -o stratum+tcp://bcn.pool.minergate.com:45550 -u SEU_EMAIL -p x`

