# disciplinaBancoDeDados
Banco de dados criado para trabalho da disciplina da faculdade 

-- Database: BancoDeDadosONG

-- DROP DATABASE IF EXISTS "BancoDeDadosONG";

CREATE DATABASE "BancoDeDadosONG"
    WITH
    OWNER = postgres
    ENCODING = 'UTF8'
    LC_COLLATE = 'Portuguese_Brazil.1252'
    LC_CTYPE = 'Portuguese_Brazil.1252'
    TABLESPACE = pg_default
    CONNECTION LIMIT = -1[doacoes.csv](https://github.com/user-attachments/files/17090798/doacoes.csv)

    IS_TEMPLATE = False;

COMMENT ON DATABASE "BancoDeDadosONG"
    IS 'Banco de dados criado para ONG Anjos de 4 patas, para o controle das doações de ração recebidas.';

    CREATE TABLE DOACOES (
CODIGO int NOT NULL, 
MARCA varchar(50) NOT NULL, 
PESO int NOT NULL, 
VALIDADE date NOT NULL, 
DATARECEBIDO date NULL, 
DOADOR varchar(50) NULL,
CONSTRAINT IDDOACAO PRIMARY KEY (CODIGO)
);

INSERT INTO DOACOES (CODIGO, MARCA, PESOKG, VALIDADE, DATARECEBIDO, DOADOR)
VALUES (1,"Monello",1,"2024-12-20","2024-07-01","anonimo")
VALUES (2,"Gran Plus",1,"2025-01-01",NULL,"anonimo")
VALUES (3,"Nutrilus",1,"2025-03-30",NULL,"anonimo")
VALUES (4,"Monello",1,"2025-02-08","2024-08-20","anonimo")
VALUES (5,"Magnus",5,"2025-04-10","2024-08-01","Mariana Ferreira")
VALUES (6,"Special Dog",5,"2025-05-12","2024-08-30","anonimo")
VALUES (7,"Gran Plus",5,"2025-04-03","2024-07-25","anonimo")

