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