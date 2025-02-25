### Exercícios de SQL

```sql
CREATE DATABASE catalogo_de_filmes CHARACTER SET utf8mb4;
```

```sql
CREATE TABLE generos(
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    generos VARCHAR(45) NOT NULL
);
```

```sql
CREATE TABLE filmes(
    idFilme INT NOT NULL PRIMARY KEY,
    titulo MEDIUMTEXT NOT NULL,
    lancamento VARCHAR(45) NOT NULL,
    generos_idGenero INT NOT NULL
);
```

```sql
CREATE TABLE detalhes(
    idDetalhes INT NOT NULL PRIMARY KEY,
    duracao INT(96),
    bilheteria DECIMAL,
    orcamento DECIMAL,
    filmes_idFILME INT NOT NULL
);
```

```sql
ALTER TABLE filmes
    ADD CONSTRAINT fk_generos_filmes
    FOREIGN KEY (generos_idGenero) REFERENCES generos(id);
    FOREIGN KEY (detalhes_idDetalhes) REFERENCES detalhes(id);
```