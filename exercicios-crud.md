### INSERT (generos)

```sql
INSERT INTO generos(nome) VALUES('Ação');
INSERT INTO generos(nome) VALUES('Comédia');
INSERT INTO generos(nome) VALUES('Fantasia');
INSERT INTO generos(nome) VALUES('Aventura');
```

```sql
INSERT INTO filmes(titulo, lancamento, genero_id) 
VALUES(
    'Deapool e Wolverine',
    '2024-06-25',
    1
), (
    'Super-Herói: O Filme',
    '2008-03-28',
    2
), (
    'Shrek',
    '2001-06-22',
    3
), (
    'Demon Slayer: Infinity Train',
    '2021-05-13',
    4
);
```

```sql
INSERT INTO detalhes(duracao, sinopse, bilheteria, orcamento, filme_id)
```

```sql
INSERT INTO detalhes(duracao, sinopse, bilheteria, orcamento, filme_id)
VALUES(
    127,
    'Deadpool & Wolverine reúne o icônico mercenário tagarela Wade Wilson (Ryan Reynolds) e o poderoso mutante Wolverine (Hugh Jackman) em uma aventura explosiva, escrita e produzida pelos mesmos talentos por trás de Deadpool (2016) e Deadpool 2 (2018). Wade Wilson desfruta de um momento de aparente calma ao lado de Vanessa (Morena Baccarin) e seus amigos e, em contra partida, Wolverine se recupera de seus ferimentos. Um têm os seus caminhos cruzados com o outro, dando início a uma improvável aliança. Juntos, eles enfrentam um inimigo formidável em comum, desencadeando uma jornada repleta de ação, humor e reviravoltas surpreendentes. Deadpool & Wolverine promete ser uma aventura épica, cheia de referências aos quadrinhos e momentos de pura adrenalina, proporcionando aos fãs uma experiência única e inesquecível no universo dos super-heróis.',
    1.300.000.000,
)
```