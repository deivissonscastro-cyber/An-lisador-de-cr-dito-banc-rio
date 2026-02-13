-- Projeto: Consulta de Elegibilidade de Crédito
-- Objetivo: Filtrar clientes com tempo de conta e saldo positivo

-- 1. Criando a tabela de simulação
CREATE TABLE clientes_banco (
    id_cliente INT PRIMARY KEY,
    nome VARCHAR(100),
    saldo_conta DECIMAL(10, 2),
    meses_cliente INT
);

-- 2. Inserindo dados de teste
INSERT INTO clientes_banco VALUES (1, 'Deivisson Castro', 5000.00, 12);
INSERT INTO clientes_banco VALUES (2, 'João Silva', 1500.00, 3);
INSERT INTO clientes_banco VALUES (3, 'Maria Oliveira', -200.00, 24);

-- 3. Consulta de clientes aptos para análise (Saldo > 0 e mais de 6 meses de conta)
SELECT nome, saldo_conta, meses_cliente 
FROM clientes_banco
WHERE saldo_conta > 0 AND meses_cliente >= 6;
