# Módulo 5 — Modelagem Física e SQL Básico

## 🎯 Objetivos
Aprender a transformar o modelo lógico em um modelo físico e criar estruturas no SGBD.

## 🧠 Conceitos

### Modelo Físico
É o modelo **implementado no SGBD** (MySQL, PostgreSQL, SQL Server...).

Inclui:
- Tipos de dados (INT, VARCHAR, DATE)
- Índices
- Restrições (NOT NULL, UNIQUE, DEFAULT)
- Integridade referencial
- Particionamento, quando necessário

## 🧱 Exemplos SQL

### Criação de Tabelas
```sql
CREATE TABLE Professor (
  id_prof INT PRIMARY KEY AUTO_INCREMENT,
  nome VARCHAR(100) NOT NULL,
  especialidade VARCHAR(100)
);
```

### Inserção de Dados
```sql
INSERT INTO Professor (nome, especialidade)
VALUES ('Carlos Lima', 'Banco de Dados');
```

### Consulta
```sql
SELECT nome FROM Professor WHERE especialidade = 'Banco de Dados';
```

## 📌 Índices e Performance
- Crie índices em colunas usadas em WHERE, JOIN e ORDER BY.
- Evite indexar colunas com baixa seletividade (ex.: booleanas).
- Monitore consultas com EXPLAIN / EXPLAIN ANALYZE.

## 🔒 Restrições e Integridade
- NOT NULL para campos obrigatórios.
- UNIQUE para colunas que devem ser únicas.
- FOREIGN KEYS para integridade referencial.
