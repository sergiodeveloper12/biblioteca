create table Cliente (
Cod_Cliente int not null ,
Nome varchar(50) not null,
CPF varchar (20) not null,
Telefonw varchar(20) not null,
Email varchar(40) not null,
inicio_emprestimo datetime,
fim_emprestimo datetime,
primary key (Cod_cliente)



use biblioteca;
 insert into estante (titulo, autor,editora,edição,Genero_literario,Ano_lançamento, emprestimo_habilitado)
 values 	('Bibia', 'J.ferreira Almeida', 'Mundial Records','1','Cristianismo','2019','N');

select * from estante;


delete from estante
where id_livro ='44';


select titulo,Genero_Literario from estante
order by titulo desc ;



update estante
set editora = 'Ed.Thomas Nelson'
where id_livro ='2';

alter table estoque
add column Ano_lançamento varchar(20);


alter table estoque
drop dados_enntrega;


alter table estoque
add dados_entrega varchar(50);

desc estante;


	select * from  estante ;



desc cliente;




alter table cliente
add column telefone varchar (20);

desc estoque ;


alter table cliente
add foreign key (livro_preferido) references estante (id_livros);


select * from cliente;

alter table cliente
add column livro_gosto int (20) not null;



alter table cliente
add foreign key (livro_gosto) references estante(id_livro); 


insert into cliente ( Cod_cliente, Nome, CPF,Email,inicio_emprestimo,fim_emprestimo,telefone,livro_gosto)
values
('003','', '22483452833','serginhophn@gmail.com', '2023-05-13 11:00:00','2023-06-13 10:59:59','11980131918','1');



SELECT estante.titulo , cliente.nome
FROM estante 
JOIN cliente ON id_livro = cliente.livro_gosto
WHERE Cod_cliente = 2;



use biblioteca ;










create  table estoque
(
ID_Livro int not null auto_increment,
nome_Livro varchar(50),
editora varchar (50),
Qtd_adquirida varchar(50),
dados_compra date,
dados_enntrega date,
primary key (ID_Livro))





