### Exercícios de SQL

```sql
CREATE DATABASE catalogo_de_filmes_corrigido CHARACTER SET utf8mb4;
```

```sql
CREATE TABLE generos(
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(45) NOT NULL
);
```

```sql
CREATE TABLE filmes(
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    titulo VARCHAR(200) NOT NULL,
    lancamento DATE NOT NULL,
    genero_id INT NOT NULL -- será uma FK (chave estrangeira)
);
```

```sql
CREATE TABLE detalhes(
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    duracao INT NOT NULL,
    sinopse TEXT(1000) NOT NULL,
    bilheteria DECIMAL(16,2) NULL,
    orcamento DECIMAL(16,2) NULL,
    filme_id INT NOT NULL --- será um FK (chave estrangeira)
);
```

## Alterando as tabelas e configurando as chaves estrangeiras (FKs)

```sql
ALTER TABLE filmes
    ADD CONSTRAINT fk_filmes_generos
    FOREIGN KEY(genero_id) REFERENCES generos(id);
```

```sql
ALTER TABLE detalhes
    ADD CONSTRAINT fk_detalhes_filmes
    FOREIGN KEY(filme_id) REFERENCES filmes(id);
```