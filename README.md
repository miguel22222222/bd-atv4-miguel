# bd-atv4-miguel
CREATE DATABASE escola;
USE escola;

CREATE TABLE aluno (
	id INT PRIMARY KEY,
	nome VARCHAR(100),
    matricula VARCHAR(20)
);
CREATE TABLE professores (
	id_aluno INT AUTO_INCREMENT,
    nome VARCHAR(100),
    idade INT,
    materia VARCHAR(50)
    PRIMARY KEY (id_aluno)
);
CREATE TABLE funcionarios (
	id INT PRIMARY KEY,
    nome VARCHAR(100),
    cargo VARCHAR(50),
    salario float
);
CREATE TABLE telefone (
	id_telefone INT AUTO_INCREMENT,
	numero VARCHAR(20),
    id_aluno INT,
    PRIMARY KEY (id_telefone),
    FOREIGN KEY (id_aluno) REFERENCES aluno(id_aluno)
 
ALTER TABLE aluno
MODIFY nome VARCHAR(150);

ALTER TABLE aluno
ADD telefone VARCHAR(15);

DROP TABLE aluno;
DROP DATABASE escola;
