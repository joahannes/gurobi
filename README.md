### Passos para instalação e configuração do Gurobi 9.0

1. Baixar o gurobi no site oficial: [LINK](http://www.gurobi.com/)

2. Descompactar arquivo baixado:

	> tar -zxf gurobi9.0.0_linux64.tar.gz

3. Adicionar variáveis de ambiente no .bashrc:

	> gedit ~/.bashrc

	> export GUROBI_HOME="/PATH/gurobi900/linux64"

	> export PATH="${PATH}:${GUROBI_HOME}/bin"

	> export LD_LIBRARY_PATH="${LD_LIBRARY_PATH}:${GUROBI_HOME}/lib"

	> export GRB_LICENSE_FILE=/home/usuario/gurobi.lic

4. Obter licença (pegar numeração no site do Gurobi):

	> ./grbgetkey 48715054-15e6-11ea-8e81-020d093b5256

5. Compilar Gurobi:

	> cd [GRB_path]/linux64/src/build

	> make

	> cp libgurobi_c++.a ../../lib/

6. Instalar pacotes Python:

	> sudo python setup.py install
