# Comandos para operações CRUD no Banco de Dados

- C -> **C**reate -> **INSERT**: inserir dados/registros na tabela
- R -> **R**ead   -> **SELECT**: consultar/ler dados/registros na tabela
- U -> **U**pdate -> **UPDATE**: atualizar dados/registros na tabela
- D -> **D**elete -> **DELETE**: excluir dados/registros na tabela

---

## INSERT (Fabricantes)

```SQL
INSERT INTO fabricantes (nome) VALUES('Asus');
INSERT INTO fabricantes (nome) VALUES('Dell');
INSERT INTO fabricantes (nome) VALUES('Apple');

INSERT INTO fabricantes (nome) VALUES('LG'),('Samsung'),('Brastemp');
```

## SELECT (Fabricantes)

```sql
SELECT * FROM fabricantes;
```

---

### INSERT (Produtos)

```sql
INSERT INTO produtos(nome, descricao, preco, quantidade, fabricante_id)
VALUES(
    'Ultrabook', 
    'Equipamento de última geração cheio de recusos, e etc e tal...',
    3999.45,
    7,
    2  -- id dp fabricante Dell
);

INSERT INTO produtos(nome, descricao, preco, quantidade, fabricante_id)
VALUES(
    'Tablet Android',
    'Tablet com a versão 16 do sistema operacional Android, possui tela de 10 polegadas e armazenamento de 128gb. Estou sem ideia do que escrever aqui.',
    900,
    12,
    5   -- Samsung 
);

INSERT INTO produtos(nome, descricao, preco, quantidade, fabricante_id)
VALUES(
    'Geladeira',
    'Refrigerador frost-free com acesso à Internet',
    5000,
    12,
    6  -- Brastemp
), (
    'Iphone 18 Pro Max Ferradão',
    'Smartphone Apple cheio das frescuras e caro pra caramba... coisa de rico...',
    666.66,
    3,
    3 -- Apple
), (
    'iPad Mini',
    'Tablet Apple com tela retina display e bla bla bla mó bunitinha',
    4999.12,
    5,
    3 -- Apple
);
```

## Comandos do exercício

```sql
INSERT INTO fabricantes (nome) VALUES('Positivo');
INSERT INTO fabricantes (nome) VALUES('Microsoft');
```

```sql
INSERT INTO produtos(nome, descricao, preco, quantidade, fabricante_id)
VALUES(
    'Xbox Series S',
    'Velocidade e desempenho de última geração',
    1997,
    5,
    8 -- Microsoft
), (
    'Notebook Motion',
    'Intel Dual Core 4GB de RAM, 128GB SSD e Tela 14,1 polegadas',
    1213.65,
    8,
    7 -- Positivo
);
```

## SELECT (Produtos)

```sql
-- Lendo TODAS as colunas de TODOS os registros
SELECT * FROM produtos;

-- Lendo somente o nome e preco de todos os registros
SELECT nome, preco FROM produtos;
SELECT preco, nome FROM produtos;

-- Mostrar nome, preco e quantidade SOMENTE dos produtos que custam abaixo de 5000
SELECT nome, preco, quantidade FROM produtos
WHERE preco < 5000;

-- Mini-exercício: mostre o nome e descrição somente dos produtos da Apple

SELECT nome, descricao FROM produtos WHERE fabricante_id = 3;
```

### Operadores Lógicos: E, OU e NÃO

#### E (AND)

```sql
-- Exibir nome e preco dos produtos que custam entre 2000 e 6000
SELECT nome, preco FROM produtos
WHERE preco >= 2000 AND preco <= 6000;
```

#### OU (OR)

```sql
-- Mini-exercício: exibir nome, descrição dos produtos da Apple e da Samsung
SELECT nome, descricao FROM produtos WHERE fabricante_id = 3 OR fabricante_id = 5;

-- Versão usando a função SQL IN()
SELECT nome, descricao FROM produtos
WHERE fabricante_id IN(3,5);
```

#### NÃO (NOT)

```sql
-- Nome e descrição e preco de todos os produtos EXCETO da Positivo
SELECT nome, descricao, preco FROM produtos
WHERE NOT fabricante_id = 8;

-- Versão usando operador relacional de "diferença/diferente"
SELECT nome, descricao, preco FROM produtos
WHERE fabricante_id !=8;
```