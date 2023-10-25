# Revisão M03 Pt.2

### Criando um banco de dados chamado "loja"

```sql
create database loja;
```

### Deletando um banco de dados chamado "loja"

```sql
drop database if exists loja;
```

### Criando uma tabela chamada "produtos"

```sql
create table if not exists produtos (
  id serial primary key,
  nome text,
  preco integer,
  ativo boolean
);
```

### Inserindo registros na tabela "produtos"

```sql
-- Notebook Samsung
insert into produtos (nome, preco, ativo) values ('Notebook Samsung', 50000, true);
-- Mouse Dell
insert into produtos (nome, preco, ativo) values ('Mouse Dell', 2500, true);
-- Monitor Samsung
insert into produtos (nome, preco, ativo) values ('Monitor Samsung', 30000, false);
```

### Listando todos os registros da tabela "produtos"

```sql
select * from produtos;
```

### Listando todos os registros da tabela "produtos" onde o id é igual a "3"

```sql
select * from produtos where id = 3;
```

### Alterando o preço do produto onde o id igual a "1"

```sql
update produtos set preco = 100000 where id = 1;
```

### Deletando o produto onde o id igual a "2"

```sql
delete from produtos where id = 2;
```

### Criando uma tabela chamada "categorias"

```sql
create table if not exists categorias (
 	id serial primary key,
  nome text
);
```

### Inserindo registros na tabela "categorias"

```sql
-- Eletrônicos e Tecnologia
insert into categorias (nome) values ('Eletrônicos e Tecnologia');
-- Alimentação
insert into categorias (nome) values ('Alimentação');
```

### Listando todos os registros da tabela "categorias"

```sql
select * from categorias;
```

### Alterando a tabela "produtos"

```sql
-- Adicionando coluna categoria
alter table produtos add column categoria integer;
-- Deletando coluna categoria
alter table produtos drop column categoria;
-- Criando coluna categoria_id
alter table produtos add column categoria_id integer;
```

### Criando uma chave estrangeira na tabela "produtos" vinculada a tabela "categorias"

Uma chave estrangeira é um campo, que aponta para a chave primária de outra tabela gerando assim uma relação entre as duas tabelas

```sql
alter table produtos add constraint fk_categoria_produto_id
foreign key (categoria_id) references categorias(id);
```

### Alterando a "categoria_id" de todos os registros da tabela "produtos"

OBS: cuidado ao fazer updates e deletes sem o **where**

```sql
update produtos set categoria_id = 1;
```

### Listando a tabela "produtos" e "categorias" juntas

```sql
select
produtos.id,
produtos.nome,
produtos.preco,
categorias.nome as categoria
from produtos
inner join categorias
on categorias.id = produtos.categoria_id;
```

![](https://dq-blog.s3.amazonaws.com/top-20-SQL-JOINs-interview-questions-and-answers/image-1.png)

## Funções

### "count" conta a quantidade de registros de uma tabela

```sql
select count(*) from produtos;
```

## "as" cria um apelido para a coluna

```sql
select count(*) as quantidade_produtos from produtos;
```

### "||" ou "concat" junta campos

```sql
select nome || ' - ' || preco as descricao from produtos;
--ou
select concat(nome,' - ', preco) as descricao from produtos;
```

### "avg" gera a média de uma coluna

```sql
select avg(preco) from produtos;
```

### "round" aredonda o valor da coluna

```sql
select round(avg(preco)) from produtos;
-- ou
select round(avg(preco), 2) from produtos;
-- ou
select round(45.898777);
```

### "min" pega o menor valor da coluna

```sql
select min(preco) from produtos;
```

### "max" pega o maior valor da coluna

```sql
select max(preco) from produtos;
```

### "sum" soma os valores da coluna

```sql
select sum(preco) from produtos;
```

### "::" ou "cast" converter tipo de uma coluna

```sql
select preco::text from produtos;
--ou
select cast(preco as text) from produtos;
```

### "now" gerar Data

```sql
select now();
```

### "coalesce" traz o primeiro não nulo(null)

```sql
select coalesce(preco) from produtos;
-- ou
select coalesce(null, 52, preco) from produtos;
```

### "group by" agrupa por coluna

```sql
select sum(preco) from produtos group by categoria_id;
```

### "order by" ordena por coluna "asc" (crescente) "desc" (decrecente)

```sql
select * from produtos order by preco asc;
-- ou
select * from produtos order by preco desc;
```

### verificando uma coluna

```sql
-- maior que 30000
select * from produtos where preco > 30000;
-- menor que 30000
select * from produtos where preco < 30000;
-- diferente que 30000
select * from produtos where preco <> 30000;
-- igual a 30000
select * from produtos where preco = 30000;
-- diferente de nulo (null)
select * from produtos where preco is not null;
-- limitado a 1 registro
select * from produtos limit 1;
-- seta quando começa a listagem (muito usado em páginação)
select * from produtos limit 10 offset 0;
-- pega todos os registros que possuem no nome a palavra "Samsung"
select * from produtos where nome like '%Samsung%'
```
