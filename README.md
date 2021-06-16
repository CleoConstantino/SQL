Curso de SQL realizado na plataforma da Rocketseat - 06/2021

**Tipos de campos:**
- *Text:* texto;
- *Number:* número;
- *Datatime:* data e tempo;
- *Primary Key:* chave primária, deve ser sempre um campo NUMBER, é o identificador da informação ÚNICA;
- *Foreign Key:* chave estrangeira, faz a relação de uma tabela com a outra, faz referencia a primary key de outra tabela ;
- *Unique:* comando usado para informar que o conteúdo do campo não pode se repetir; 
**- Regras para escrever nome de tabelas e de campos:**
1 - Deve começar por uma letra do alfabeto;
2 - Os caracteres seguintes não são permitidos: ( ) + - / * ; = & | # > < ^ ' { } %
3 - Não pode conter espaços;
4 - Não pode conter acentuação;
5 - Ex: nome_de_usuario, id_user.
 
**Operadores relacionais:**
- O operador igual (=)  só funciona em campos que são NUMBER, ex: `SELECT * FROM aluno WHERE cpf = 45678945645;`
- O operador like funciona para campos do tipo texto (substitui o campo =) e o texto deve estar entre "aspas", ex: `SELECT * FROM aluno WHERE nome like "jakeliny gracielly";` 
- A % é usada para informar ao banco que o texto que vem antes ou em seguida não importa, ex: `SELECT * FROM aluno WHERE nome like "%jozefina%"`
- Operador maior que, ex: `SELECT * FROM aluno WHERE matricula > 1`
- Operador menor que, ex: `SELECT * FROM aluno WHERE matricula < 3`
- Operador maior ou igual, ex: `SELECT * FROM aluno WHERE matricula >= 2`
- Operador menor ou igual, ex: `SELECT * FROM aluno WHERE matricula <= 3`
- Operador não igual a, ex: `SELECT * FROM aluno WHERE matricula <> 3`
- Operador diferente de, ex: `SELECT * FROM aluno WHERE matricula != 3` 

**Operadores matemáticos:**

- Adição +, ex: `SELECT * FROM aluno WHERE matricula = 1 + 1`
- Subtração - , ex: `SELECT * FROM aluno WHERE matricula = 3 - 1`
- Multiplicação `*` , ex:  `SELECT * FROM aluno WHERE matricula = 3 * 1`
- Divisão /, ex: `SELECT * FROM aluno WHERE matricula = 3 / 1`
- Módulo %, é o número que resta de uma divisão ex:  `SELECT * FROM aluno WHERE matricula = 3 % 1`

Operadores lógicos:

- *AND:* serve para juntar 2 condições no WHERE: `SELECT * FROM aluno WHERE nome like "J%" AND matricula < 2`
- *OR:* serve para atender uma das condições ou as duas: `SELECT * FROM aluno WHERE matricula > 1 OR nome like "j%"`
- *BETWEEN e NOT BETWEEN*: serve para buscar entre intervalos, ao utilizar o NOT ele vai buscar fora daquele intervalo: `SELECT * FROM funcionarios WHERE id_funcionario NOT BETWEEN 4 and 7`
- *IN e NOT IN:* serve para agrupar as informações, ao utilizar o NOT ele vai buscar as informações diferente das informadas: `SELECT * FROM funcionarios WHERE id_departamento NOT IN (1, 3, 5)`
- *IS NULL e IS NOT NULL:* `NULL significa que o campo está vazio: SELECT * FROM funcionarios WHERE id_departamento IS NULL`

**Mais comandos:**

- *INSERT INTO:* serve para inserir informações:  `INSERT INTO aluno (nome, cpf, responsavel) VALUES ("Maria Luiza", 45678912345, "Wantuil Soares")`
- *UPDATE:* serve para alterar algum dado que já foi inserido na tabela: `UPDATE aluno SET nome="Mariano Soares", responsavel="Marcio Soares" WHERE matricula = 2`
- DELETE: permite apagar uma informação apaga o registro e não um campo: `DELETE FROM aluno WHERE matricula = 3`

**Unindo tabelas:**

- JOIN: o comando de unir tabelas é importante principalmente no momento que precisa fazer um SELECT:  `SELECT * FROM funcionarios JOIN departamentos ON departamentos.id_dept = funcionarios.id_departamento`
- JOIN com WHERE: `SELECT * FROM funcionarios JOIN departamentos ON departamentos.id_dept = funcionarios.id_departamento WHERE departamentos.id_pedt = 2`
- JOIN especificando campos: `SELECT funcionarios.nome, funcionarios.cpf, departamentos.descrcao FROM funcionarios JOIN departamentos ON departamentos.id_dept = funcionarios.id_departamento`
- Alias: pode ser utilizado para abreviação do nome da tabela ou alterar o nome dos campos e funciona apenas dentro do SELECT: `SELECT func.nome as "Nome", func.cpf as "CPF", dept.descricao as "Departamento" FROM funcionarios as func JOIN departamentos as dept ON func.id_departamento = dept.id_dept`
- LEFT OUTER JOIN: faz com que todo o conteúdo da tabela que está na frente do FROM apareça mesmo que não tenha um relacionamento no ON: `SELECT * FROM departamentos LEFT OUTER JOIN funcionarios ON funcionarios.id_departamento = departamentos.id_dept`

**Comandos avançados:**

- ORDER BY:
- LIMIT:
- OFFSET:
- COUNT:
- GROUP BY:
- JOIN, GROUP BY e COUNT juntos:
- HAVING:

**Comandos nas tabelas:**

- CREATE TABLE:
- ALTER TABLE:
- DROP TABLE:
