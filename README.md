# Esquema conceitual para banco de dados

## Descrição do projeto

<p align="justify">Este desafio de projeto consiste na criação de modelo conceitual que posterioemente será utilizado como base para criação dos modelos lógico e físico. O cenário de uma oficina mecãnica foi utilizado para a criação deste modelo. A proposta é desenvolver um banco de dados para a atender às seguintes demandas.</p>

- Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica.
- Clientes levam veículos à oficina mecânica para serem consertados ou para passarem por revisões  periódicas.
- Cada veículo é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma OS com data de entrega.
- A partir da OS, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra.
- O valor de cada peça também irá compor a OSO cliente autoriza a execução dos serviços.
- A mesma equipe avalia e executa os serviços.
- Os mecânicos possuem código, nome, endereço e especialidade.
- Cada OS possui: n°, data de emissão, um valor, status e uma data para conclusão dos trabalhos.

## Modelo Conceitual
- Imagem Modelo Conceitual desenvolvido no software BRMW.
<div aling="center">
 <img src="https://github.com/FredericoSander/Esquema_conceitual_para_banco_de_dados/blob/main/Img/Esquema%20conceitual.png">
</div>

## Entidades

<p align="justify">As entidades dos bancos de dados são a representação de um objeto ou conceito do mundo real relevante para o sistema que está sendo desenvolvido. Em termos práticos, as entidades são às tabelas do banco de dados. Toda entidade possue atributos, que são as caracteristicas ou propriedades utilizadas para descrever a entidade. No banco de dados, cada atributo torna-se uma coluna dentro da tabela.</p>
O modelo conceitual porpoem a criação de 6 entidades para projeto de banco de dados, sendo elas:

- Clientes
- Fornecedor
- Funcionários
- Estoque
- Ordem de Serviço
- Serviços

### Entidade Cliente

<p align="justify">A entidade Cliente armazena as informações de todos os clientes da oficina mecânica, como Nome, Sobrenome, CPF e Endereço. Por meio do relacionamento com a entidade Ordem de Serviço, é possível rastrear todas ordem de serviço que forma geradas para cada cliente, com suas respectivas <b>Data da OS, Status da OS e Data de entregas</b> dos serviço.</p>

### Entidade Fornecedor

<p align="justify">A entidade Fornecedor armazena as informações de todos os Fornecedores da oficina mecânica, como <b>Razão Social, Nome Fantasia, CNPJ ou CPF e Endereço</b>. A entidade Fornecedor está relacionada a entidade Estoque e, por meio deste relacionamento, é possivel verificar quais são dos produto foram mais vendidos por cada fornecedor, possibilitando uma comparação de valores de produtos semelhantes.</p>

### Entidade Funcionários

<p align="justify">A entidade Funcionários armazena as informações de todos os Funcionários da oficina mecânica, como de <b>Nome, Sobrenome, CPF, Cargo, Data de admissão, Data de Aniversário e Endereço</b>. A entidade Funcionários está relacionada a entidade Ordem de Serviço e, por meio deste relacionamento, é possivel verificar quais Ordem de Serviço foram direcionadas a cada funcionário, possibilitando um rastreamento da produtividade de cada um.</p>

### Estoque

<p align="justify">A entidade Estoque recebe as informações de todos os produtos utilizados da oficina mecânica, como <b>Nome do Produto, Valor de Compra, Valor de Venda e Quantidade</b>. A entidade Estoque está relacionada às entidades Fornecedor e Ordem de Serviço. Por meio do relacionamento entre Estoque e Fornecedor, é possivel verificar quais são dos produtos que foram vendidos e seus respectivos fornecedores, possibilitando uma comparação de valores de produtos semelhantes. Por meio do relacionamento entre Estoque e Ordem de Serviço é possivel verificar quais produto 
que foram solicitados para cada Ordem de Serviço e seus respectivos valores de venda.</p>

### Ordem de Serviço

<p align="justify">A entidade Ordem de Serviço aramazena as informações <b>IdServiço, Data da OS, Data da Entrega, Status do Serviço</b>. Essas informações são geradas durante a criação da Ordem de Serviço, e por meio de relacionamentos possibilitam o rastreamento dos serviços a serem realizados, dos produtos utilizados que estão disponíveis na entidade Estoque e dos funcionário que executaram os serviços</p>

Por meio do relacionamento entre as entidades é possível rastrear todo o processo de criação das ordens de serviços, funcionários que executaram os serviços e valores dos serviços realizados.

## Autor

- [Frederico S N Cota](https://github.com/FredericoSander)