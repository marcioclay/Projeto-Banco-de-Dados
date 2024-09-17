# COMANDOS DDL

#----------------------------------------------------------------------------------#

create database empresa;        	//cria uma base de dados 

#---------------------------------------------------------------#

use empresa;   				//abre a base de dados

#----------------------------------------------------------------#
					//cria as tabelas departamento e empregados
CREATE TABLE departamentos
( num_departamento INTEGER NOT NULL,
nome VARCHAR(40) NOT NULL,
localizacao VARCHAR(15) NOT NULL,
PRIMARY KEY (num_departamento)
);

CREATE TABLE empregados
( numero INTEGER NOT NULL,
nome VARCHAR(40) NOT NULL,
funcao VARCHAR(20) NOT NULL,
salario DECIMAL(10,2) NOT NULL,
premios INTEGER DEFAULT NULL,
num_departamento INTEGER NOT NULL,
PRIMARY KEY (numero),
FOREIGN KEY (num_departamento) REFERENCES
departamentos (num_departamento)
);

#----------------------------------------------------------------------------------#

					//apaga uma tabela
DROP TABLE departamentos;

#----------------------------------------------------------------------------------#


					#//alterar a estrutura de uma tabela (cria/ atualiza/exclui COLUNAS)

					// ADICIONAR COLUNA

ALTER TABLE empregados
ADD (sexo CHAR(1) DEFAULT 'F' CHECK (sexo IN ('M', 'F'))
); 


					// ALTERA OS TIPOS DE DADOS NA COLUNA

ALTER TABLE empregados
MODIFY sexo CHAR(3);

					// ADICIONA COLUNA DE CHAVE PRIMARIA NA TABELA

ALTER TABLE departamentos
ADD primary key(num_departamento);


					// REMOVE COLUNA

ALTER TABLE empregados
DROP sexo;

#----------------------------------------------------------------------------------#
Inserir dados na Tabela
INSERT into departamentos (num_departamento,nome,localizacao) values(5,'secretaria','sala');
select *from departamentos;
