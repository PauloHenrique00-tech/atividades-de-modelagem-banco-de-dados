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
INSERT INTO detalhes(duracao, sinopse,filme_id)
```

```sql
INSERT INTO detalhes(duracao, sinopse, filme_id)
VALUES(
    127,
    'Deadpool & Wolverine reúne o icônico mercenário tagarela Wade Wilson (Ryan Reynolds) e o poderoso mutante Wolverine (Hugh Jackman) em uma aventura explosiva, escrita e produzida pelos mesmos talentos por trás de Deadpool (2016) e Deadpool 2 (2018). Wade Wilson desfruta de um momento de aparente calma ao lado de Vanessa (Morena Baccarin) e seus amigos e, em contra partida, Wolverine se recupera de seus ferimentos. Um têm os seus caminhos cruzados com o outro, dando início a uma improvável aliança. Juntos, eles enfrentam um inimigo formidável em comum, desencadeando uma jornada repleta de ação, humor e reviravoltas surpreendentes. Deadpool & Wolverine promete ser uma aventura épica, cheia de referências aos quadrinhos e momentos de pura adrenalina, proporcionando aos fãs uma experiência única e inesquecível no universo dos super-heróis.',
    1
), (
    125,
    'Após ser picado por uma libélula geneticamente alterada, Rick Riker (Drake Bell) tem sua vida alterada para sempre. Ele ganha superpoderes e passa a usá-los para combater o mal, sob a alcunha do Homem-Libélula. Entretanto Rick enfrenta um problema: sempre que tenta salvar alguém acaba matando-o acidentalmente. Apesar disto ele precisa enfrentar o Ampulheta, um vilão que deseja roubar a fonte de vida das pessoas para alcançar a imortalidade.',
    2
), (
    129,
    'Em um pântano distante vive Shrek (Mike Myers), um ogro solitário que vê, sem mais nem menos, sua vida ser invadida por uma série de personagens de contos de fada, como três ratos cegos, um grande e malvado lobo e ainda três porcos que não têm um lugar onde morar. Todos eles foram expulsos de seus lares pelo maligno Lorde Farquaad (John Lithgow). Determinado a recuperar a tranquilidade de antes, Shrek resolve encontrar Farquaad e com ele faz um acordo: todos os personagens poderão retornar aos seus lares se ele e seu amigo Burro (Eddie Murphy) resgatarem uma bela princesa (Cameron Diaz), que é prisioneira de um dragão. Porém, quando Shrek e o Burro enfim conseguem resgatar a princesa logo eles descobrem que seus problemas estão apenas começando.'
    3
), (
    157,
    'Em Demon Slayer - Mugen Train, durante o período Taisho no Japão, o jovem Tanjiro volta para casa depois de um dia de trabalho e encontra sua família brutalmente assassinada por um demônio. Para pior a situação, sua irmã mais jovem, Nezuko, foi transformada em uma criatura demoníaca. Agora ele precisará lutar para vingar sua família e recuperar a irmã.',
    4
);

UPDATE filmes SET nome = 'Demon Slayer - Mugen Train: O Filme' 
WHERE genero_id = 4;

DELETE from filmes WHERE id = 1;
```