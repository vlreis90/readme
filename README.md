# Documentação dos Scripts SQL - Teste Senior NeoBPO

Este documento fornece uma visão geral e instruções de uso para os arquivos SQL fornecidos, que são parte de uma solução para gerenciar dados e análises em um sistema de banco de dados.

## Arquivos

### 1. Questão 1

- **Descrição**: Este script contém procedimentos para inserção e atualização de dados detalhados de despesas. São feitas validações da existêncidas das tabelas que irão receber os dados e criação das mesmas caso não existam. Além disso, há uma lógica para importar dados de um arquivo CSV para uma tabela temporária e, posteriormente, mover esses dados para a tabela principal.
- **Instruções de Uso**:
  - Certifique-se de substituir `'!!!!! Insira aqui o caminho para o arquivo !!!!!\\CONVERTIDO\\DESPESAS.csv'` no comando BULK INSERT pelo caminho correto do arquivo CSV.
  - Execute o script em um ambiente que suporte transações SQL, como Microsoft SQL Server.

### 2. Questão 2

- **Descrição**: Este script contém uma sequência de passos para exemplificar como tratar possíveis conflitos de dados em Tempo real em um banco de dados de estoque de vendas, para minimizar conflitos de estoque foram implementadas transações com controle de concorrência, que pode ser aplicado através da chave estrangeira e também a inclusão de um lock para evitar vendas simultâneas. .
- **Instruções de Uso**:
  - Use este script para entender como implementar transações robustas e tratamento de erros em suas operações de banco de dados.
  - As seções de tratamento de erros podem ser adaptadas para outros scripts ou procedimentos armazenados para aumentar a robustez do sistema.

### 3. Questão 3

- **Descrição**: Este script tem como intuito exemplificar boas práticas para otimização de consultas para relatórios com grandes volumes de dados, como exemplo este configura uma tabela `Posts` para análises de sentimento, incluindo a criação de índices para otimização de consultas. Também fornece exemplos de consultas otimizadas que utilizam esses índices.
- **Instruções de Uso**:
  - Execute o script para criar a tabela e os índices.
  - Utilize as consultas fornecidas como exemplos para desenvolver outras consultas específicas conforme necessário.
  - Periodicamente, reconstrua os índices para manter o desempenho do banco de dados, utilizando os comandos fornecidos no final do script.

## Recomendações Gerais

- Revise cada script e ajuste os caminhos dos arquivos e outros parâmetros específicos do ambiente antes de executar.
- Realize backups regulares antes de realizar operações de importação ou atualização em massa.
- Monitore o desempenho do banco de dados e ajuste os índices conforme necessário para otimizar a velocidade de consulta.

## Autor
 Valério Luiz Dantas Reis (valerio.reis@neobpo.com.br)

