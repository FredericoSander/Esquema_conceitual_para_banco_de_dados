# Esquema Conceitual para Oficina Mecânica

## Descrição do Projeto
Este desafio de projeto consiste na criação de um modelo conceitual que será utilizado como base para os modelos lógico e físico de um banco de dados. O cenário escolhido é o de uma oficina mecânica. O objetivo é desenvolver um sistema de controle e gerenciamento de ordens de serviço.

### Requisitos do Sistema
- Os clientes levam veículos à oficina para conserto ou revisão.
- Cada veículo é designado a uma equipe de mecânicos que identifica os serviços necessários e preenche uma Ordem de Serviço (OS).
- A partir da OS, calcula-se o valor dos serviços com base em uma tabela de referência de mão de obra.
- O valor das peças também compõe o total da OS.
- O cliente autoriza a execução dos serviços.
- A mesma equipe avalia e executa os serviços.

## Modelo Conceitual
O modelo conceitual foi desenvolvido utilizando o software BRMW e é composto por 6 entidades principais: **Clientes**, **Fornecedor**, **Funcionários**, **Estoque**, **Ordem de Serviço** e **Serviços**. Cada uma dessas entidades possui atributos que descrevem suas características e estão interligadas por relacionamentos.

### Entidades e Relacionamentos

#### 1. **Cliente**
A entidade **Cliente** armazena informações sobre os clientes da oficina, como nome, sobrenome, CPF e endereço completo. Esta entidade se relaciona com a entidade **Ordem de Serviço**, permitindo rastrear todas as OS geradas para cada cliente.

**Atributos:**
- `idCliente` (chave primária)
- Nome
- Sobrenome
- CPF
- Endereço (logradouro, número, bairro, cidade, estado, país)

#### 2. **Fornecedor**
A entidade **Fornecedor** armazena informações sobre os fornecedores da oficina, como razão social, nome fantasia, CNPJ e endereço. Está relacionada à entidade **Estoque**, permitindo verificar quais produtos são fornecidos por cada fornecedor.

**Atributos:**
- `idFornecedor` (chave primária)
- Razão Social
- Nome Fantasia
- CNPJ
- Endereço (logradouro, número, bairro, cidade, estado, país)

#### 3. **Funcionários**
A entidade **Funcionários** armazena informações sobre os funcionários da oficina, como nome, sobrenome, CPF, cargo, data de admissão e endereço. Está relacionada à entidade **Ordem de Serviço**, permitindo rastrear quais OS foram atribuídas a cada funcionário.

**Atributos:**
- `idFuncionario` (chave primária)
- Nome
- Sobrenome
- CPF
- Cargo
- Data de Admissão
- Data de Aniversário
- Endereço (logradouro, número, bairro, cidade, estado, país)

#### 4. **Estoque**
A entidade **Estoque** armazena informações sobre os produtos utilizados na oficina, como nome do produto, valor de compra, valor de venda e quantidade. Está relacionada às entidades **Fornecedor** e **Ordem de Serviço**.

**Atributos:**
- `idProduto` (chave primária)
- Nome do Produto
- Valor do Produto
- Quantidade

#### 5. **Ordem de Serviço (OS)**
A entidade **Ordem de Serviço** armazena informações sobre as ordens de serviço geradas na oficina, como data da emissão, data da entrega, status do serviço e valores.

**Atributos:**
- `idOrdemServico` (chave primária)
- Data da OS
- Data de Entrega
- Status do Serviço

#### 6. **Serviços**
A entidade **Serviços** armazena informações sobre os serviços oferecidos pela oficina, como nome do serviço, tipo de serviço e valor.

**Atributos:**
- `idServico` (chave primária)
- Nome
- Tipo de Serviço
- Valor do Serviço

### Relacionamentos

- **OS-Cliente:** Cada cliente pode ter várias ordens de serviço, mas cada OS está associada a um único cliente.
- **OS-Funcionários:** Cada ordem de serviço pode ser executada por vários funcionários.
- **OS-Estoque:** As ordens de serviço consomem produtos do estoque.
- **OS-Serviços:** Cada ordem de serviço pode incluir vários serviços.
- **Fornecedor-Estoque:** Cada fornecedor fornece vários produtos para o estoque.

## Imagem do Modelo Conceitual
A imagem do modelo conceitual ilustra as entidades, atributos e relacionamentos descritos acima. Cada entidade está conectada a outras por meio de relacionamentos que facilitam o rastreamento e a análise dos dados.

![Modelo conceitual](https://github.com/FredericoSander/Esquema_conceitual_para_banco_de_dados/blob/main/Img/Esquema%20conceitual.png)

## Conclusão
O modelo conceitual apresentado atende às necessidades do sistema de controle e gerenciamento de ordens de serviço para uma oficina mecânica. Ele garante que todas as informações relevantes sejam armazenadas de maneira estruturada e que os relacionamentos entre os dados permitam uma análise eficiente das operações da oficina.

---

## Autor

- [Frederico S N Cota](https://github.com/FredericoSander)