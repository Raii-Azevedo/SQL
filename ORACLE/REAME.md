## SQL - ORACLE
 - O SQL é a linguagem de manuntenção de servidores de Bancos de Dados.
 - Através do SQL formam vários especialístas como:
     - DBA: Administrador de Banco dades
       - É responsável pela manuntenção dos servidores de banco de dados. É p profissional que vai garantir que o sistema está funcionando 24hs por dia. Vai fazer a manuntenção e garantir o backup de dados.
     - AD: Administrado de Dados
       -  Profissional que conhece a fundo o processo empresarial, define tabelas que serão criadas e os relacionamentos entre essas tabelas.
    - DB: Desenvolvedor de Banco de Dados
      - O DB tem um grande conhecimento de lógica de programação e responsávelpor criar rotinas e gerenciar os processos que são feitos dentro do próprio SGBD.

## INSTALANDO ORACLE NO UBUNTU
Instalação e Configuração do Oracle Express Edition e SQL Developer no Ubuntu


Aqui estão os passos para instalar o Oracle Express Edition (XE) e o SQL Developer no Ubuntu:

	-Instalar o Oracle Express Edition (XE)
	A Oracle não fornece pacotes oficiais do Oracle XE para Ubuntu. No entanto, você pode usar o pacote RPM fornecido pela Oracle e convertê-lo para o formato DEB usando a ferramenta alien. Siga estes passos:

	a. Baixe o pacote RPM do Oracle XE do site oficial da Oracle: https://www.oracle.com/database/technologies/xe-downloads.html

	b. Instale as dependências necessárias:

			-sudo apt-get update
			-sudo apt-get install alien libaio1 unixodbc

c. Converta o pacote RPM para DEB e instale-o:

			- sudo alien --scripts -d oracle-xe-18c-*.rpm
			- sudo dpkg -i oracle-xe_18c-*.deb

d. Configure o Oracle XE:

			- sudo /etc/init.d/oracle-xe-18c configure

e. Adicione as variáveis de ambiente: 

			echo 'export ORACLE_HOME=/opt/oracle/product/18c/dbhomeXE' >> ~/.bashrc
			echo 'export PATH=$PATH:$ORACLE_HOME/bin' >> ~/.bashrc
			echo 'export ORACLE_SID=XE' >> ~/.bashrc 
			
- Em seguida:
			source ~/.bashrc
			
			
#### Créditos ao:
-[Fábio Bebert](https://www.vivaolinux.com.br/dica/Instalacao-e-Configuracao-do-Oracle-Express-Edition-e-SQL-Developer-no-Ubuntu)
